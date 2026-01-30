# Komoju::PaymentsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_payment**](PaymentsApi.md#cancel_payment) | **POST** /payments/{id}/cancel | Payment: Cancel |
| [**capture_payment**](PaymentsApi.md#capture_payment) | **POST** /payments/{id}/capture | Payment: Capture |
| [**create_payment**](PaymentsApi.md#create_payment) | **POST** /payments | Payment: Create |
| [**create_refund_request**](PaymentsApi.md#create_refund_request) | **POST** /payments/{id}/refund_request | Payment: Refund Request |
| [**finalize_payment**](PaymentsApi.md#finalize_payment) | **POST** /payments/{id}/finalize | Payment: Finalize |
| [**list_payment_methods**](PaymentsApi.md#list_payment_methods) | **GET** /payment_methods | Payment Method: List |
| [**list_payments**](PaymentsApi.md#list_payments) | **GET** /payments | Payment: List |
| [**refund_payment**](PaymentsApi.md#refund_payment) | **POST** /payments/{id}/refund | Payment: Refund |
| [**show_payment**](PaymentsApi.md#show_payment) | **GET** /payments/{id} | Payment: Show |
| [**update_payment**](PaymentsApi.md#update_payment) | **PATCH** /payments/{id} | Payment: Update |


## cancel_payment

> <Payment> cancel_payment(id)

Payment: Cancel

Cancels a payment.  The given payment must have a state of `pending` or `authorized` in order to be canceled.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.

begin
  # Payment: Cancel
  result = api_instance.cancel_payment(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->cancel_payment: #{e}"
end
```

#### Using the cancel_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> cancel_payment_with_http_info(id)

```ruby
begin
  # Payment: Cancel
  data, status_code, headers = api_instance.cancel_payment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->cancel_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## capture_payment

> <Payment> capture_payment(id, capture_payment_request)

Payment: Capture

Captures a payment.  Only works when the payment was created with `capture` set to false, or via a session with `capture` set to `\"manual\"`.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.
capture_payment_request = Komoju::CapturePaymentRequest.new # CapturePaymentRequest | 

begin
  # Payment: Capture
  result = api_instance.capture_payment(id, capture_payment_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->capture_payment: #{e}"
end
```

#### Using the capture_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> capture_payment_with_http_info(id, capture_payment_request)

```ruby
begin
  # Payment: Capture
  data, status_code, headers = api_instance.capture_payment_with_http_info(id, capture_payment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->capture_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |
| **capture_payment_request** | [**CapturePaymentRequest**](CapturePaymentRequest.md) |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_payment

> <Payment> create_payment(create_payment_request)

Payment: Create

Creates a payment for a given `amount` and `currency`.  There are two ways to create payment:  - For one-time payment, you can pass `payment_details` with payment method type and additional attributes. - For recurring payment, you can pass customer's ID via `customer` attribute. Customer's saved payment method will be used for the payment.  Note that either `payment_details` or `customer` is required for the payment. However, both of them should not be given at the same time.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
create_payment_request = Komoju::CreatePaymentRequestWithCustomer.new({amount: 1000, currency: Komoju::Currency::JPY, customer: 'cust14ur4hvws08idzacf6et8'}) # CreatePaymentRequest | 

begin
  # Payment: Create
  result = api_instance.create_payment(create_payment_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->create_payment: #{e}"
end
```

#### Using the create_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> create_payment_with_http_info(create_payment_request)

```ruby
begin
  # Payment: Create
  data, status_code, headers = api_instance.create_payment_with_http_info(create_payment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->create_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_payment_request** | [**CreatePaymentRequest**](CreatePaymentRequest.md) |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_refund_request

> create_refund_request(id, create_refund_request_request)

Payment: Refund Request

A \"Refund Request\" requests that a payment be refunded manually. This can be used for payment methods that do not support refunds, such as konbini. To support non-refundable payment methods, a bank account must be specified so that we know where to send the funds. Since it is a manual process, the refund will be carried out at a later date, and there's a possibility of it being rejected.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.
create_refund_request_request = Komoju::CreateRefundRequestRequest.new({amount: 1000, customer_name: 'customer_name_example', bank_name: 'bank_name_example', branch_number: 'branch_number_example', account_type: 'normal', account_number: 37, include_payment_method_fee: false}) # CreateRefundRequestRequest | 

begin
  # Payment: Refund Request
  api_instance.create_refund_request(id, create_refund_request_request)
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->create_refund_request: #{e}"
end
```

#### Using the create_refund_request_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> create_refund_request_with_http_info(id, create_refund_request_request)

```ruby
begin
  # Payment: Refund Request
  data, status_code, headers = api_instance.create_refund_request_with_http_info(id, create_refund_request_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->create_refund_request_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |
| **create_refund_request_request** | [**CreateRefundRequestRequest**](CreateRefundRequestRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## finalize_payment

> <Payment> finalize_payment(id, finalize_payment_request)

Payment: Finalize



### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.
finalize_payment_request = Komoju::FinalizePaymentRequest.new({ac_type: 'tc', field55: 'field55_example', track2: 'track2_example'}) # FinalizePaymentRequest | 

begin
  # Payment: Finalize
  result = api_instance.finalize_payment(id, finalize_payment_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->finalize_payment: #{e}"
end
```

#### Using the finalize_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> finalize_payment_with_http_info(id, finalize_payment_request)

```ruby
begin
  # Payment: Finalize
  data, status_code, headers = api_instance.finalize_payment_with_http_info(id, finalize_payment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->finalize_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |
| **finalize_payment_request** | [**FinalizePaymentRequest**](FinalizePaymentRequest.md) |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_payment_methods

> <Array<AvailablePaymentMethod>> list_payment_methods

Payment Method: List

Lists available payment methods.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new

begin
  # Payment Method: List
  result = api_instance.list_payment_methods
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->list_payment_methods: #{e}"
end
```

#### Using the list_payment_methods_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AvailablePaymentMethod>>, Integer, Hash)> list_payment_methods_with_http_info

```ruby
begin
  # Payment Method: List
  data, status_code, headers = api_instance.list_payment_methods_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AvailablePaymentMethod>>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->list_payment_methods_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;AvailablePaymentMethod&gt;**](AvailablePaymentMethod.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_payments

> <PaymentList> list_payments(opts)

Payment: List

Retrieves a paginated list of payments. Pagination can be configured with `page` and `per_page` parameters.  Payments can be filtered by `currency`, `external_order_num`, and `status`.  A time range can be specified with `start_time`, and `end_time`.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  merchant_id: 'merchant_id_example', # String | 
  currency: Komoju::Currency::JPY, # Currency | 
  external_order_num: 'external_order_num_example', # String | A unique ID from your application used to track this payment.
  status: 'pending,captured' # String | The status of the payment. Can be a single status or comma-separated values.
}

begin
  # Payment: List
  result = api_instance.list_payments(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->list_payments: #{e}"
end
```

#### Using the list_payments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentList>, Integer, Hash)> list_payments_with_http_info(opts)

```ruby
begin
  # Payment: List
  data, status_code, headers = api_instance.list_payments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentList>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->list_payments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **merchant_id** | **String** |  | [optional] |
| **currency** | [**Currency**](.md) |  | [optional] |
| **external_order_num** | **String** | A unique ID from your application used to track this payment. | [optional] |
| **status** | **String** | The status of the payment. Can be a single status or comma-separated values. | [optional] |

### Return type

[**PaymentList**](PaymentList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## refund_payment

> <Payment> refund_payment(id, refund_payment_request)

Payment: Refund

Refunds an arbitrary amount of money from an existing payment. If no amount is specified, the whole payment is refunded.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.
refund_payment_request = Komoju::RefundPaymentRequest.new # RefundPaymentRequest | 

begin
  # Payment: Refund
  result = api_instance.refund_payment(id, refund_payment_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->refund_payment: #{e}"
end
```

#### Using the refund_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> refund_payment_with_http_info(id, refund_payment_request)

```ruby
begin
  # Payment: Refund
  data, status_code, headers = api_instance.refund_payment_with_http_info(id, refund_payment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->refund_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |
| **refund_payment_request** | [**RefundPaymentRequest**](RefundPaymentRequest.md) |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## show_payment

> <Payment> show_payment(id)

Payment: Show

Retrieves a single payment object by its `id`.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.

begin
  # Payment: Show
  result = api_instance.show_payment(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->show_payment: #{e}"
end
```

#### Using the show_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> show_payment_with_http_info(id)

```ruby
begin
  # Payment: Show
  data, status_code, headers = api_instance.show_payment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->show_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_payment

> <Payment> update_payment(id, update_payment_request)

Payment: Update

Updates a payment.  Only a payment's `description` and `metadata` can be changed.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::PaymentsApi.new
id = 'id_example' # String | A unique identifier for the payment.
update_payment_request = Komoju::UpdatePaymentRequest.new # UpdatePaymentRequest | 

begin
  # Payment: Update
  result = api_instance.update_payment(id, update_payment_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->update_payment: #{e}"
end
```

#### Using the update_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> update_payment_with_http_info(id, update_payment_request)

```ruby
begin
  # Payment: Update
  data, status_code, headers = api_instance.update_payment_with_http_info(id, update_payment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue Komoju::ApiError => e
  puts "Error when calling PaymentsApi->update_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the payment. |  |
| **update_payment_request** | [**UpdatePaymentRequest**](UpdatePaymentRequest.md) |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

