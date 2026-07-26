# Zippendo::UpdateOrgBrandingRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **primary_color** | **String** | Primary brand color (hex) — tints the document title and table headers | [optional] |
| **secondary_color** | **String** | Secondary brand color (hex) — tints the subtitle, section headings, and totals accent | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateOrgBrandingRequest.new(
  primary_color: #1D4ED8,
  secondary_color: #F59E0B
)
```

