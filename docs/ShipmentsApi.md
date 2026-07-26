# Zippendo::ShipmentsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**batch_send_shipments**](ShipmentsApi.md#batch_send_shipments) | **POST** /orgs/{orgId}/shipments/batch-send | Batch send shipments |
| [**batch_split_shipment**](ShipmentsApi.md#batch_split_shipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/batch-split-shipment | Batch split shipment |
| [**create_return_shipment**](ShipmentsApi.md#create_return_shipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/create-return | Create return shipment |
| [**create_shipment**](ShipmentsApi.md#create_shipment) | **POST** /orgs/{orgId}/shipments | Create shipment |
| [**delete_shipment**](ShipmentsApi.md#delete_shipment) | **DELETE** /orgs/{orgId}/shipments/{shipmentId} | Delete shipment |
| [**get_shipment**](ShipmentsApi.md#get_shipment) | **GET** /orgs/{orgId}/shipments/{shipmentId} | Get shipment |
| [**get_shipment_document_content**](ShipmentsApi.md#get_shipment_document_content) | **GET** /orgs/{orgId}/shipments/{shipmentId}/documents/{documentId}/content | Download shipment document |
| [**list_shipments**](ShipmentsApi.md#list_shipments) | **GET** /orgs/{orgId}/shipments | List shipments |
| [**send_shipment**](ShipmentsApi.md#send_shipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/send | Send shipment |
| [**split_shipment**](ShipmentsApi.md#split_shipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-shipment | Split shipment |
| [**split_shipment_parcel**](ShipmentsApi.md#split_shipment_parcel) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-parcel | Split parcels |
| [**track_shipment**](ShipmentsApi.md#track_shipment) | **GET** /orgs/{orgId}/shipments/{shipmentId}/tracking | Get shipment tracking |
| [**update_shipment**](ShipmentsApi.md#update_shipment) | **PATCH** /orgs/{orgId}/shipments/{shipmentId} | Update shipment |


## batch_send_shipments

> <BatchSendShipments200Response> batch_send_shipments(org_id, batch_send_shipments_request)

Batch send shipments

Book multiple pending/error shipments with their carriers in one request. Each shipment is processed independently and reported in `results`; a failure on one shipment never aborts the others. Use it to send every shipment on an order at once.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
batch_send_shipments_request = Zippendo::BatchSendShipmentsRequest.new({shipment_ids: ["shp_01H8XABC123", "shp_01H8XDEF456"]}) # BatchSendShipmentsRequest | 

begin
  # Batch send shipments
  result = api_instance.batch_send_shipments(org_id, batch_send_shipments_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->batch_send_shipments: #{e}"
end
```

#### Using the batch_send_shipments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchSendShipments200Response>, Integer, Hash)> batch_send_shipments_with_http_info(org_id, batch_send_shipments_request)

```ruby
begin
  # Batch send shipments
  data, status_code, headers = api_instance.batch_send_shipments_with_http_info(org_id, batch_send_shipments_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchSendShipments200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->batch_send_shipments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **batch_send_shipments_request** | [**BatchSendShipmentsRequest**](BatchSendShipmentsRequest.md) |  |  |

### Return type

[**BatchSendShipments200Response**](BatchSendShipments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## batch_split_shipment

> <BatchSplitShipment201Response> batch_split_shipment(org_id, shipment_id, batch_split_shipment_request)

Batch split shipment

Split a parcel into multiple new shipments with per-line quantities in a single atomic operation. Only draft or pending shipments can be split.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.
batch_split_shipment_request = Zippendo::BatchSplitShipmentRequest.new({parcel_id: 'prc_5a6b7c8d', shipments: [Zippendo::BatchSplitShipmentRequestShipmentsInner.new({order_lines: [Zippendo::BatchSplitShipmentRequestShipmentsInnerOrderLinesInner.new({id: 'ol_9c1d2e3f', quantity: 1})]})]}) # BatchSplitShipmentRequest | 

begin
  # Batch split shipment
  result = api_instance.batch_split_shipment(org_id, shipment_id, batch_split_shipment_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->batch_split_shipment: #{e}"
end
```

#### Using the batch_split_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchSplitShipment201Response>, Integer, Hash)> batch_split_shipment_with_http_info(org_id, shipment_id, batch_split_shipment_request)

```ruby
begin
  # Batch split shipment
  data, status_code, headers = api_instance.batch_split_shipment_with_http_info(org_id, shipment_id, batch_split_shipment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchSplitShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->batch_split_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |
| **batch_split_shipment_request** | [**BatchSplitShipmentRequest**](BatchSplitShipmentRequest.md) |  |  |

### Return type

[**BatchSplitShipment201Response**](BatchSplitShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_return_shipment

> <CreateShipment201Response> create_return_shipment(org_id, shipment_id)

Create return shipment

Create and auto-send a return shipment from a dispatched outbound shipment with swapped sender/receiver. Requires a configured return shipping rule.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.

begin
  # Create return shipment
  result = api_instance.create_return_shipment(org_id, shipment_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->create_return_shipment: #{e}"
end
```

#### Using the create_return_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShipment201Response>, Integer, Hash)> create_return_shipment_with_http_info(org_id, shipment_id)

```ruby
begin
  # Create return shipment
  data, status_code, headers = api_instance.create_return_shipment_with_http_info(org_id, shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->create_return_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_shipment

> <CreateShipment201Response> create_shipment(org_id, create_shipment_request)

Create shipment

Create a new shipment for an organization. When orderId is provided, parties and parcels are derived from the order.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
create_shipment_request = Zippendo::CreateShipmentRequest.new({type: 'outbound', carrier_settings: Zippendo::CreateShipmentRequestCarrierSettings.new({carrier_id: 'car_pn_001', product_id: 'prod_mypack_home', services: ["A7"], additional_parameters: { key: Zippendo::CreateShippingRuleRequestAdditionalParametersAnyOfValue.new({id: 'sp_pn_4521', name: 'Føtex Nørrebro', address: 'Nørrebrogade 20, 2200 København N'})}})}) # CreateShipmentRequest | 

begin
  # Create shipment
  result = api_instance.create_shipment(org_id, create_shipment_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->create_shipment: #{e}"
end
```

#### Using the create_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShipment201Response>, Integer, Hash)> create_shipment_with_http_info(org_id, create_shipment_request)

```ruby
begin
  # Create shipment
  data, status_code, headers = api_instance.create_shipment_with_http_info(org_id, create_shipment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->create_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_shipment_request** | [**CreateShipmentRequest**](CreateShipmentRequest.md) |  |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_shipment

> <RevokeApiToken200Response> delete_shipment(org_id, shipment_id)

Delete shipment

Delete a shipment. Only shipments in pending status can be deleted.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.

begin
  # Delete shipment
  result = api_instance.delete_shipment(org_id, shipment_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->delete_shipment: #{e}"
end
```

#### Using the delete_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RevokeApiToken200Response>, Integer, Hash)> delete_shipment_with_http_info(org_id, shipment_id)

```ruby
begin
  # Delete shipment
  data, status_code, headers = api_instance.delete_shipment_with_http_info(org_id, shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RevokeApiToken200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->delete_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |

### Return type

[**RevokeApiToken200Response**](RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shipment

> <CreateShipment201Response> get_shipment(org_id, shipment_id)

Get shipment

Retrieve a single shipment by its ID, including parcels, parties, documents and activity.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.

begin
  # Get shipment
  result = api_instance.get_shipment(org_id, shipment_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->get_shipment: #{e}"
end
```

#### Using the get_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShipment201Response>, Integer, Hash)> get_shipment_with_http_info(org_id, shipment_id)

```ruby
begin
  # Get shipment
  data, status_code, headers = api_instance.get_shipment_with_http_info(org_id, shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->get_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shipment_document_content

> get_shipment_document_content(org_id, shipment_id, document_id, opts)

Download shipment document

Streams a shipment document or label file from storage.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.
document_id = 'doc_8f3a2b1c' # String | Document identifier.
opts = {
  disposition: 'inline', # String | Render the document inline (default) or force a download.
  filename: 'label' # String | Suggested filename (without extension) for attachment downloads.
}

begin
  # Download shipment document
  api_instance.get_shipment_document_content(org_id, shipment_id, document_id, opts)
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->get_shipment_document_content: #{e}"
end
```

#### Using the get_shipment_document_content_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_shipment_document_content_with_http_info(org_id, shipment_id, document_id, opts)

```ruby
begin
  # Download shipment document
  data, status_code, headers = api_instance.get_shipment_document_content_with_http_info(org_id, shipment_id, document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->get_shipment_document_content_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |
| **document_id** | **String** | Document identifier. |  |
| **disposition** | **String** | Render the document inline (default) or force a download. | [optional][default to &#39;inline&#39;] |
| **filename** | **String** | Suggested filename (without extension) for attachment downloads. | [optional] |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_shipments

> <ListShipments200Response> list_shipments(org_id, opts)

List shipments

List all shipments for an organization, paginated and ordered by newest first.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20 # Integer | Items per page (max 100)
}

begin
  # List shipments
  result = api_instance.list_shipments(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->list_shipments: #{e}"
end
```

#### Using the list_shipments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListShipments200Response>, Integer, Hash)> list_shipments_with_http_info(org_id, opts)

```ruby
begin
  # List shipments
  data, status_code, headers = api_instance.list_shipments_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListShipments200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->list_shipments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |

### Return type

[**ListShipments200Response**](ListShipments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_shipment

> <CreateShipment201Response> send_shipment(org_id, shipment_id)

Send shipment

Book a pending or error shipment with the carrier, generating labels and tracking. Returns 422 with carrier errors if booking fails.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.

begin
  # Send shipment
  result = api_instance.send_shipment(org_id, shipment_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->send_shipment: #{e}"
end
```

#### Using the send_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShipment201Response>, Integer, Hash)> send_shipment_with_http_info(org_id, shipment_id)

```ruby
begin
  # Send shipment
  data, status_code, headers = api_instance.send_shipment_with_http_info(org_id, shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->send_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## split_shipment

> <SplitShipment201Response> split_shipment(org_id, shipment_id, split_shipment_request)

Split shipment

Move order lines from a parcel into a new shipment. Only draft or pending shipments can be split.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.
split_shipment_request = Zippendo::SplitShipmentRequest.new({parcel_id: 'prc_5a6b7c8d'}) # SplitShipmentRequest | 

begin
  # Split shipment
  result = api_instance.split_shipment(org_id, shipment_id, split_shipment_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->split_shipment: #{e}"
end
```

#### Using the split_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SplitShipment201Response>, Integer, Hash)> split_shipment_with_http_info(org_id, shipment_id, split_shipment_request)

```ruby
begin
  # Split shipment
  data, status_code, headers = api_instance.split_shipment_with_http_info(org_id, shipment_id, split_shipment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SplitShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->split_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |
| **split_shipment_request** | [**SplitShipmentRequest**](SplitShipmentRequest.md) |  |  |

### Return type

[**SplitShipment201Response**](SplitShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## split_shipment_parcel

> <SplitShipmentParcel200Response> split_shipment_parcel(org_id, shipment_id, split_shipment_parcel_request)

Split parcels

Redistribute order lines across parcels within a shipment, moving lines between parcels and creating new ones. Only draft, pending or error shipments can be modified.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.
split_shipment_parcel_request = Zippendo::SplitShipmentParcelRequest.new({parcels: [Zippendo::SplitShipmentParcelRequestParcelsInner.new({order_lines: [Zippendo::BatchSplitShipmentRequestShipmentsInnerOrderLinesInner.new({id: 'ol_9c1d2e3f', quantity: 1})]})]}) # SplitShipmentParcelRequest | 

begin
  # Split parcels
  result = api_instance.split_shipment_parcel(org_id, shipment_id, split_shipment_parcel_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->split_shipment_parcel: #{e}"
end
```

#### Using the split_shipment_parcel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SplitShipmentParcel200Response>, Integer, Hash)> split_shipment_parcel_with_http_info(org_id, shipment_id, split_shipment_parcel_request)

```ruby
begin
  # Split parcels
  data, status_code, headers = api_instance.split_shipment_parcel_with_http_info(org_id, shipment_id, split_shipment_parcel_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SplitShipmentParcel200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->split_shipment_parcel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |
| **split_shipment_parcel_request** | [**SplitShipmentParcelRequest**](SplitShipmentParcelRequest.md) |  |  |

### Return type

[**SplitShipmentParcel200Response**](SplitShipmentParcel200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## track_shipment

> <TrackShipment200Response> track_shipment(org_id, shipment_id)

Get shipment tracking

Retrieve the tracking timeline for a shipment, including current status and all carrier events.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.

begin
  # Get shipment tracking
  result = api_instance.track_shipment(org_id, shipment_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->track_shipment: #{e}"
end
```

#### Using the track_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrackShipment200Response>, Integer, Hash)> track_shipment_with_http_info(org_id, shipment_id)

```ruby
begin
  # Get shipment tracking
  data, status_code, headers = api_instance.track_shipment_with_http_info(org_id, shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrackShipment200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->track_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |

### Return type

[**TrackShipment200Response**](TrackShipment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_shipment

> <CreateShipment201Response> update_shipment(org_id, shipment_id, update_shipment_request)

Update shipment

Update an existing shipment. Only draft, pending or error shipments can be updated; an applied shipping rule overrides carrier settings and sender party.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::ShipmentsApi.new
org_id = 'org_1a2b3c4d' # String | Organization identifier.
shipment_id = 'shp_4d9e7a2f' # String | Shipment identifier.
update_shipment_request = Zippendo::UpdateShipmentRequest.new # UpdateShipmentRequest | 

begin
  # Update shipment
  result = api_instance.update_shipment(org_id, shipment_id, update_shipment_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->update_shipment: #{e}"
end
```

#### Using the update_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShipment201Response>, Integer, Hash)> update_shipment_with_http_info(org_id, shipment_id, update_shipment_request)

```ruby
begin
  # Update shipment
  data, status_code, headers = api_instance.update_shipment_with_http_info(org_id, shipment_id, update_shipment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShipment201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling ShipmentsApi->update_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization identifier. |  |
| **shipment_id** | **String** | Shipment identifier. |  |
| **update_shipment_request** | [**UpdateShipmentRequest**](UpdateShipmentRequest.md) |  |  |

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

