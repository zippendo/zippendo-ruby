# Zippendo::OrgsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_org_logo**](OrgsApi.md#delete_org_logo) | **DELETE** /orgs/{orgId}/branding/logo | Delete org logo |
| [**get_org**](OrgsApi.md#get_org) | **GET** /orgs/{id} | Get org |
| [**get_org_branding**](OrgsApi.md#get_org_branding) | **GET** /orgs/{orgId}/branding | Get org branding |
| [**get_org_logo**](OrgsApi.md#get_org_logo) | **GET** /orgs/{orgId}/branding/logo | Download org logo |
| [**update_org**](OrgsApi.md#update_org) | **PUT** /orgs/{id} | Update org |
| [**update_org_branding**](OrgsApi.md#update_org_branding) | **PUT** /orgs/{orgId}/branding | Update org branding |
| [**upload_org_logo**](OrgsApi.md#upload_org_logo) | **POST** /orgs/{orgId}/branding/logo | Upload org logo |


## delete_org_logo

> <GetOrgBranding200Response> delete_org_logo(org_id)

Delete org logo

Removes the org logo. Requires the customBranding entitlement.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID

begin
  # Delete org logo
  result = api_instance.delete_org_logo(org_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->delete_org_logo: #{e}"
end
```

#### Using the delete_org_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrgBranding200Response>, Integer, Hash)> delete_org_logo_with_http_info(org_id)

```ruby
begin
  # Delete org logo
  data, status_code, headers = api_instance.delete_org_logo_with_http_info(org_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrgBranding200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->delete_org_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_org

> <GetOrg200Response> get_org(id)

Get org

Returns a specific organization by ID, including its member count.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
id = 'clz9x8a7b0001' # String | Resource ID

begin
  # Get org
  result = api_instance.get_org(id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->get_org: #{e}"
end
```

#### Using the get_org_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrg200Response>, Integer, Hash)> get_org_with_http_info(id)

```ruby
begin
  # Get org
  data, status_code, headers = api_instance.get_org_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrg200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->get_org_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Resource ID |  |

### Return type

[**GetOrg200Response**](GetOrg200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_org_branding

> <GetOrgBranding200Response> get_org_branding(org_id)

Get org branding

Returns the org's brand colors and an authenticated URL to download the logo.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID

begin
  # Get org branding
  result = api_instance.get_org_branding(org_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->get_org_branding: #{e}"
end
```

#### Using the get_org_branding_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrgBranding200Response>, Integer, Hash)> get_org_branding_with_http_info(org_id)

```ruby
begin
  # Get org branding
  data, status_code, headers = api_instance.get_org_branding_with_http_info(org_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrgBranding200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->get_org_branding_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_org_logo

> File get_org_logo(org_id)

Download org logo

Returns the org logo image bytes with the stored content type.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID

begin
  # Download org logo
  result = api_instance.get_org_logo(org_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->get_org_logo: #{e}"
end
```

#### Using the get_org_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> get_org_logo_with_http_info(org_id)

```ruby
begin
  # Download org logo
  data, status_code, headers = api_instance.get_org_logo_with_http_info(org_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->get_org_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |

### Return type

**File**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: image/png, image/jpeg, image/webp


## update_org

> <UpdateOrg200Response> update_org(id, update_org_request)

Update org

Updates an existing organization's profile, billing, and customs settings.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
id = 'clz9x8a7b0001' # String | Resource ID
update_org_request = Zippendo::UpdateOrgRequest.new # UpdateOrgRequest | 

begin
  # Update org
  result = api_instance.update_org(id, update_org_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->update_org: #{e}"
end
```

#### Using the update_org_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateOrg200Response>, Integer, Hash)> update_org_with_http_info(id, update_org_request)

```ruby
begin
  # Update org
  data, status_code, headers = api_instance.update_org_with_http_info(id, update_org_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateOrg200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->update_org_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Resource ID |  |
| **update_org_request** | [**UpdateOrgRequest**](UpdateOrgRequest.md) |  |  |

### Return type

[**UpdateOrg200Response**](UpdateOrg200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_org_branding

> <GetOrgBranding200Response> update_org_branding(org_id, update_org_branding_request)

Update org branding

Sets the org brand colors. Requires the customBranding entitlement.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
update_org_branding_request = Zippendo::UpdateOrgBrandingRequest.new # UpdateOrgBrandingRequest | 

begin
  # Update org branding
  result = api_instance.update_org_branding(org_id, update_org_branding_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->update_org_branding: #{e}"
end
```

#### Using the update_org_branding_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrgBranding200Response>, Integer, Hash)> update_org_branding_with_http_info(org_id, update_org_branding_request)

```ruby
begin
  # Update org branding
  data, status_code, headers = api_instance.update_org_branding_with_http_info(org_id, update_org_branding_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrgBranding200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->update_org_branding_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **update_org_branding_request** | [**UpdateOrgBrandingRequest**](UpdateOrgBrandingRequest.md) |  |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upload_org_logo

> <GetOrgBranding200Response> upload_org_logo(org_id, file)

Upload org logo

Uploads the org logo as multipart/form-data. Accepts PNG, JPG, or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Requires the customBranding entitlement.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::OrgsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
file = File.new('/path/to/some/file') # File | Image file (PNG, JPG, or WEBP)

begin
  # Upload org logo
  result = api_instance.upload_org_logo(org_id, file)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->upload_org_logo: #{e}"
end
```

#### Using the upload_org_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetOrgBranding200Response>, Integer, Hash)> upload_org_logo_with_http_info(org_id, file)

```ruby
begin
  # Upload org logo
  data, status_code, headers = api_instance.upload_org_logo_with_http_info(org_id, file)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetOrgBranding200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling OrgsApi->upload_org_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **file** | **File** | Image file (PNG, JPG, or WEBP) |  |

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

