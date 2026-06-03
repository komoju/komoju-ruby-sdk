# Komoju::SubscriptionsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_customer**](SubscriptionsApi.md#create_customer) | **POST** /customers | Customer: Create |
| [**create_subscription**](SubscriptionsApi.md#create_subscription) | **POST** /subscriptions | Subscription: Create |
| [**delete_customer**](SubscriptionsApi.md#delete_customer) | **DELETE** /customers/{id} | Customer: Destroy |
| [**delete_subscription**](SubscriptionsApi.md#delete_subscription) | **DELETE** /subscriptions/{id} | Subscription: Destroy |
| [**list_customers**](SubscriptionsApi.md#list_customers) | **GET** /customers | Customer: List |
| [**list_subscriptions**](SubscriptionsApi.md#list_subscriptions) | **GET** /subscriptions | Subscription: List |
| [**show_customer**](SubscriptionsApi.md#show_customer) | **GET** /customers/{id} | Customer: Show |
| [**show_subscription**](SubscriptionsApi.md#show_subscription) | **GET** /subscriptions/{id} | Subscription: Show |
| [**update_customer**](SubscriptionsApi.md#update_customer) | **PATCH** /customers/{id} | Customer: Update |

## Request Models

- [**CreateCustomerRequest**](CreateCustomerRequest.md) — used by `create_customer`
- [**CreateSubscriptionRequest**](CreateSubscriptionRequest.md) — used by `create_subscription`
- [**UpdateCustomerRequest**](UpdateCustomerRequest.md) — used by `update_customer`


## create_customer

> <Customer> create_customer(create_customer_request)

Customer: Create

Creates a new customer with the specified `payment_details`. Customer payment details are stored in a secure, PCI DSS-compliant way.  Once you have a customer, you may specify the customer's `id` instead of `payment_details` when creating a payment.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
create_customer_request = Komoju::CreateCustomerRequest.new # CreateCustomerRequest | 

begin
  # Customer: Create
  result = api_instance.create_customer(create_customer_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->create_customer: #{e}"
end
```

#### Using the create_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> create_customer_with_http_info(create_customer_request)

```ruby
begin
  # Customer: Create
  data, status_code, headers = api_instance.create_customer_with_http_info(create_customer_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->create_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_customer_request** | [**CreateCustomerRequest**](CreateCustomerRequest.md) |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_subscription

> <Subscription> create_subscription(create_subscription_request)

Subscription: Create

Create a new subscription. A subscription represents a recurring payment. Recurring payments may be on a `weekly`, `monthly`, or `yearly` basis, specified by the period parameter.  In order to create a subscription, a customer ID must be supplied. The customer object contains saved payment info, which is regularly charged by the subscription.  A subscription can't be modified once it's created. To change a subscription, you must delete it and create a new one.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
create_subscription_request = Komoju::CreateSubscriptionRequest.new({customer: 'customer_example', amount: 37, currency: Komoju::Currency::JPY, period: Komoju::SubscriptionPeriod::WEEKLY}) # CreateSubscriptionRequest | 

begin
  # Subscription: Create
  result = api_instance.create_subscription(create_subscription_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->create_subscription: #{e}"
end
```

#### Using the create_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Subscription>, Integer, Hash)> create_subscription_with_http_info(create_subscription_request)

```ruby
begin
  # Subscription: Create
  data, status_code, headers = api_instance.create_subscription_with_http_info(create_subscription_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Subscription>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->create_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_subscription_request** | [**CreateSubscriptionRequest**](CreateSubscriptionRequest.md) |  |  |

### Return type

[**Subscription**](Subscription.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_customer

> <Customer> delete_customer(id)

Customer: Destroy

Deletes the customer with the given `id`. This complete erases the stored payment details from our database.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
id = 'id_example' # String | 

begin
  # Customer: Destroy
  result = api_instance.delete_customer(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->delete_customer: #{e}"
end
```

#### Using the delete_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> delete_customer_with_http_info(id)

```ruby
begin
  # Customer: Destroy
  data, status_code, headers = api_instance.delete_customer_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->delete_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_subscription

> <Subscription> delete_subscription(id)

Subscription: Destroy

Delete a subscription. Once deleted, the subscription's regular payments will stop.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
id = 'id_example' # String | 

begin
  # Subscription: Destroy
  result = api_instance.delete_subscription(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->delete_subscription: #{e}"
end
```

#### Using the delete_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Subscription>, Integer, Hash)> delete_subscription_with_http_info(id)

```ruby
begin
  # Subscription: Destroy
  data, status_code, headers = api_instance.delete_subscription_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Subscription>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->delete_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Subscription**](Subscription.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_customers

> <CustomerList> list_customers(opts)

Customer: List

Retrieves a paginated list of all previously-registered customers.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  expiration: 'expiration_example' # String | The expiration of the customer's credit card in MMYY format.
}

begin
  # Customer: List
  result = api_instance.list_customers(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->list_customers: #{e}"
end
```

#### Using the list_customers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerList>, Integer, Hash)> list_customers_with_http_info(opts)

```ruby
begin
  # Customer: List
  data, status_code, headers = api_instance.list_customers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerList>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->list_customers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **expiration** | **String** | The expiration of the customer&#39;s credit card in MMYY format. | [optional] |

### Return type

[**CustomerList**](CustomerList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_subscriptions

> <SubscriptionList> list_subscriptions(opts)

Subscription: List

List existing subscriptions.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56 # Integer | Page number to query for.
}

begin
  # Subscription: List
  result = api_instance.list_subscriptions(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->list_subscriptions: #{e}"
end
```

#### Using the list_subscriptions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionList>, Integer, Hash)> list_subscriptions_with_http_info(opts)

```ruby
begin
  # Subscription: List
  data, status_code, headers = api_instance.list_subscriptions_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionList>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->list_subscriptions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |

### Return type

[**SubscriptionList**](SubscriptionList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_customer

> <Customer> show_customer(id)

Customer: Show

Retrieves customer personal information.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
id = 'id_example' # String | 

begin
  # Customer: Show
  result = api_instance.show_customer(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->show_customer: #{e}"
end
```

#### Using the show_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> show_customer_with_http_info(id)

```ruby
begin
  # Customer: Show
  data, status_code, headers = api_instance.show_customer_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->show_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_subscription

> <Subscription> show_subscription(id)

Subscription: Show

Show an existing subscription, including its customer and scrubbed payment details.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
id = 'id_example' # String | 

begin
  # Subscription: Show
  result = api_instance.show_subscription(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->show_subscription: #{e}"
end
```

#### Using the show_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Subscription>, Integer, Hash)> show_subscription_with_http_info(id)

```ruby
begin
  # Subscription: Show
  data, status_code, headers = api_instance.show_subscription_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Subscription>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->show_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Subscription**](Subscription.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_customer

> <Customer> update_customer(id, update_customer_request)

Customer: Update

Updates the customer with the given `id`. A new set of `payment_details` may be specified.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SubscriptionsApi.new
id = 'id_example' # String | 
update_customer_request = Komoju::UpdateCustomerRequest.new # UpdateCustomerRequest | 

begin
  # Customer: Update
  result = api_instance.update_customer(id, update_customer_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->update_customer: #{e}"
end
```

#### Using the update_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> update_customer_with_http_info(id, update_customer_request)

```ruby
begin
  # Customer: Update
  data, status_code, headers = api_instance.update_customer_with_http_info(id, update_customer_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue Komoju::ApiError => e
  puts "Error when calling SubscriptionsApi->update_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **update_customer_request** | [**UpdateCustomerRequest**](UpdateCustomerRequest.md) |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

