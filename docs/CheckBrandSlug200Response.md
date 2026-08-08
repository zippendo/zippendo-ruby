# Zippendo::CheckBrandSlug200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slug** | **String** | The slug that was checked |  |
| **available** | **Boolean** | Whether the slug is free within this organization |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CheckBrandSlug200Response.new(
  slug: acme,
  available: true
)
```

