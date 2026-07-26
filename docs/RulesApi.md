# Zippendo::RulesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_shipping_rule**](RulesApi.md#create_shipping_rule) | **POST** /orgs/{orgId}/shipping-rules | Create shipping rule |
| [**delete_shipping_rule**](RulesApi.md#delete_shipping_rule) | **DELETE** /orgs/{orgId}/shipping-rules/{ruleId} | Delete shipping rule |
| [**get_shipping_rule**](RulesApi.md#get_shipping_rule) | **GET** /orgs/{orgId}/shipping-rules/{ruleId} | Get shipping rule |
| [**list_shipping_rules**](RulesApi.md#list_shipping_rules) | **GET** /orgs/{orgId}/shipping-rules | List shipping rules |
| [**update_shipping_rule**](RulesApi.md#update_shipping_rule) | **PATCH** /orgs/{orgId}/shipping-rules/{ruleId} | Update shipping rule |


## create_shipping_rule

> <CreateShippingRule201Response> create_shipping_rule(org_id, create_shipping_rule_request)

Create shipping rule

Creates a new shipping rule with conditions and carrier product for the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::RulesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
create_shipping_rule_request = Zippendo::CreateShippingRuleRequest.new({name: 'Standard DK', carrier_id: 'carr_01HZX9K2QF', product_id: 'PNL13', services: ["EMAIL_NOTIFICATION"], address_id: 'addr_01HZX9K2QF', receiving_countries: ["DK", "SE"], conditions: [{"type": "flatRate", "shippingPrice": 39, "currency": "DKK"}]}) # CreateShippingRuleRequest | 

begin
  # Create shipping rule
  result = api_instance.create_shipping_rule(org_id, create_shipping_rule_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->create_shipping_rule: #{e}"
end
```

#### Using the create_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShippingRule201Response>, Integer, Hash)> create_shipping_rule_with_http_info(org_id, create_shipping_rule_request)

```ruby
begin
  # Create shipping rule
  data, status_code, headers = api_instance.create_shipping_rule_with_http_info(org_id, create_shipping_rule_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShippingRule201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->create_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_shipping_rule_request** | [**CreateShippingRuleRequest**](CreateShippingRuleRequest.md) |  |  |

### Return type

[**CreateShippingRule201Response**](CreateShippingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_shipping_rule

> <DeleteShippingRule200Response> delete_shipping_rule(org_id, rule_id)

Delete shipping rule

Deletes a shipping rule belonging to the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::RulesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
rule_id = 'rule_01HZX9K2QF' # String | Shipping Rule ID

begin
  # Delete shipping rule
  result = api_instance.delete_shipping_rule(org_id, rule_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->delete_shipping_rule: #{e}"
end
```

#### Using the delete_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteShippingRule200Response>, Integer, Hash)> delete_shipping_rule_with_http_info(org_id, rule_id)

```ruby
begin
  # Delete shipping rule
  data, status_code, headers = api_instance.delete_shipping_rule_with_http_info(org_id, rule_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteShippingRule200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->delete_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **rule_id** | **String** | Shipping Rule ID |  |

### Return type

[**DeleteShippingRule200Response**](DeleteShippingRule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shipping_rule

> <ListShippingRules200ResponseDataInner> get_shipping_rule(org_id, rule_id)

Get shipping rule

Returns a single shipping rule with its carrier, address and printer relations.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::RulesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
rule_id = 'rule_01HZX9K2QF' # String | Shipping Rule ID

begin
  # Get shipping rule
  result = api_instance.get_shipping_rule(org_id, rule_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->get_shipping_rule: #{e}"
end
```

#### Using the get_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListShippingRules200ResponseDataInner>, Integer, Hash)> get_shipping_rule_with_http_info(org_id, rule_id)

```ruby
begin
  # Get shipping rule
  data, status_code, headers = api_instance.get_shipping_rule_with_http_info(org_id, rule_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListShippingRules200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->get_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **rule_id** | **String** | Shipping Rule ID |  |

### Return type

[**ListShippingRules200ResponseDataInner**](ListShippingRules200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_shipping_rules

> <ListShippingRules200Response> list_shipping_rules(org_id, opts)

List shipping rules

Returns a paginated list of shipping rules for the organization with their relations.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::RulesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20 # Integer | Items per page (max 100)
}

begin
  # List shipping rules
  result = api_instance.list_shipping_rules(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->list_shipping_rules: #{e}"
end
```

#### Using the list_shipping_rules_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListShippingRules200Response>, Integer, Hash)> list_shipping_rules_with_http_info(org_id, opts)

```ruby
begin
  # List shipping rules
  data, status_code, headers = api_instance.list_shipping_rules_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListShippingRules200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->list_shipping_rules_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |

### Return type

[**ListShippingRules200Response**](ListShippingRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_shipping_rule

> <CreateShippingRule201Response> update_shipping_rule(org_id, rule_id, update_shipping_rule_request)

Update shipping rule

Updates an existing shipping rule for the organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::RulesApi.new
org_id = 'org_01HZX9K2QF' # String | Organization ID
rule_id = 'rule_01HZX9K2QF' # String | Shipping Rule ID
update_shipping_rule_request = Zippendo::UpdateShippingRuleRequest.new # UpdateShippingRuleRequest | 

begin
  # Update shipping rule
  result = api_instance.update_shipping_rule(org_id, rule_id, update_shipping_rule_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->update_shipping_rule: #{e}"
end
```

#### Using the update_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateShippingRule201Response>, Integer, Hash)> update_shipping_rule_with_http_info(org_id, rule_id, update_shipping_rule_request)

```ruby
begin
  # Update shipping rule
  data, status_code, headers = api_instance.update_shipping_rule_with_http_info(org_id, rule_id, update_shipping_rule_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateShippingRule201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling RulesApi->update_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **rule_id** | **String** | Shipping Rule ID |  |
| **update_shipping_rule_request** | [**UpdateShippingRuleRequest**](UpdateShippingRuleRequest.md) |  |  |

### Return type

[**CreateShippingRule201Response**](CreateShippingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

