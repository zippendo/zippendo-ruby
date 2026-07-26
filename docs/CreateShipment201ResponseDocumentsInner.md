# Zippendo::CreateShipment201ResponseDocumentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique document identifier. |  |
| **shipment_id** | **String** | Identifier of the shipment this document belongs to. |  |
| **document_type** | **String** | Type of shipment document. |  |
| **format** | **String** | File format of the document content. |  |
| **content** | **String** | Base64-encoded document/label content. |  |
| **size** | **String** | Physical print size of the document. | [default to &#39;A4&#39;] |
| **created_at** | **String** | Timestamp when the document was created. |  |
| **updated_at** | **String** | Timestamp when the document was last updated. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseDocumentsInner.new(
  id: doc_8f3a2b1c,
  shipment_id: shp_4d9e7a2f,
  document_type: label,
  format: pdf,
  content: JVBERi0xLjQKJeLjz9MKMS...,
  size: 100X150,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z
)
```

