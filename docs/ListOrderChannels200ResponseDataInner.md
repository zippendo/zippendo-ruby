# Zippendo::ListOrderChannels200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique order channel ID. |  |
| **name** | **String** | Display name of the channel. |  |
| **type** | **String** | Type of the order channel (sales platform). |  |
| **enabled** | **Boolean** | Whether the channel is active. |  |
| **brand_id** | **String** | Brand this channel belongs to, or null for organization-wide. Orders synced from this channel inherit it, and so do the shipments and documents made from them. |  |
| **has_credentials** | **Boolean** | Whether credentials are configured (values are never exposed). |  |
| **settings** | [**ListOrderChannels200ResponseDataInnerSettings**](ListOrderChannels200ResponseDataInnerSettings.md) |  |  |
| **webhooks_enabled** | **Boolean** | Whether real-time webhooks are enabled. | [optional] |
| **last_sync_at** | **Time** | Timestamp of the last successful sync. | [optional] |
| **last_sync_error** | **String** | Error message from the last failed sync. | [optional] |
| **shipping_rule_ids** | **Array&lt;String&gt;** | IDs of shipping rules linked to this channel. | [optional] |
| **org_id** | **String** | Owning organization ID. |  |
| **created_at** | **String** | Creation timestamp (ISO 8601). |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601). |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrderChannels200ResponseDataInner.new(
  id: clz9k2f0a0001abcd1234efgh,
  name: Anna&#39;s Shopify Store,
  type: shopify,
  enabled: true,
  brand_id: brnd_8f3kd92ld0,
  has_credentials: true,
  settings: null,
  webhooks_enabled: true,
  last_sync_at: 2026-06-22T14:30Z,
  last_sync_error: Invalid API credentials,
  shipping_rule_ids: [&quot;clz9k2f0a0002abcd5678ijkl&quot;],
  org_id: clz9k2f0a0000abcd0000zzzz,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z
)
```

