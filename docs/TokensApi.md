# Zippendo::TokensApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_api_token**](TokensApi.md#create_api_token) | **POST** /orgs/{orgId}/api-tokens | Create API keys |
| [**get_api_token**](TokensApi.md#get_api_token) | **GET** /orgs/{orgId}/api-tokens/{tokenId} | Get API keys |
| [**list_api_tokens**](TokensApi.md#list_api_tokens) | **GET** /orgs/{orgId}/api-tokens | List API keys |
| [**revoke_api_token**](TokensApi.md#revoke_api_token) | **DELETE** /orgs/{orgId}/api-tokens/{tokenId} | Revoke API keys |
| [**update_api_token**](TokensApi.md#update_api_token) | **PATCH** /orgs/{orgId}/api-tokens/{tokenId} | Update API keys |
| [**verify_api_token**](TokensApi.md#verify_api_token) | **POST** /api-tokens/verify | Verify API keys |


## create_api_token

> <CreateApiToken201Response> create_api_token(org_id, create_api_token_request)

Create API keys

Creates a new API token for the specified organization. The full token is only shown once.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::TokensApi.new
org_id = 'org_4d8af01qw2' # String | Organization ID
create_api_token_request = Zippendo::CreateApiTokenRequest.new({name: 'Warehouse integration', scopes: ["read: shipments", "write: shipments"]}) # CreateApiTokenRequest | 

begin
  # Create API keys
  result = api_instance.create_api_token(org_id, create_api_token_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->create_api_token: #{e}"
end
```

#### Using the create_api_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateApiToken201Response>, Integer, Hash)> create_api_token_with_http_info(org_id, create_api_token_request)

```ruby
begin
  # Create API keys
  data, status_code, headers = api_instance.create_api_token_with_http_info(org_id, create_api_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateApiToken201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->create_api_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_api_token_request** | [**CreateApiTokenRequest**](CreateApiTokenRequest.md) |  |  |

### Return type

[**CreateApiToken201Response**](CreateApiToken201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_api_token

> <ListApiTokens200ResponseDataInner> get_api_token(org_id, token_id)

Get API keys

Returns metadata for a specific API token. The token secret is never returned.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::TokensApi.new
org_id = 'org_4d8af01qw2' # String | Organization ID
token_id = 'tok_6e2fa83ij9' # String | API Token ID

begin
  # Get API keys
  result = api_instance.get_api_token(org_id, token_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->get_api_token: #{e}"
end
```

#### Using the get_api_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListApiTokens200ResponseDataInner>, Integer, Hash)> get_api_token_with_http_info(org_id, token_id)

```ruby
begin
  # Get API keys
  data, status_code, headers = api_instance.get_api_token_with_http_info(org_id, token_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListApiTokens200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->get_api_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **token_id** | **String** | API Token ID |  |

### Return type

[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_api_tokens

> <ListApiTokens200Response> list_api_tokens(org_id, opts)

List API keys

Returns a paginated list of API tokens belonging to the specified organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::TokensApi.new
org_id = 'org_4d8af01qw2' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20 # Integer | Items per page (max 100)
}

begin
  # List API keys
  result = api_instance.list_api_tokens(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->list_api_tokens: #{e}"
end
```

#### Using the list_api_tokens_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListApiTokens200Response>, Integer, Hash)> list_api_tokens_with_http_info(org_id, opts)

```ruby
begin
  # List API keys
  data, status_code, headers = api_instance.list_api_tokens_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListApiTokens200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->list_api_tokens_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |

### Return type

[**ListApiTokens200Response**](ListApiTokens200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## revoke_api_token

> <RevokeApiToken200Response> revoke_api_token(org_id, token_id)

Revoke API keys

Revokes and deletes an API token.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::TokensApi.new
org_id = 'org_4d8af01qw2' # String | Organization ID
token_id = 'tok_6e2fa83ij9' # String | API Token ID

begin
  # Revoke API keys
  result = api_instance.revoke_api_token(org_id, token_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->revoke_api_token: #{e}"
end
```

#### Using the revoke_api_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RevokeApiToken200Response>, Integer, Hash)> revoke_api_token_with_http_info(org_id, token_id)

```ruby
begin
  # Revoke API keys
  data, status_code, headers = api_instance.revoke_api_token_with_http_info(org_id, token_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RevokeApiToken200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->revoke_api_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **token_id** | **String** | API Token ID |  |

### Return type

[**RevokeApiToken200Response**](RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_api_token

> <ListApiTokens200ResponseDataInner> update_api_token(org_id, token_id, update_api_token_request)

Update API keys

Updates the name of an API token.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::TokensApi.new
org_id = 'org_4d8af01qw2' # String | Organization ID
token_id = 'tok_6e2fa83ij9' # String | API Token ID
update_api_token_request = Zippendo::UpdateApiTokenRequest.new({name: 'Warehouse integration'}) # UpdateApiTokenRequest | 

begin
  # Update API keys
  result = api_instance.update_api_token(org_id, token_id, update_api_token_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->update_api_token: #{e}"
end
```

#### Using the update_api_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListApiTokens200ResponseDataInner>, Integer, Hash)> update_api_token_with_http_info(org_id, token_id, update_api_token_request)

```ruby
begin
  # Update API keys
  data, status_code, headers = api_instance.update_api_token_with_http_info(org_id, token_id, update_api_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListApiTokens200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->update_api_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **token_id** | **String** | API Token ID |  |
| **update_api_token_request** | [**UpdateApiTokenRequest**](UpdateApiTokenRequest.md) |  |  |

### Return type

[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## verify_api_token

> <VerifyApiToken200Response> verify_api_token(verify_api_token_request)

Verify API keys

Verifies whether an API token is valid and returns its metadata.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::TokensApi.new
verify_api_token_request = Zippendo::VerifyApiTokenRequest.new({token: 'zipp_live_8f3kd92ld0a7b6c5d4e3f2a1'}) # VerifyApiTokenRequest | 

begin
  # Verify API keys
  result = api_instance.verify_api_token(verify_api_token_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->verify_api_token: #{e}"
end
```

#### Using the verify_api_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VerifyApiToken200Response>, Integer, Hash)> verify_api_token_with_http_info(verify_api_token_request)

```ruby
begin
  # Verify API keys
  data, status_code, headers = api_instance.verify_api_token_with_http_info(verify_api_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VerifyApiToken200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling TokensApi->verify_api_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **verify_api_token_request** | [**VerifyApiTokenRequest**](VerifyApiTokenRequest.md) |  |  |

### Return type

[**VerifyApiToken200Response**](VerifyApiToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

