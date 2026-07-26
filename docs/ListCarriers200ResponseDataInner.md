# Zippendo::ListCarriers200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique carrier identifier |  |
| **name** | **String** | Carrier display name |  |
| **carrier_slug** | **String** | Carrier slug identifier |  |
| **config** | [**Hash&lt;String, ListCarriers200ResponseDataInnerConfigValue&gt;**](ListCarriers200ResponseDataInnerConfigValue.md) | Carrier configuration (required and optional fields) |  |
| **org_id** | **String** | Owning organization ID |  |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601) |  |
| **logo** | **String** | Carrier logo URL | [optional] |
| **brand_color** | **String** | Carrier brand color (hex) | [optional] |
| **deprecated** | **Boolean** | Whether this carrier integration is deprecated (still works, but discouraged) | [optional] |
| **deprecation_message** | **String** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarriers200ResponseDataInner.new(
  id: carr_01HZX9K2QF,
  name: PostNord,
  carrier_slug: postnord,
  config: {&quot;customerNumber&quot;:&quot;123456&quot;},
  org_id: org_01HZX9K2QF,
  created_at: 2026-06-22T09:00:00.000Z,
  updated_at: 2026-06-22T09:00:00.000Z,
  logo: https://cdn.zippendo.com/logos/postnord.svg,
  brand_color: #005BAA,
  deprecated: true,
  deprecation_message: The standalone Instabox API is deprecated. Migrate to the Instabee-powered Instabox integration.
)
```

