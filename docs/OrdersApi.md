# Zippendo::OrdersApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_order**](OrdersApi.md#create_order) | **POST** /orgs/{orgId}/orders | Create order |
| [**delete_order**](OrdersApi.md#delete_order) | **DELETE** /orgs/{orgId}/orders/{orderId} | Delete order |
| [**get_order**](OrdersApi.md#get_order) | **GET** /orgs/{orgId}/orders/{orderId} | Get order |
| [**list_orders**](OrdersApi.md#list_orders) | **GET** /orgs/{orgId}/orders | List orders |
| [**update_order**](OrdersApi.md#update_order) | **PATCH** /orgs/{orgId}/orders/{orderId} | Update order |


## create_order

> <CreateOrder201Response> create_order(org_id, create_order_request)

Create order

Creates a new order under an existing order channel for the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrdersApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
create_order_request = Zippendo::CreateOrderRequest.new({order_number: '#1042', order_channel_id: 'clz9k2f0a0001abcd1234efgh', order_lines: [Zippendo::CreateOrderRequestOrderLinesInner.new({name: 'Wool Sweater', quantity: 2})]}) # CreateOrderRequest | 

begin
  # Create order
  result = api_instance.create_order(org_id, create_order_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->create_order: #{e}"
end
```

#### Using the create_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateOrder201Response>, Integer, Hash)> create_order_with_http_info(org_id, create_order_request)

```ruby
begin
  # Create order
  data, status_code, headers = api_instance.create_order_with_http_info(org_id, create_order_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateOrder201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->create_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_order_request** | [**CreateOrderRequest**](CreateOrderRequest.md) |  |  |

### Return type

[**CreateOrder201Response**](CreateOrder201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_order

> <RevokeApiToken200Response> delete_order(org_id, order_id)

Delete order

Deletes an order. Fails if the order has associated shipments.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrdersApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
order_id = 'clz9k2f0a0003abcd9012mnop' # String | Order ID.

begin
  # Delete order
  result = api_instance.delete_order(org_id, order_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->delete_order: #{e}"
end
```

#### Using the delete_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RevokeApiToken200Response>, Integer, Hash)> delete_order_with_http_info(org_id, order_id)

```ruby
begin
  # Delete order
  data, status_code, headers = api_instance.delete_order_with_http_info(org_id, order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RevokeApiToken200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->delete_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **order_id** | **String** | Order ID. |  |

### Return type

[**RevokeApiToken200Response**](RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_order

> <GetOrder200Response> get_order(org_id, order_id)

Get order

Returns a single order with its channel, shipping rule, shipments, and documents.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrdersApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
order_id = 'clz9k2f0a0003abcd9012mnop' # String | Order ID.

begin
  # Get order
  result = api_instance.get_order(org_id, order_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->get_order: #{e}"
end
```

#### Using the get_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrder200Response>, Integer, Hash)> get_order_with_http_info(org_id, order_id)

```ruby
begin
  # Get order
  data, status_code, headers = api_instance.get_order_with_http_info(org_id, order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrder200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->get_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **order_id** | **String** | Order ID. |  |

### Return type

[**GetOrder200Response**](GetOrder200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_orders

> <ListOrders200Response> list_orders(org_id, opts)

List orders

Returns a paginated list of orders for an organization, filterable by status, channel, and search term.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrdersApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20, # Integer | Items per page (max 100)
  brand_id: 'brnd_8f3kd92ld0', # String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
  status: 'pending', # String | Order fulfilment status derived from its shipments.
  order_channel_id: 'clz9k2f0a0001abcd1234efgh', # String | Filter by order channel ID.
  search: 'Anna' # String | Search by order number or customer name/email.
}

begin
  # List orders
  result = api_instance.list_orders(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->list_orders: #{e}"
end
```

#### Using the list_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrders200Response>, Integer, Hash)> list_orders_with_http_info(org_id, opts)

```ruby
begin
  # List orders
  data, status_code, headers = api_instance.list_orders_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrders200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->list_orders_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |
| **brand_id** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **status** | **String** | Order fulfilment status derived from its shipments. | [optional] |
| **order_channel_id** | **String** | Filter by order channel ID. | [optional] |
| **search** | **String** | Search by order number or customer name/email. | [optional] |

### Return type

[**ListOrders200Response**](ListOrders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_order

> <CreateOrder201Response> update_order(org_id, order_id, update_order_request)

Update order

Updates an order that is not yet fulfilled or cancelled.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrdersApi.new
org_id = 'clz9k2f0a0000abcd0000zzzz' # String | Organization ID.
order_id = 'clz9k2f0a0003abcd9012mnop' # String | Order ID.
update_order_request = Zippendo::UpdateOrderRequest.new # UpdateOrderRequest | 

begin
  # Update order
  result = api_instance.update_order(org_id, order_id, update_order_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->update_order: #{e}"
end
```

#### Using the update_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateOrder201Response>, Integer, Hash)> update_order_with_http_info(org_id, order_id, update_order_request)

```ruby
begin
  # Update order
  data, status_code, headers = api_instance.update_order_with_http_info(org_id, order_id, update_order_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateOrder201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrdersApi->update_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID. |  |
| **order_id** | **String** | Order ID. |  |
| **update_order_request** | [**UpdateOrderRequest**](UpdateOrderRequest.md) |  |  |

### Return type

[**CreateOrder201Response**](CreateOrder201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

