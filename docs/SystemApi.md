# Zippendo::SystemApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**health_check**](SystemApi.md#health_check) | **GET** /health | Health check |


## health_check

> <HealthCheck200Response> health_check

Health check

Return the service health status, current timestamp, and version.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::SystemApi.new

begin
  # Health check
  result = api_instance.health_check
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling SystemApi->health_check: #{e}"
end
```

#### Using the health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<HealthCheck200Response>, Integer, Hash)> health_check_with_http_info

```ruby
begin
  # Health check
  data, status_code, headers = api_instance.health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <HealthCheck200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling SystemApi->health_check_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**HealthCheck200Response**](HealthCheck200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

