# Zippendo::SplitShipmentParcelRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parcels** | [**Array&lt;SplitShipmentParcelRequestParcelsInner&gt;**](SplitShipmentParcelRequestParcelsInner.md) | Target parcel layout to redistribute order lines into. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::SplitShipmentParcelRequest.new(
  parcels: null
)
```

