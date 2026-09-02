# Zippendo::OrderChannelsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_order_channel**](OrderChannelsApi.md#create_order_channel) | **POST** /orgs/{orgId}/order-channels | Create order channel |
| [**create_order_channel_webhook_secret**](OrderChannelsApi.md#create_order_channel_webhook_secret) | **POST** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Create or rotate webhook signing secret |
| [**delete_order_channel**](OrderChannelsApi.md#delete_order_channel) | **DELETE** /orgs/{orgId}/order-channels/{channelId} | Delete order channel |
| [**get_order_channel**](OrderChannelsApi.md#get_order_channel) | **GET** /orgs/{orgId}/order-channels/{channelId} | Get order channel |
| [**get_order_channel_webhook_status**](OrderChannelsApi.md#get_order_channel_webhook_status) | **GET** /orgs/{orgId}/order-channels/{channelId}/webhooks | Get channel webhook status |
| [**list_order_channels**](OrderChannelsApi.md#list_order_channels) | **GET** /orgs/{orgId}/order-channels | List order channels |
| [**revoke_order_channel_webhook_secret**](OrderChannelsApi.md#revoke_order_channel_webhook_secret) | **DELETE** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Revoke webhook signing secret |
| [**update_order_channel**](OrderChannelsApi.md#update_order_channel) | **PATCH** /orgs/{orgId}/order-channels/{channelId} | Update order channel |


## create_order_channel

> <ListOrderChannels200ResponseDataInner> create_order_channel(org_id, create_order_channel_request)

Create order channel

Creates a new order channel for an organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
create_order_channel_request = Zippendo::CreateOrderChannelRequest.new({name: 'Anna's webshop', type: 'manual'}) # CreateOrderChannelRequest | 

begin
  # Create order channel
  result = api_instance.create_order_channel(org_id, create_order_channel_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->create_order_channel: #{e}"
end
```

#### Using the create_order_channel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrderChannels200ResponseDataInner>, Integer, Hash)> create_order_channel_with_http_info(org_id, create_order_channel_request)

```ruby
begin
  # Create order channel
  data, status_code, headers = api_instance.create_order_channel_with_http_info(org_id, create_order_channel_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrderChannels200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->create_order_channel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_order_channel_request** | [**CreateOrderChannelRequest**](CreateOrderChannelRequest.md) |  |  |

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_order_channel_webhook_secret

> <CreateOrderChannelWebhookSecret201Response> create_order_channel_webhook_secret(org_id, channel_id)

Create or rotate webhook signing secret

Generates (or rotates) the custom channel's webhook signing secret used to authenticate order pushes to the ingest URL. The secret is returned only once. Rotating invalidates the previous secret immediately.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
channel_id = 'clz9k2f0a0001abcd1234efgh' # String | Order channel ID.

begin
  # Create or rotate webhook signing secret
  result = api_instance.create_order_channel_webhook_secret(org_id, channel_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->create_order_channel_webhook_secret: #{e}"
end
```

#### Using the create_order_channel_webhook_secret_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateOrderChannelWebhookSecret201Response>, Integer, Hash)> create_order_channel_webhook_secret_with_http_info(org_id, channel_id)

```ruby
begin
  # Create or rotate webhook signing secret
  data, status_code, headers = api_instance.create_order_channel_webhook_secret_with_http_info(org_id, channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateOrderChannelWebhookSecret201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->create_order_channel_webhook_secret_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **channel_id** | **String** | Order channel ID. |  |

### Return type

[**CreateOrderChannelWebhookSecret201Response**](CreateOrderChannelWebhookSecret201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_order_channel

> <RevokeApiToken200Response> delete_order_channel(org_id, channel_id)

Delete order channel

Deletes an order channel and cascades deletion of its orders.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
channel_id = 'clz9k2f0a0001abcd1234efgh' # String | Order channel ID.

begin
  # Delete order channel
  result = api_instance.delete_order_channel(org_id, channel_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->delete_order_channel: #{e}"
end
```

#### Using the delete_order_channel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RevokeApiToken200Response>, Integer, Hash)> delete_order_channel_with_http_info(org_id, channel_id)

```ruby
begin
  # Delete order channel
  data, status_code, headers = api_instance.delete_order_channel_with_http_info(org_id, channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RevokeApiToken200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->delete_order_channel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **channel_id** | **String** | Order channel ID. |  |

### Return type

[**RevokeApiToken200Response**](RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_order_channel

> <ListOrderChannels200ResponseDataInner> get_order_channel(org_id, channel_id)

Get order channel

Returns a single order channel by ID, including its linked shipping rules.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
channel_id = 'clz9k2f0a0001abcd1234efgh' # String | Order channel ID.

begin
  # Get order channel
  result = api_instance.get_order_channel(org_id, channel_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->get_order_channel: #{e}"
end
```

#### Using the get_order_channel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrderChannels200ResponseDataInner>, Integer, Hash)> get_order_channel_with_http_info(org_id, channel_id)

```ruby
begin
  # Get order channel
  data, status_code, headers = api_instance.get_order_channel_with_http_info(org_id, channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrderChannels200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->get_order_channel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **channel_id** | **String** | Order channel ID. |  |

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_order_channel_webhook_status

> <GetOrderChannelWebhookStatus200Response> get_order_channel_webhook_status(org_id, channel_id)

Get channel webhook status

Returns whether webhooks are enabled and lists the webhooks registered with the platform.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
channel_id = 'clz9k2f0a0001abcd1234efgh' # String | Order channel ID.

begin
  # Get channel webhook status
  result = api_instance.get_order_channel_webhook_status(org_id, channel_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->get_order_channel_webhook_status: #{e}"
end
```

#### Using the get_order_channel_webhook_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrderChannelWebhookStatus200Response>, Integer, Hash)> get_order_channel_webhook_status_with_http_info(org_id, channel_id)

```ruby
begin
  # Get channel webhook status
  data, status_code, headers = api_instance.get_order_channel_webhook_status_with_http_info(org_id, channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrderChannelWebhookStatus200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->get_order_channel_webhook_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **channel_id** | **String** | Order channel ID. |  |

### Return type

[**GetOrderChannelWebhookStatus200Response**](GetOrderChannelWebhookStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_order_channels

> <ListOrderChannels200Response> list_order_channels(org_id, opts)

List order channels

Returns a paginated list of order channels for an organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20, # Integer | Items per page (max 100)
  brand_id: 'brnd_8f3kd92ld0', # String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
  brand_scope: 'own', # String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
  type: 'shopify', # String | Filter by channel type.
  enabled: 'true', # String | Filter by enabled state.
  search: 'Anna's Shopify Store' # String | Search by channel name.
}

begin
  # List order channels
  result = api_instance.list_order_channels(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->list_order_channels: #{e}"
end
```

#### Using the list_order_channels_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrderChannels200Response>, Integer, Hash)> list_order_channels_with_http_info(org_id, opts)

```ruby
begin
  # List order channels
  data, status_code, headers = api_instance.list_order_channels_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrderChannels200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->list_order_channels_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |
| **brand_id** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brand_scope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] |
| **type** | **String** | Filter by channel type. | [optional] |
| **enabled** | **String** | Filter by enabled state. | [optional] |
| **search** | **String** | Search by channel name. | [optional] |

### Return type

[**ListOrderChannels200Response**](ListOrderChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## revoke_order_channel_webhook_secret

> <RevokeOrderChannelWebhookSecret200Response> revoke_order_channel_webhook_secret(org_id, channel_id)

Revoke webhook signing secret

Revokes the custom channel's webhook signing secret. All subsequent pushes to the ingest URL are rejected until a new secret is generated.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
channel_id = 'clz9k2f0a0001abcd1234efgh' # String | Order channel ID.

begin
  # Revoke webhook signing secret
  result = api_instance.revoke_order_channel_webhook_secret(org_id, channel_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->revoke_order_channel_webhook_secret: #{e}"
end
```

#### Using the revoke_order_channel_webhook_secret_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RevokeOrderChannelWebhookSecret200Response>, Integer, Hash)> revoke_order_channel_webhook_secret_with_http_info(org_id, channel_id)

```ruby
begin
  # Revoke webhook signing secret
  data, status_code, headers = api_instance.revoke_order_channel_webhook_secret_with_http_info(org_id, channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RevokeOrderChannelWebhookSecret200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->revoke_order_channel_webhook_secret_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **channel_id** | **String** | Order channel ID. |  |

### Return type

[**RevokeOrderChannelWebhookSecret200Response**](RevokeOrderChannelWebhookSecret200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_order_channel

> <ListOrderChannels200ResponseDataInner> update_order_channel(org_id, channel_id, update_order_channel_request)

Update order channel

Updates an order channel and its linked shipping rules.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrderChannelsApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
channel_id = 'clz9k2f0a0001abcd1234efgh' # String | Order channel ID.
update_order_channel_request = Zippendo::UpdateOrderChannelRequest.new # UpdateOrderChannelRequest | 

begin
  # Update order channel
  result = api_instance.update_order_channel(org_id, channel_id, update_order_channel_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->update_order_channel: #{e}"
end
```

#### Using the update_order_channel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrderChannels200ResponseDataInner>, Integer, Hash)> update_order_channel_with_http_info(org_id, channel_id, update_order_channel_request)

```ruby
begin
  # Update order channel
  data, status_code, headers = api_instance.update_order_channel_with_http_info(org_id, channel_id, update_order_channel_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrderChannels200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling OrderChannelsApi->update_order_channel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **channel_id** | **String** | Order channel ID. |  |
| **update_order_channel_request** | [**UpdateOrderChannelRequest**](UpdateOrderChannelRequest.md) |  |  |

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

