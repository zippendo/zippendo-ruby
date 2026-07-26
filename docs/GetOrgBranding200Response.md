# Zippendo::GetOrgBranding200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **primary_color** | **String** | Primary brand color (hex) |  |
| **secondary_color** | **String** | Secondary brand color (hex) |  |
| **logo_url** | **String** | Authenticated URL to download the org logo image, or null if no logo is set |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrgBranding200Response.new(
  primary_color: #1D4ED8,
  secondary_color: #F59E0B,
  logo_url: /orgs/org_123/branding/logo
)
```

