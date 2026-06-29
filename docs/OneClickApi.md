# Komoju::OneClickApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_external_customer**](OneClickApi.md#delete_external_customer) | **DELETE** /external_customers/{id} | External Customer: Destroy |

## Request Models



## delete_external_customer

> <DeleteExternalCustomer200Response> delete_external_customer(id)

External Customer: Destroy

Deletes the external customer created by the Hosted Page One-Click feature with the given `id`. This completely erases the stored payment details from our database.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::OneClickApi.new
id = 'id_example' # String | 

begin
  # External Customer: Destroy
  result = api_instance.delete_external_customer(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling OneClickApi->delete_external_customer: #{e}"
end
```

#### Using the delete_external_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteExternalCustomer200Response>, Integer, Hash)> delete_external_customer_with_http_info(id)

```ruby
begin
  # External Customer: Destroy
  data, status_code, headers = api_instance.delete_external_customer_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteExternalCustomer200Response>
rescue Komoju::ApiError => e
  puts "Error when calling OneClickApi->delete_external_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**DeleteExternalCustomer200Response**](DeleteExternalCustomer200Response.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

