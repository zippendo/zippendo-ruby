# Zippendo::UpdateCarrierRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Carrier display name | [optional] |
| **carrier_slug** | **String** | Carrier slug identifier | [optional] |
| **config** | [**Hash&lt;String, ListCarriers200ResponseDataInnerConfigValue&gt;**](ListCarriers200ResponseDataInnerConfigValue.md) | Carrier configuration (required and optional fields) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateCarrierRequest.new(
  name: GLS,
  carrier_slug: gls,
  config: {&quot;customerNumber&quot;:&quot;123456&quot;}
)
```

