# Komoju::SessionsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_session**](SessionsApi.md#cancel_session) | **POST** /sessions/{id}/cancel | Session: Cancel |
| [**create_session**](SessionsApi.md#create_session) | **POST** /sessions | Session: Create |
| [**pay_session**](SessionsApi.md#pay_session) | **POST** /sessions/{id}/pay | Session: Pay |
| [**show_session**](SessionsApi.md#show_session) | **GET** /sessions/{id} | Session: Show |

## Request Models

- [**CreateSessionRequest**](CreateSessionRequest.md) — used by `create_session`
- [**PaySessionRequest**](PaySessionRequest.md) — used by `pay_session`


## cancel_session

> <Session> cancel_session(id)

Session: Cancel

Cancels a session.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SessionsApi.new
id = 'id_example' # String | A unique identifier for the session.

begin
  # Session: Cancel
  result = api_instance.cancel_session(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->cancel_session: #{e}"
end
```

#### Using the cancel_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Session>, Integer, Hash)> cancel_session_with_http_info(id)

```ruby
begin
  # Session: Cancel
  data, status_code, headers = api_instance.cancel_session_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Session>
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->cancel_session_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the session. |  |

### Return type

[**Session**](Session.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_session

> <Session> create_session(create_session_request)

Session: Create

Creates a session. There're 3 modes for the session:  * `payment`: A payment will be created after user completed the session (default). * `customer`: A customer will be created instead of a payment, or updated if `customer_id` is given. This customer resource can then be used to perform delayed billing or subscriptions. * `customer_payment`: A payment will be created, and customer will be created or updated. You can use this mode to charge money upfront and save customer's payment details in one go.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SessionsApi.new
create_session_request = Komoju::CreateSessionRequestWithCustomerMode.new({mode: 'customer', currency: Komoju::Currency::JPY}) # CreateSessionRequest | 

begin
  # Session: Create
  result = api_instance.create_session(create_session_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->create_session: #{e}"
end
```

#### Using the create_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Session>, Integer, Hash)> create_session_with_http_info(create_session_request)

```ruby
begin
  # Session: Create
  data, status_code, headers = api_instance.create_session_with_http_info(create_session_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Session>
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->create_session_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_session_request** | [**CreateSessionRequest**](CreateSessionRequest.md) |  |  |

### Return type

[**Session**](Session.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pay_session

> <PaySessionResponse> pay_session(id, pay_session_request)

Session: Pay

Provide customer payment details to pay for a session.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SessionsApi.new
id = 'id_example' # String | A unique identifier for the session.
pay_session_request = Komoju::PaySessionRequest.new({payment_details: Komoju::PaymentDetailsAU.new({type: 'au'})}) # PaySessionRequest | 

begin
  # Session: Pay
  result = api_instance.pay_session(id, pay_session_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->pay_session: #{e}"
end
```

#### Using the pay_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaySessionResponse>, Integer, Hash)> pay_session_with_http_info(id, pay_session_request)

```ruby
begin
  # Session: Pay
  data, status_code, headers = api_instance.pay_session_with_http_info(id, pay_session_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaySessionResponse>
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->pay_session_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the session. |  |
| **pay_session_request** | [**PaySessionRequest**](PaySessionRequest.md) |  |  |

### Return type

[**PaySessionResponse**](PaySessionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## show_session

> <Session> show_session(id)

Session: Show

Retrieves a Session given its ID.  A Session's status changes when the user completes or cancels their payment. You can listen for those events via webhooks, or use this API to poll for changes.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SessionsApi.new
id = 'id_example' # String | A unique identifier for the session.

begin
  # Session: Show
  result = api_instance.show_session(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->show_session: #{e}"
end
```

#### Using the show_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Session>, Integer, Hash)> show_session_with_http_info(id)

```ruby
begin
  # Session: Show
  data, status_code, headers = api_instance.show_session_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Session>
rescue Komoju::ApiError => e
  puts "Error when calling SessionsApi->show_session_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the session. |  |

### Return type

[**Session**](Session.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

