# Zippendo::CreateShipment201ResponseTracking

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Public carrier tracking URL. | [optional] |
| **number** | **String** | Carrier tracking number. | [optional] |
| **label_free_code** | **String** | Label-free drop-off code. | [optional] |
| **qr_code_link** | **String** | DEPRECATED — use &#x60;qrCodeDataUri&#x60; (embeddable data URI) or &#x60;qrCodeUrl&#x60; (hosted link). Catch-all that carries whichever applies, kept populated for backwards compatibility during the migration and until it is disabled. | [optional] |
| **qr_code_data_uri** | **String** | Embeddable &#x60;data:&#x60; URI of the QR code image for label-free drop-off — base64 image bytes you can drop straight into an &lt;img&gt;/email. Null when the carrier returns a hosted link instead (see &#x60;qrCodeUrl&#x60;). | [optional] |
| **qr_code_url** | **String** | Carrier-hosted URL of the QR code image for label-free drop-off, returned by carriers (e.g. Bring) that link to the image rather than embedding it. Null when the carrier returns embeddable bytes (see &#x60;qrCodeDataUri&#x60;). | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseTracking.new(
  url: https://tracking.postnord.com/00370724710000012345,
  number: 00370724710000012345,
  label_free_code: AB12CD34,
  qr_code_link: data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mNk+M9QDwADhgGAWjR9awAAAABJRU5ErkJggg&#x3D;&#x3D;,
  qr_code_data_uri: data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mNk+M9QDwADhgGAWjR9awAAAABJRU5ErkJggg&#x3D;&#x3D;,
  qr_code_url: https://qr.bring.com/label-free/AB12CD34.png
)
```

