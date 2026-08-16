# Zippendo::ConnectCarrierRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Carrier display name |  |
| **carrier_slug** | **String** | Carrier slug identifier |  |
| **config** | [**Hash&lt;String, ListCarriers200ResponseDataInnerConfigValue&gt;**](ListCarriers200ResponseDataInnerConfigValue.md) | Carrier configuration (required and optional fields) |  |
| **brand_id** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ConnectCarrierRequest.new(
  name: PostNord,
  carrier_slug: postnord,
  config: {&quot;customerNumber&quot;:&quot;123456&quot;},
  brand_id: brnd_8f3kd92ld0
)
```

