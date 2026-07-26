# Zippendo::ListAvailableCarriers200ResponseInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Display name of the carrier |  |
| **slug** | **String** | Unique carrier slug identifier |  |
| **group** | **String** | Carrier group or family name | [optional] |
| **description** | **String** | Short description of the carrier | [optional] |
| **logo** | **String** | URL to the carrier logo image | [optional] |
| **brand_color** | **String** | Carrier brand color (hex) | [optional] |
| **learn_more_url** | **String** | URL with more information about the carrier | [optional] |
| **required_fields** | [**Array&lt;ListAvailableCarriers200ResponseInnerRequiredFieldsInner&gt;**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Configuration fields that must be provided to connect the carrier | [optional] |
| **optional_fields** | [**Array&lt;ListAvailableCarriers200ResponseInnerRequiredFieldsInner&gt;**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Optional configuration fields for the carrier | [optional] |
| **deprecated** | **Boolean** | Whether this integration is deprecated (still works, but discouraged) | [optional] |
| **deprecation_message** | **String** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListAvailableCarriers200ResponseInner.new(
  name: PostNord,
  slug: postnord,
  group: Nordic,
  description: Nordic postal and parcel carrier,
  logo: https://cdn.zippendo.com/carriers/postnord.svg,
  brand_color: #0072CE,
  learn_more_url: https://www.postnord.dk,
  required_fields: null,
  optional_fields: null,
  deprecated: true,
  deprecation_message: The standalone Instabox API is deprecated. Migrate to the Instabee-powered Instabox integration.
)
```

