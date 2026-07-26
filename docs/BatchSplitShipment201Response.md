# Zippendo::BatchSplitShipment201Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **original_shipment** | [**CreateShipment201Response**](CreateShipment201Response.md) |  |  |
| **new_shipments** | [**Array&lt;CreateShipment201Response&gt;**](CreateShipment201Response.md) | Newly created shipments resulting from the split. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSplitShipment201Response.new(
  original_shipment: null,
  new_shipments: null
)
```

