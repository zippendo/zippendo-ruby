# Zippendo::ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **un_number** | **String** | Key of the additional parameter that takes the four-digit UN number. | [optional] |
| **hazard_class** | **String** | Key of the additional parameter that takes the ADR hazard class. | [optional] |
| **packing_group** | **String** | Key of the additional parameter that takes the packing group (I, II or III). | [optional] |
| **proper_shipping_name** | **String** | Key of the additional parameter that takes the proper shipping name. | [optional] |
| **weight_grams_per_parcel** | **String** | Key of the additional parameter that takes the weight of the dangerous goods in the heaviest parcel, in grams. | [optional] |
| **weight_kg** | **String** | Key of the additional parameter that takes the total weight of the dangerous goods, in kg. | [optional] |
| **weight_kg_per_parcel** | **String** | Key of the additional parameter that takes the weight of the dangerous goods in the heaviest parcel, in kg. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters.new(
  un_number: lqUnNumber,
  hazard_class: lqClass,
  packing_group: lqPackagingGroup,
  proper_shipping_name: adrDescription,
  weight_grams_per_parcel: lqSubWeight,
  weight_kg: adrWeight,
  weight_kg_per_parcel: dangerousGoodsLqWeight
)
```

