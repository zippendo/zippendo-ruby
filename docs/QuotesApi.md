# Zippendo::QuotesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_shipping_quote**](QuotesApi.md#create_shipping_quote) | **POST** /orgs/{orgId}/shipping-quote | Calculate shipping rates |


## create_shipping_quote

> <CreateShippingQuote200Response> create_shipping_quote(org_id, create_shipping_quote_request)

Calculate shipping rates

Calculates shipping rates from configured shipping rules based on cart items and destination.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::QuotesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
create_shipping_quote_request = Zippendo::CreateShippingQuoteRequest.new({destination: Zippendo::CreateShippingQuoteRequestDestination.new({country: 'DK'}), items: [{"name": "Uld trøje", "quantity": 2, "grams": 500, "price": 29900}], currency: 'DKK'}) # CreateShippingQuoteRequest | 

begin
  # Calculate shipping rates
  result = api_instance.create_shipping_quote(org_id, create_shipping_quote_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling QuotesApi->create_shipping_quote: #{e}"
end
```

#### Using the create_shipping_quote_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShippingQuote200Response>, Integer, Hash)> create_shipping_quote_with_http_info(org_id, create_shipping_quote_request)

```ruby
begin
  # Calculate shipping rates
  data, status_code, headers = api_instance.create_shipping_quote_with_http_info(org_id, create_shipping_quote_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShippingQuote200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling QuotesApi->create_shipping_quote_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_shipping_quote_request** | [**CreateShippingQuoteRequest**](CreateShippingQuoteRequest.md) |  |  |

### Return type

[**CreateShippingQuote200Response**](CreateShippingQuote200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

