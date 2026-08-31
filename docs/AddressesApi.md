# Zippendo::AddressesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_address**](AddressesApi.md#create_address) | **POST** /orgs/{orgId}/addresses | Create address |
| [**delete_address**](AddressesApi.md#delete_address) | **DELETE** /orgs/{orgId}/addresses/{addressId} | Delete address |
| [**get_address**](AddressesApi.md#get_address) | **GET** /orgs/{orgId}/addresses/{addressId} | Get address |
| [**list_addresses**](AddressesApi.md#list_addresses) | **GET** /orgs/{orgId}/addresses | List addresses |
| [**update_address**](AddressesApi.md#update_address) | **PUT** /orgs/{orgId}/addresses/{addressId} | Update address |


## create_address

> <ListAddresses200ResponseDataInner> create_address(org_id, create_address_request)

Create address

Creates a new sender, pickup or return address for the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::AddressesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
create_address_request = Zippendo::CreateAddressRequest.new({name: 'Hovedlager', att_contact: 'Mette Hansen', address1: 'Vesterbrogade 1', zipcode: '1620', city: 'København', phone: '+4533123456', country_code: 'DK', email: 'lager@example.dk'}) # CreateAddressRequest | 

begin
  # Create address
  result = api_instance.create_address(org_id, create_address_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->create_address: #{e}"
end
```

#### Using the create_address_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAddresses200ResponseDataInner>, Integer, Hash)> create_address_with_http_info(org_id, create_address_request)

```ruby
begin
  # Create address
  data, status_code, headers = api_instance.create_address_with_http_info(org_id, create_address_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAddresses200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->create_address_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_address_request** | [**CreateAddressRequest**](CreateAddressRequest.md) |  |  |

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_address

> String delete_address(org_id, address_id)

Delete address

Deletes an address belonging to the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::AddressesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
address_id = 'addr_01HZX9K2QF' # String | Address ID

begin
  # Delete address
  result = api_instance.delete_address(org_id, address_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->delete_address: #{e}"
end
```

#### Using the delete_address_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(String, Integer, Hash)> delete_address_with_http_info(org_id, address_id)

```ruby
begin
  # Delete address
  data, status_code, headers = api_instance.delete_address_with_http_info(org_id, address_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => String
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->delete_address_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **address_id** | **String** | Address ID |  |

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_address

> <ListAddresses200ResponseDataInner> get_address(org_id, address_id)

Get address

Returns a single address belonging to the organization, identified by its ID.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::AddressesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
address_id = 'addr_01HZX9K2QF' # String | Address ID

begin
  # Get address
  result = api_instance.get_address(org_id, address_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->get_address: #{e}"
end
```

#### Using the get_address_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAddresses200ResponseDataInner>, Integer, Hash)> get_address_with_http_info(org_id, address_id)

```ruby
begin
  # Get address
  data, status_code, headers = api_instance.get_address_with_http_info(org_id, address_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAddresses200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->get_address_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **address_id** | **String** | Address ID |  |

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_addresses

> <ListAddresses200Response> list_addresses(org_id, opts)

List addresses

Returns a paginated list of addresses for the organization, optionally filtered by type.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::AddressesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20, # Integer | Items per page (max 100)
  type: 'sender', # String | Filter by address type (sender, pickup, return)
  country_code: 'DK', # String | Filter by ISO 3166-1 alpha-2 country code.
  search: 'Copenhagen', # String | Search by address name, contact or city.
  brand_id: 'brnd_8f3kd92ld0', # String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
  brand_scope: 'own' # String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
}

begin
  # List addresses
  result = api_instance.list_addresses(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->list_addresses: #{e}"
end
```

#### Using the list_addresses_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAddresses200Response>, Integer, Hash)> list_addresses_with_http_info(org_id, opts)

```ruby
begin
  # List addresses
  data, status_code, headers = api_instance.list_addresses_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAddresses200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->list_addresses_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |
| **type** | **String** | Filter by address type (sender, pickup, return) | [optional] |
| **country_code** | **String** | Filter by ISO 3166-1 alpha-2 country code. | [optional] |
| **search** | **String** | Search by address name, contact or city. | [optional] |
| **brand_id** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brand_scope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] |

### Return type

[**ListAddresses200Response**](ListAddresses200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_address

> <ListAddresses200ResponseDataInner> update_address(org_id, address_id, update_address_request)

Update address

Updates an existing address belonging to the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::AddressesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
address_id = 'addr_01HZX9K2QF' # String | Address ID
update_address_request = Zippendo::UpdateAddressRequest.new # UpdateAddressRequest | 

begin
  # Update address
  result = api_instance.update_address(org_id, address_id, update_address_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->update_address: #{e}"
end
```

#### Using the update_address_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAddresses200ResponseDataInner>, Integer, Hash)> update_address_with_http_info(org_id, address_id, update_address_request)

```ruby
begin
  # Update address
  data, status_code, headers = api_instance.update_address_with_http_info(org_id, address_id, update_address_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAddresses200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling AddressesApi->update_address_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **address_id** | **String** | Address ID |  |
| **update_address_request** | [**UpdateAddressRequest**](UpdateAddressRequest.md) |  |  |

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

