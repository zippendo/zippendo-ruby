# Zippendo::CarriersApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**connect_carrier**](CarriersApi.md#connect_carrier) | **POST** /orgs/{orgId}/carriers | Connect carrier |
| [**disconnect_carrier**](CarriersApi.md#disconnect_carrier) | **DELETE** /orgs/{orgId}/carriers/{carrierId} | Disconnect carrier |
| [**get_carrier**](CarriersApi.md#get_carrier) | **GET** /orgs/{orgId}/carriers/{carrierId} | Get carrier |
| [**list_carrier_product_service_points**](CarriersApi.md#list_carrier_product_service_points) | **POST** /orgs/{orgId}/carriers/{carrierId}/products/{productId}/service-points | List product service points |
| [**list_carrier_products**](CarriersApi.md#list_carrier_products) | **GET** /orgs/{orgId}/carriers/{carrierId}/products | List carrier products |
| [**list_carriers**](CarriersApi.md#list_carriers) | **GET** /orgs/{orgId}/carriers | List carriers |
| [**update_carrier**](CarriersApi.md#update_carrier) | **PUT** /orgs/{orgId}/carriers/{carrierId} | Update carrier |


## connect_carrier

> <ListCarriers200ResponseDataInner> connect_carrier(org_id, connect_carrier_request)

Connect carrier

Connects a new carrier to the organization with its configuration.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
connect_carrier_request = Zippendo::ConnectCarrierRequest.new({name: 'PostNord', carrier_slug: 'postnord', config: { key: Zippendo::ListCarriers200ResponseDataInnerConfigValue.new}}) # ConnectCarrierRequest | 

begin
  # Connect carrier
  result = api_instance.connect_carrier(org_id, connect_carrier_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->connect_carrier: #{e}"
end
```

#### Using the connect_carrier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCarriers200ResponseDataInner>, Integer, Hash)> connect_carrier_with_http_info(org_id, connect_carrier_request)

```ruby
begin
  # Connect carrier
  data, status_code, headers = api_instance.connect_carrier_with_http_info(org_id, connect_carrier_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCarriers200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->connect_carrier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **connect_carrier_request** | [**ConnectCarrierRequest**](ConnectCarrierRequest.md) |  |  |

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## disconnect_carrier

> String disconnect_carrier(org_id, carrier_id)

Disconnect carrier

Disconnects a carrier from the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
carrier_id = 'carr_01HZX9K2QF' # String | Carrier ID

begin
  # Disconnect carrier
  result = api_instance.disconnect_carrier(org_id, carrier_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->disconnect_carrier: #{e}"
end
```

#### Using the disconnect_carrier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(String, Integer, Hash)> disconnect_carrier_with_http_info(org_id, carrier_id)

```ruby
begin
  # Disconnect carrier
  data, status_code, headers = api_instance.disconnect_carrier_with_http_info(org_id, carrier_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => String
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->disconnect_carrier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **carrier_id** | **String** | Carrier ID |  |

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_carrier

> <ListCarriers200ResponseDataInner> get_carrier(org_id, carrier_id)

Get carrier

Returns a single connected carrier.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
carrier_id = 'carr_01HZX9K2QF' # String | Carrier ID

begin
  # Get carrier
  result = api_instance.get_carrier(org_id, carrier_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->get_carrier: #{e}"
end
```

#### Using the get_carrier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCarriers200ResponseDataInner>, Integer, Hash)> get_carrier_with_http_info(org_id, carrier_id)

```ruby
begin
  # Get carrier
  data, status_code, headers = api_instance.get_carrier_with_http_info(org_id, carrier_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCarriers200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->get_carrier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **carrier_id** | **String** | Carrier ID |  |

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_carrier_product_service_points

> <Array<ListCarrierProductServicePoints200ResponseInner>> list_carrier_product_service_points(org_id, carrier_id, product_id, list_carrier_product_service_points_request)

List product service points

Returns pickup service points near a location for a specific carrier product.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
carrier_id = 'carr_01HZX9K2QF' # String | Carrier ID
product_id = 'PNL13' # String | Carrier product ID
list_carrier_product_service_points_request = Zippendo::ListCarrierProductServicePointsRequest.new({address1: 'Vesterbrogade 1', postal_code: '1620', city: 'København', country_code: 'DK'}) # ListCarrierProductServicePointsRequest | 

begin
  # List product service points
  result = api_instance.list_carrier_product_service_points(org_id, carrier_id, product_id, list_carrier_product_service_points_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->list_carrier_product_service_points: #{e}"
end
```

#### Using the list_carrier_product_service_points_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ListCarrierProductServicePoints200ResponseInner>>, Integer, Hash)> list_carrier_product_service_points_with_http_info(org_id, carrier_id, product_id, list_carrier_product_service_points_request)

```ruby
begin
  # List product service points
  data, status_code, headers = api_instance.list_carrier_product_service_points_with_http_info(org_id, carrier_id, product_id, list_carrier_product_service_points_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ListCarrierProductServicePoints200ResponseInner>>
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->list_carrier_product_service_points_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **carrier_id** | **String** | Carrier ID |  |
| **product_id** | **String** | Carrier product ID |  |
| **list_carrier_product_service_points_request** | [**ListCarrierProductServicePointsRequest**](ListCarrierProductServicePointsRequest.md) |  |  |

### Return type

[**Array&lt;ListCarrierProductServicePoints200ResponseInner&gt;**](ListCarrierProductServicePoints200ResponseInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_carrier_products

> <Array<ListCarrierProducts200ResponseInner>> list_carrier_products(org_id, carrier_id)

List carrier products

Returns the shipping products available for a connected carrier.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
carrier_id = 'carr_01HZX9K2QF' # String | Carrier ID

begin
  # List carrier products
  result = api_instance.list_carrier_products(org_id, carrier_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->list_carrier_products: #{e}"
end
```

#### Using the list_carrier_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ListCarrierProducts200ResponseInner>>, Integer, Hash)> list_carrier_products_with_http_info(org_id, carrier_id)

```ruby
begin
  # List carrier products
  data, status_code, headers = api_instance.list_carrier_products_with_http_info(org_id, carrier_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ListCarrierProducts200ResponseInner>>
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->list_carrier_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **carrier_id** | **String** | Carrier ID |  |

### Return type

[**Array&lt;ListCarrierProducts200ResponseInner&gt;**](ListCarrierProducts200ResponseInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_carriers

> <ListCarriers200Response> list_carriers(org_id, opts)

List carriers

Returns a paginated list of carriers connected to the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20 # Integer | Items per page (max 100)
}

begin
  # List carriers
  result = api_instance.list_carriers(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->list_carriers: #{e}"
end
```

#### Using the list_carriers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCarriers200Response>, Integer, Hash)> list_carriers_with_http_info(org_id, opts)

```ruby
begin
  # List carriers
  data, status_code, headers = api_instance.list_carriers_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCarriers200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->list_carriers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |

### Return type

[**ListCarriers200Response**](ListCarriers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_carrier

> <ListCarriers200ResponseDataInner> update_carrier(org_id, carrier_id, update_carrier_request)

Update carrier

Updates a connected carrier's configuration or name.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarriersApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
carrier_id = 'carr_01HZX9K2QF' # String | Carrier ID
update_carrier_request = Zippendo::UpdateCarrierRequest.new # UpdateCarrierRequest | 

begin
  # Update carrier
  result = api_instance.update_carrier(org_id, carrier_id, update_carrier_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->update_carrier: #{e}"
end
```

#### Using the update_carrier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCarriers200ResponseDataInner>, Integer, Hash)> update_carrier_with_http_info(org_id, carrier_id, update_carrier_request)

```ruby
begin
  # Update carrier
  data, status_code, headers = api_instance.update_carrier_with_http_info(org_id, carrier_id, update_carrier_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCarriers200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling CarriersApi->update_carrier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **carrier_id** | **String** | Carrier ID |  |
| **update_carrier_request** | [**UpdateCarrierRequest**](UpdateCarrierRequest.md) |  |  |

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

