# Zippendo::ListCarriers200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;ListCarriers200ResponseDataInner&gt;**](ListCarriers200ResponseDataInner.md) | Page of results |  |
| **total** | **Float** | Total matching items across all pages |  |
| **page** | **Float** | Current page number (1-based) |  |
| **limit** | **Float** | Items per page |  |
| **total_pages** | **Float** | Total number of pages |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarriers200Response.new(
  data: null,
  total: 137,
  page: 1,
  limit: 20,
  total_pages: 7
)
```

