# Zippendo::CreateShipmentRequestParcelsInnerDimensions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **length** | **Float** | Parcel length in centimetres. |  |
| **width** | **Float** | Parcel width in centimetres. |  |
| **height** | **Float** | Parcel height in centimetres. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipmentRequestParcelsInnerDimensions.new(
  length: 30,
  width: 20,
  height: 15
)
```

