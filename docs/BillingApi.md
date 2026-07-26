# Zippendo::BillingApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_billing_usage**](BillingApi.md#get_billing_usage) | **GET** /orgs/{orgId}/billing/usage | Get usage |


## get_billing_usage

> <GetBillingUsage200Response> get_billing_usage(org_id)

Get usage

Get detailed usage statistics for the current billing period.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BillingApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID

begin
  # Get usage
  result = api_instance.get_billing_usage(org_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BillingApi->get_billing_usage: #{e}"
end
```

#### Using the get_billing_usage_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetBillingUsage200Response>, Integer, Hash)> get_billing_usage_with_http_info(org_id)

```ruby
begin
  # Get usage
  data, status_code, headers = api_instance.get_billing_usage_with_http_info(org_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetBillingUsage200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling BillingApi->get_billing_usage_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |

### Return type

[**GetBillingUsage200Response**](GetBillingUsage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

