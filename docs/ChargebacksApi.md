# Komoju::ChargebacksApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**accept_chargeback_request**](ChargebacksApi.md#accept_chargeback_request) | **POST** /chargeback_requests/{id}/accept | Chargeback: Accept |
| [**defend_chargeback_request**](ChargebacksApi.md#defend_chargeback_request) | **POST** /chargeback_requests/{id}/defend | Chargeback: Defend |
| [**list_chargeback_requests**](ChargebacksApi.md#list_chargeback_requests) | **GET** /chargeback_requests | Chargeback: List |
| [**show_chargeback_request**](ChargebacksApi.md#show_chargeback_request) | **GET** /chargeback_requests/{id} | Chargeback: Show |

## Request Models

- [**DefendChargebackRequestBody**](DefendChargebackRequestBody.md) — used by `defend_chargeback_request`


## accept_chargeback_request

> accept_chargeback_request(id)

Chargeback: Accept

Accepts a chargeback, agreeing to the dispute. Takes no request body.  A chargeback can only be accepted while its status is `pending`. If the due date has passed, the request returns an error. Accepting an already-accepted chargeback returns `204` (idempotent).

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::ChargebacksApi.new
id = 'id_example' # String | The chargeback request UUID.

begin
  # Chargeback: Accept
  api_instance.accept_chargeback_request(id)
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->accept_chargeback_request: #{e}"
end
```

#### Using the accept_chargeback_request_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> accept_chargeback_request_with_http_info(id)

```ruby
begin
  # Chargeback: Accept
  data, status_code, headers = api_instance.accept_chargeback_request_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->accept_chargeback_request_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The chargeback request UUID. |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## defend_chargeback_request

> defend_chargeback_request(id, defend_chargeback_request_body)

Chargeback: Defend

Submits a defense against a chargeback, including supporting documentation.  A chargeback can only be defended while its status is `pending`. If the due date has passed, the request returns an error. Defending an already-defended chargeback returns `204` (idempotent). Only one defense can be created per chargeback request.  The `document.document_base64` payload must be 15 MB or less. Supported types are PDF, JPG/JPEG, PNG, and GIF; the type is inferred from the file's bytes, not the filename.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::ChargebacksApi.new
id = 'id_example' # String | The chargeback request UUID.
defend_chargeback_request_body = Komoju::DefendChargebackRequestBody.new({description: 'description_example', document: Komoju::DefendChargebackDocument.new({document_base64: 'document_base64_example'})}) # DefendChargebackRequestBody | 

begin
  # Chargeback: Defend
  api_instance.defend_chargeback_request(id, defend_chargeback_request_body)
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->defend_chargeback_request: #{e}"
end
```

#### Using the defend_chargeback_request_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> defend_chargeback_request_with_http_info(id, defend_chargeback_request_body)

```ruby
begin
  # Chargeback: Defend
  data, status_code, headers = api_instance.defend_chargeback_request_with_http_info(id, defend_chargeback_request_body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->defend_chargeback_request_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The chargeback request UUID. |  |
| **defend_chargeback_request_body** | [**DefendChargebackRequestBody**](DefendChargebackRequestBody.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_chargeback_requests

> <ChargebackRequestList> list_chargeback_requests(opts)

Chargeback: List

Retrieves a paginated list of chargeback requests for the authenticated merchant.  Results are ordered with `pending` chargebacks first, followed by non-pending chargebacks. There is no request sort parameter.  This endpoint is only available to merchants with the chargeback feature enabled; otherwise it returns `404 Not Found`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::ChargebacksApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  status: Komoju::ChargebackStatus::PENDING, # ChargebackStatus | Filter by chargeback status.
  payment_id: 'payment_id_example', # String | Filter by the associated payment ID.
  due_date_start: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Lower bound (inclusive) on the chargeback's due date.
  due_date_end: Time.parse('2013-10-20T19:20:30+01:00') # Time | Upper bound (inclusive) on the chargeback's due date.
}

begin
  # Chargeback: List
  result = api_instance.list_chargeback_requests(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->list_chargeback_requests: #{e}"
end
```

#### Using the list_chargeback_requests_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ChargebackRequestList>, Integer, Hash)> list_chargeback_requests_with_http_info(opts)

```ruby
begin
  # Chargeback: List
  data, status_code, headers = api_instance.list_chargeback_requests_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ChargebackRequestList>
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->list_chargeback_requests_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **status** | [**ChargebackStatus**](.md) | Filter by chargeback status. | [optional] |
| **payment_id** | **String** | Filter by the associated payment ID. | [optional] |
| **due_date_start** | **Time** | Lower bound (inclusive) on the chargeback&#39;s due date. | [optional] |
| **due_date_end** | **Time** | Upper bound (inclusive) on the chargeback&#39;s due date. | [optional] |

### Return type

[**ChargebackRequestList**](ChargebackRequestList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_chargeback_request

> <ChargebackRequestDetail> show_chargeback_request(id)

Chargeback: Show

Retrieves the details of a single chargeback request, including its timeline, payment, customer, and defense (if one exists).  This endpoint is only available to merchants with the chargeback feature enabled; otherwise it returns `404 Not Found`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::ChargebacksApi.new
id = 'id_example' # String | The chargeback request UUID.

begin
  # Chargeback: Show
  result = api_instance.show_chargeback_request(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->show_chargeback_request: #{e}"
end
```

#### Using the show_chargeback_request_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ChargebackRequestDetail>, Integer, Hash)> show_chargeback_request_with_http_info(id)

```ruby
begin
  # Chargeback: Show
  data, status_code, headers = api_instance.show_chargeback_request_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ChargebackRequestDetail>
rescue Komoju::ApiError => e
  puts "Error when calling ChargebacksApi->show_chargeback_request_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The chargeback request UUID. |  |

### Return type

[**ChargebackRequestDetail**](ChargebackRequestDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

