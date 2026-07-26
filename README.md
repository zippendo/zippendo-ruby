# Zippendo Ruby SDK

Official Ruby client for the [Zippendo](https://zippendo.com) shipping & logistics API. Requires
Ruby 2.7+.

## Install

```sh
gem install zippendo
```

## Authentication

Create an API token in your Zippendo dashboard (**Settings → API tokens**) — a Bearer token prefixed
with `zipp_`. Configure it once:

```ruby
require "zippendo"

Zippendo.configure do |config|
  config.access_token = ENV["ZIPPENDO_API_TOKEN"]
end
```

The base URL defaults to `https://api.zippendo.com`.

## Resources & clients

The API is split into resource clients — `ShipmentsApi`, `OrdersApi`, `CarriersApi`, `AddressesApi`,
`RulesApi`, `WebhooksApi`, `TokensApi`, and more:

```ruby
shipments = Zippendo::ShipmentsApi.new
orders = Zippendo::OrdersApi.new
```

## The `org_id` parameter

Every call takes an `org_id` (your organization ID, found in the dashboard). It is explicit on each
call by design: one API token can be granted access to multiple organizations, and `org_id` selects
which one the request acts on.

## Listing & pagination

List endpoints accept `:page` (1-based) and `:limit`, and return a page with `data` plus `total`,
`page`, `limit`, and `total_pages`:

```ruby
result = shipments.list_shipments("org_8f3kd92ld0", page: 1, limit: 50)
puts result.data                       # Array<Shipment>
puts "#{result.total} / #{result.total_pages}"
```

## Creating resources

```ruby
order = orders.create_order("org_8f3kd92ld0", Zippendo::CreateOrderRequest.new(
  order_number: "1001",
  order_channel_id: "chan_7d2k1",
  order_lines: [Zippendo::CreateOrderRequestOrderLinesInner.new(name: "T-shirt", quantity: 2)]
))
puts order.id
```

See [`./docs`](./docs) for the full request/response shape of every operation.

## Error handling

Non-2xx responses raise `Zippendo::ApiError`. The body is Zippendo's canonical
`{ code, error, message }` — branch on the machine-readable `code`:

```ruby
begin
  shipments.get_shipment("org_8f3kd92ld0", "shp_missing")
rescue Zippendo::ApiError => e
  puts e.code            # HTTP status
  puts e.response_body   # JSON, e.g. {"code":"SHIPMENT_NOT_FOUND", ...}
end
```

## Configuration

Point the client at a different environment by overriding the host:

```ruby
Zippendo.configure do |config|
  config.access_token = ENV["ZIPPENDO_API_TOKEN"]
  config.host = "staging.api.zippendo.com"
end
```

## Reference

Full per-endpoint and per-model documentation is in [`./docs`](./docs). Hosted reference:
<https://www.zippendo.com/docs/api-reference/overview>.

## License

[MIT](./LICENSE.md)
