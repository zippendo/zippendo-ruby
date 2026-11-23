# Zippendo::ListCarrierProducts200ResponseInnerDangerousGoodsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **kind** | **String** | &#x60;limited_quantity&#x60;: dangerous goods packed in limited quantities (LQ). &#x60;regulated&#x60;: fully regulated dangerous goods (ADR). |  |
| **service_id** | **String** | The service that declares these dangerous goods to the carrier. |  |
| **parameters** | [**ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters**](ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters.md) |  |  |
| **owned_parameters** | **Array&lt;String&gt;** | Every additional parameter that describes the declared goods, including those &#x60;parameters&#x60; does not fill. A declaration replaces them all, so a value saved for other goods is never sent. | [optional] |
| **single_parcel** | **Boolean** | The carrier takes this declaration on a shipment of one parcel only. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProducts200ResponseInnerDangerousGoodsInner.new(
  kind: limited_quantity,
  service_id: LQ,
  parameters: null,
  owned_parameters: [&quot;lqUnNumber&quot;,&quot;lqPackagingGroup&quot;,&quot;lqClass&quot;,&quot;lqCode&quot;,&quot;lqSubWeight&quot;],
  single_parcel: true
)
```

