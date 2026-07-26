# Zippendo::CarrierCatalogApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_available_carriers**](CarrierCatalogApi.md#list_available_carriers) | **GET** /orgs/{orgId}/available-carriers | List available carriers |


## list_available_carriers

> <Array<ListAvailableCarriers200ResponseInner>> list_available_carriers(org_id)

List available carriers

Returns the carriers available to connect, as supported by the carrier server.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::CarrierCatalogApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID

begin
  # List available carriers
  result = api_instance.list_available_carriers(org_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling CarrierCatalogApi->list_available_carriers: #{e}"
end
```

#### Using the list_available_carriers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ListAvailableCarriers200ResponseInner>>, Integer, Hash)> list_available_carriers_with_http_info(org_id)

```ruby
begin
  # List available carriers
  data, status_code, headers = api_instance.list_available_carriers_with_http_info(org_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ListAvailableCarriers200ResponseInner>>
rescue Zippendo::ApiError => e
  puts "Error when calling CarrierCatalogApi->list_available_carriers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |

### Return type

[**Array&lt;ListAvailableCarriers200ResponseInner&gt;**](ListAvailableCarriers200ResponseInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

