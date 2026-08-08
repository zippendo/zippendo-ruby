# Zippendo::BrandsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**archive_org_brand**](BrandsApi.md#archive_org_brand) | **POST** /orgs/{orgId}/brands/{brandId}/archive | Archive brand |
| [**check_brand_slug**](BrandsApi.md#check_brand_slug) | **GET** /orgs/{orgId}/brands/check-slug/{slug} | Check brand slug availability |
| [**create_org_brand**](BrandsApi.md#create_org_brand) | **POST** /orgs/{orgId}/brands | Create brand |
| [**delete_brand_logo**](BrandsApi.md#delete_brand_logo) | **DELETE** /orgs/{orgId}/brands/{brandId}/logo | Delete brand logo |
| [**get_brand_logo**](BrandsApi.md#get_brand_logo) | **GET** /orgs/{orgId}/brands/{brandId}/logo | Get brand logo |
| [**get_org_brand**](BrandsApi.md#get_org_brand) | **GET** /orgs/{orgId}/brands/{brandId} | Get brand |
| [**list_org_brands**](BrandsApi.md#list_org_brands) | **GET** /orgs/{orgId}/brands | List brands |
| [**unarchive_org_brand**](BrandsApi.md#unarchive_org_brand) | **POST** /orgs/{orgId}/brands/{brandId}/unarchive | Unarchive brand |
| [**update_org_brand**](BrandsApi.md#update_org_brand) | **PATCH** /orgs/{orgId}/brands/{brandId} | Update brand |
| [**upload_brand_logo**](BrandsApi.md#upload_brand_logo) | **POST** /orgs/{orgId}/brands/{brandId}/logo | Upload brand logo |


## archive_org_brand

> <ListOrgBrands200ResponseDataInner> archive_org_brand(org_id, brand_id)

Archive brand

Archives a brand: it leaves the brand switcher and default listings, but its orders, shipments and settings are retained and remain visible in the organization-wide view.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID

begin
  # Archive brand
  result = api_instance.archive_org_brand(org_id, brand_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->archive_org_brand: #{e}"
end
```

#### Using the archive_org_brand_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> archive_org_brand_with_http_info(org_id, brand_id)

```ruby
begin
  # Archive brand
  data, status_code, headers = api_instance.archive_org_brand_with_http_info(org_id, brand_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->archive_org_brand_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## check_brand_slug

> <CheckBrandSlug200Response> check_brand_slug(org_id, slug)

Check brand slug availability

Reports whether a brand slug is free within this organization. Brand slugs are unique per organization, so the same slug may exist in another organization. Archived brands still hold their slug.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
slug = 'acme' # String | Brand slug to check

begin
  # Check brand slug availability
  result = api_instance.check_brand_slug(org_id, slug)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->check_brand_slug: #{e}"
end
```

#### Using the check_brand_slug_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckBrandSlug200Response>, Integer, Hash)> check_brand_slug_with_http_info(org_id, slug)

```ruby
begin
  # Check brand slug availability
  data, status_code, headers = api_instance.check_brand_slug_with_http_info(org_id, slug)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckBrandSlug200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->check_brand_slug_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **slug** | **String** | Brand slug to check |  |

### Return type

[**CheckBrandSlug200Response**](CheckBrandSlug200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_org_brand

> <ListOrgBrands200ResponseDataInner> create_org_brand(org_id, create_org_brand_request)

Create brand

Creates a brand (sub-account) in the organization. The slug is derived from the name when omitted. Requires a plan that includes brands.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
create_org_brand_request = Zippendo::CreateOrgBrandRequest.new({name: 'Acme'}) # CreateOrgBrandRequest | 

begin
  # Create brand
  result = api_instance.create_org_brand(org_id, create_org_brand_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->create_org_brand: #{e}"
end
```

#### Using the create_org_brand_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> create_org_brand_with_http_info(org_id, create_org_brand_request)

```ruby
begin
  # Create brand
  data, status_code, headers = api_instance.create_org_brand_with_http_info(org_id, create_org_brand_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->create_org_brand_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_org_brand_request** | [**CreateOrgBrandRequest**](CreateOrgBrandRequest.md) |  |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_brand_logo

> <ListOrgBrands200ResponseDataInner> delete_brand_logo(org_id, brand_id)

Delete brand logo

Removes a brand's logo. Its documents fall back to the organization's logo. Requires the brands and customBranding entitlements.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID

begin
  # Delete brand logo
  result = api_instance.delete_brand_logo(org_id, brand_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->delete_brand_logo: #{e}"
end
```

#### Using the delete_brand_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> delete_brand_logo_with_http_info(org_id, brand_id)

```ruby
begin
  # Delete brand logo
  data, status_code, headers = api_instance.delete_brand_logo_with_http_info(org_id, brand_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->delete_brand_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_brand_logo

> File get_brand_logo(org_id, brand_id)

Get brand logo

Streams the brand's logo bytes. This is the URL returned as the brand's `logoUrl`.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID

begin
  # Get brand logo
  result = api_instance.get_brand_logo(org_id, brand_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->get_brand_logo: #{e}"
end
```

#### Using the get_brand_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> get_brand_logo_with_http_info(org_id, brand_id)

```ruby
begin
  # Get brand logo
  data, status_code, headers = api_instance.get_brand_logo_with_http_info(org_id, brand_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->get_brand_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |

### Return type

**File**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: image/png, image/jpeg, image/webp


## get_org_brand

> <ListOrgBrands200ResponseDataInner> get_org_brand(org_id, brand_id)

Get brand

Returns a single brand (sub-account) by id.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID

begin
  # Get brand
  result = api_instance.get_org_brand(org_id, brand_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->get_org_brand: #{e}"
end
```

#### Using the get_org_brand_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> get_org_brand_with_http_info(org_id, brand_id)

```ruby
begin
  # Get brand
  data, status_code, headers = api_instance.get_org_brand_with_http_info(org_id, brand_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->get_org_brand_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_org_brands

> <ListOrgBrands200Response> list_org_brands(org_id, opts)

List brands

Returns the organization's brands (sub-accounts). Archived brands are excluded unless `includeArchived` is set.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
opts = {
  include_archived: 'false' # String | Include archived brands in the response
}

begin
  # List brands
  result = api_instance.list_org_brands(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->list_org_brands: #{e}"
end
```

#### Using the list_org_brands_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200Response>, Integer, Hash)> list_org_brands_with_http_info(org_id, opts)

```ruby
begin
  # List brands
  data, status_code, headers = api_instance.list_org_brands_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->list_org_brands_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **include_archived** | **String** | Include archived brands in the response | [optional] |

### Return type

[**ListOrgBrands200Response**](ListOrgBrands200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## unarchive_org_brand

> <ListOrgBrands200ResponseDataInner> unarchive_org_brand(org_id, brand_id)

Unarchive brand

Restores an archived brand so it appears in the brand switcher again.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID

begin
  # Unarchive brand
  result = api_instance.unarchive_org_brand(org_id, brand_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->unarchive_org_brand: #{e}"
end
```

#### Using the unarchive_org_brand_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> unarchive_org_brand_with_http_info(org_id, brand_id)

```ruby
begin
  # Unarchive brand
  data, status_code, headers = api_instance.unarchive_org_brand_with_http_info(org_id, brand_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->unarchive_org_brand_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_org_brand

> <ListOrgBrands200ResponseDataInner> update_org_brand(org_id, brand_id, update_org_brand_request)

Update brand

Updates a brand's name, slug, identity overrides (company name, VAT, customs, address) and document colours. Null clears an override so the organization's value applies again.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID
update_org_brand_request = Zippendo::UpdateOrgBrandRequest.new # UpdateOrgBrandRequest | 

begin
  # Update brand
  result = api_instance.update_org_brand(org_id, brand_id, update_org_brand_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->update_org_brand: #{e}"
end
```

#### Using the update_org_brand_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> update_org_brand_with_http_info(org_id, brand_id, update_org_brand_request)

```ruby
begin
  # Update brand
  data, status_code, headers = api_instance.update_org_brand_with_http_info(org_id, brand_id, update_org_brand_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->update_org_brand_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |
| **update_org_brand_request** | [**UpdateOrgBrandRequest**](UpdateOrgBrandRequest.md) |  |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upload_brand_logo

> <ListOrgBrands200ResponseDataInner> upload_brand_logo(org_id, brand_id, file)

Upload brand logo

Uploads a brand's logo as multipart/form-data. Accepts PNG, JPG or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Documents for this brand's shipments use it instead of the organization's logo. Requires the brands and customBranding entitlements.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::BrandsApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
brand_id = 'brnd_8f3kd92ld0' # String | Brand ID
file = File.new('/path/to/some/file') # File | Image file (PNG, JPG, or WEBP)

begin
  # Upload brand logo
  result = api_instance.upload_brand_logo(org_id, brand_id, file)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->upload_brand_logo: #{e}"
end
```

#### Using the upload_brand_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgBrands200ResponseDataInner>, Integer, Hash)> upload_brand_logo_with_http_info(org_id, brand_id, file)

```ruby
begin
  # Upload brand logo
  data, status_code, headers = api_instance.upload_brand_logo_with_http_info(org_id, brand_id, file)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgBrands200ResponseDataInner>
rescue Zippendo::ApiError => e
  puts "Error when calling BrandsApi->upload_brand_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **brand_id** | **String** | Brand ID |  |
| **file** | **File** | Image file (PNG, JPG, or WEBP) |  |

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

