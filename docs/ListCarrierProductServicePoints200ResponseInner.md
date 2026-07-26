# Zippendo::ListCarrierProductServicePoints200ResponseInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **lat** | **Float** | Latitude of the service point |  |
| **lng** | **Float** | Longitude of the service point |  |
| **name** | **String** | Name of the service point |  |
| **service_point_id** | **String** | Unique service point identifier |  |
| **opening_hours** | **Array&lt;String&gt;** | Opening hours of the service point | [optional] |
| **description** | **String** | Additional description of the service point | [optional] |
| **distance** | **Float** | Distance from the searched location in meters | [optional] |
| **address** | [**ListCarrierProductServicePoints200ResponseInnerAddress**](ListCarrierProductServicePoints200ResponseInnerAddress.md) |  | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProductServicePoints200ResponseInner.new(
  lat: 55.6761,
  lng: 12.5683,
  name: PostNord Pakkeshop Netto,
  service_point_id: 1234567,
  opening_hours: null,
  description: Located inside Netto supermarket,
  distance: 320,
  address: null
)
```

