# Zippendo::WebhooksApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_org_webhook**](WebhooksApi.md#create_org_webhook) | **POST** /orgs/{orgId}/webhooks | Create webhook |
| [**delete_org_webhook**](WebhooksApi.md#delete_org_webhook) | **DELETE** /orgs/{orgId}/webhooks/{webhookId} | Delete webhook |
| [**get_org_webhook**](WebhooksApi.md#get_org_webhook) | **GET** /orgs/{orgId}/webhooks/{webhookId} | Get webhook |
| [**list_org_webhook_deliveries**](WebhooksApi.md#list_org_webhook_deliveries) | **GET** /orgs/{orgId}/webhooks/{webhookId}/deliveries | List webhook deliveries |
| [**list_org_webhooks**](WebhooksApi.md#list_org_webhooks) | **GET** /orgs/{orgId}/webhooks | List webhooks |
| [**test_org_webhook**](WebhooksApi.md#test_org_webhook) | **POST** /orgs/{orgId}/webhooks/{webhookId}/test | Test webhook |
| [**update_org_webhook**](WebhooksApi.md#update_org_webhook) | **PATCH** /orgs/{orgId}/webhooks/{webhookId} | Update webhook |


## create_org_webhook

> <CreateOrgWebhook201Response> create_org_webhook(org_id, create_org_webhook_request)

Create webhook

Create a new webhook endpoint for an organization that receives event notifications.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
create_org_webhook_request = Zippendo::CreateOrgWebhookRequest.new({name: 'Order fulfilment notifier', url: 'https://hooks.example.dk/zippendo', events: ["shipment.created", "tracking.updated"]}) # CreateOrgWebhookRequest | 

begin
  # Create webhook
  result = api_instance.create_org_webhook(org_id, create_org_webhook_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->create_org_webhook: #{e}"
end
```

#### Using the create_org_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateOrgWebhook201Response>, Integer, Hash)> create_org_webhook_with_http_info(org_id, create_org_webhook_request)

```ruby
begin
  # Create webhook
  data, status_code, headers = api_instance.create_org_webhook_with_http_info(org_id, create_org_webhook_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateOrgWebhook201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->create_org_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **create_org_webhook_request** | [**CreateOrgWebhookRequest**](CreateOrgWebhookRequest.md) |  |  |

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_org_webhook

> <DeleteOrgWebhook200Response> delete_org_webhook(org_id, webhook_id)

Delete webhook

Permanently delete a webhook and all its delivery logs.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_clx1a2b3c4' # String | Organization ID
webhook_id = 'wh_clx1a2b3c4' # String | Webhook ID

begin
  # Delete webhook
  result = api_instance.delete_org_webhook(org_id, webhook_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->delete_org_webhook: #{e}"
end
```

#### Using the delete_org_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteOrgWebhook200Response>, Integer, Hash)> delete_org_webhook_with_http_info(org_id, webhook_id)

```ruby
begin
  # Delete webhook
  data, status_code, headers = api_instance.delete_org_webhook_with_http_info(org_id, webhook_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteOrgWebhook200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->delete_org_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **webhook_id** | **String** | Webhook ID |  |

### Return type

[**DeleteOrgWebhook200Response**](DeleteOrgWebhook200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_org_webhook

> <CreateOrgWebhook201Response> get_org_webhook(org_id, webhook_id)

Get webhook

Get a specific webhook including its signing secret.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_clx1a2b3c4' # String | Organization ID
webhook_id = 'wh_clx1a2b3c4' # String | Webhook ID

begin
  # Get webhook
  result = api_instance.get_org_webhook(org_id, webhook_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->get_org_webhook: #{e}"
end
```

#### Using the get_org_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateOrgWebhook201Response>, Integer, Hash)> get_org_webhook_with_http_info(org_id, webhook_id)

```ruby
begin
  # Get webhook
  data, status_code, headers = api_instance.get_org_webhook_with_http_info(org_id, webhook_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateOrgWebhook201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->get_org_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **webhook_id** | **String** | Webhook ID |  |

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_org_webhook_deliveries

> <ListOrgWebhookDeliveries200Response> list_org_webhook_deliveries(org_id, webhook_id, opts)

List webhook deliveries

List the delivery history for a specific webhook.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_clx1a2b3c4' # String | Organization ID
webhook_id = 'wh_clx1a2b3c4' # String | Webhook ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20 # Integer | Items per page (max 100)
}

begin
  # List webhook deliveries
  result = api_instance.list_org_webhook_deliveries(org_id, webhook_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->list_org_webhook_deliveries: #{e}"
end
```

#### Using the list_org_webhook_deliveries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgWebhookDeliveries200Response>, Integer, Hash)> list_org_webhook_deliveries_with_http_info(org_id, webhook_id, opts)

```ruby
begin
  # List webhook deliveries
  data, status_code, headers = api_instance.list_org_webhook_deliveries_with_http_info(org_id, webhook_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgWebhookDeliveries200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->list_org_webhook_deliveries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **webhook_id** | **String** | Webhook ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |

### Return type

[**ListOrgWebhookDeliveries200Response**](ListOrgWebhookDeliveries200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_org_webhooks

> <ListOrgWebhooks200Response> list_org_webhooks(org_id, opts)

List webhooks

List all webhooks belonging to an organization.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_8f3kd92ld0' # String | Organization ID
opts = {
  page: 1, # Integer | Page number (1-based)
  limit: 20 # Integer | Items per page (max 100)
}

begin
  # List webhooks
  result = api_instance.list_org_webhooks(org_id, opts)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->list_org_webhooks: #{e}"
end
```

#### Using the list_org_webhooks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListOrgWebhooks200Response>, Integer, Hash)> list_org_webhooks_with_http_info(org_id, opts)

```ruby
begin
  # List webhooks
  data, status_code, headers = api_instance.list_org_webhooks_with_http_info(org_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListOrgWebhooks200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->list_org_webhooks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional][default to 20] |

### Return type

[**ListOrgWebhooks200Response**](ListOrgWebhooks200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## test_org_webhook

> <TestOrgWebhook200Response> test_org_webhook(org_id, webhook_id)

Test webhook

Send a test ping event to the webhook endpoint to verify connectivity.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_clx1a2b3c4' # String | Organization ID
webhook_id = 'wh_clx1a2b3c4' # String | Webhook ID

begin
  # Test webhook
  result = api_instance.test_org_webhook(org_id, webhook_id)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->test_org_webhook: #{e}"
end
```

#### Using the test_org_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TestOrgWebhook200Response>, Integer, Hash)> test_org_webhook_with_http_info(org_id, webhook_id)

```ruby
begin
  # Test webhook
  data, status_code, headers = api_instance.test_org_webhook_with_http_info(org_id, webhook_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TestOrgWebhook200Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->test_org_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **webhook_id** | **String** | Webhook ID |  |

### Return type

[**TestOrgWebhook200Response**](TestOrgWebhook200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_org_webhook

> <CreateOrgWebhook201Response> update_org_webhook(org_id, webhook_id, update_org_webhook_request)

Update webhook

Update the configuration of an existing webhook.

### Examples

```ruby
require 'time'
require 'zippendo'
# setup authorization
Zippendo.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Zippendo::WebhooksApi.new
org_id = 'org_clx1a2b3c4' # String | Organization ID
webhook_id = 'wh_clx1a2b3c4' # String | Webhook ID
update_org_webhook_request = Zippendo::UpdateOrgWebhookRequest.new # UpdateOrgWebhookRequest | 

begin
  # Update webhook
  result = api_instance.update_org_webhook(org_id, webhook_id, update_org_webhook_request)
  p result
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->update_org_webhook: #{e}"
end
```

#### Using the update_org_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateOrgWebhook201Response>, Integer, Hash)> update_org_webhook_with_http_info(org_id, webhook_id, update_org_webhook_request)

```ruby
begin
  # Update webhook
  data, status_code, headers = api_instance.update_org_webhook_with_http_info(org_id, webhook_id, update_org_webhook_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateOrgWebhook201Response>
rescue Zippendo::ApiError => e
  puts "Error when calling WebhooksApi->update_org_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **org_id** | **String** | Organization ID |  |
| **webhook_id** | **String** | Webhook ID |  |
| **update_org_webhook_request** | [**UpdateOrgWebhookRequest**](UpdateOrgWebhookRequest.md) |  |  |

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

