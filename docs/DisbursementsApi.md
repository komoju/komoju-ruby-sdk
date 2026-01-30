# Komoju::DisbursementsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_disbursement**](DisbursementsApi.md#cancel_disbursement) | **POST** /disbursements/{id}/cancel | Disbursement: Cancel |
| [**create_disbursement**](DisbursementsApi.md#create_disbursement) | **POST** /disbursements | Disbursement: Create |
| [**disbursement_report**](DisbursementsApi.md#disbursement_report) | **GET** /disbursements/report | Disbursement: Report |
| [**list_disbursements**](DisbursementsApi.md#list_disbursements) | **GET** /disbursements | Disbursement: List |
| [**show_disbursement**](DisbursementsApi.md#show_disbursement) | **GET** /disbursements/{id} | Disbursement: Show |


## cancel_disbursement

> <Disbursement> cancel_disbursement(id, cancel_disbursement_request)

Disbursement: Cancel

Cancels a disbursement.

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

api_instance = Komoju::DisbursementsApi.new
id = 'id_example' # String | 
cancel_disbursement_request = Komoju::CancelDisbursementRequest.new({cancel_reason: 'cancel_reason_example'}) # CancelDisbursementRequest | 

begin
  # Disbursement: Cancel
  result = api_instance.cancel_disbursement(id, cancel_disbursement_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->cancel_disbursement: #{e}"
end
```

#### Using the cancel_disbursement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Disbursement>, Integer, Hash)> cancel_disbursement_with_http_info(id, cancel_disbursement_request)

```ruby
begin
  # Disbursement: Cancel
  data, status_code, headers = api_instance.cancel_disbursement_with_http_info(id, cancel_disbursement_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Disbursement>
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->cancel_disbursement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **cancel_disbursement_request** | [**CancelDisbursementRequest**](CancelDisbursementRequest.md) |  |  |

### Return type

[**Disbursement**](Disbursement.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_disbursement

> <Disbursement> create_disbursement(create_disbursement_request)

Disbursement: Create

Creates a new disbursement.

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

api_instance = Komoju::DisbursementsApi.new
create_disbursement_request = Komoju::CreateDisbursementRequest.new({amount: 37, currency: Komoju::Currency::JPY, account_number: 'account_number_example', account_type: 'ordinary', account_name_kana: 'account_name_kana_example', bank_code: 'bank_code_example', branch_code: 'branch_code_example'}) # CreateDisbursementRequest | 

begin
  # Disbursement: Create
  result = api_instance.create_disbursement(create_disbursement_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->create_disbursement: #{e}"
end
```

#### Using the create_disbursement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Disbursement>, Integer, Hash)> create_disbursement_with_http_info(create_disbursement_request)

```ruby
begin
  # Disbursement: Create
  data, status_code, headers = api_instance.create_disbursement_with_http_info(create_disbursement_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Disbursement>
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->create_disbursement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_disbursement_request** | [**CreateDisbursementRequest**](CreateDisbursementRequest.md) |  |  |

### Return type

[**Disbursement**](Disbursement.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## disbursement_report

> disbursement_report(start_time, end_time, currency, status)

Disbursement: Report

View disbursements in CSV format.

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

api_instance = Komoju::DisbursementsApi.new
start_time = Time.parse('2013-10-20T19:20:30+01:00') # Time | 
end_time = Time.parse('2013-10-20T19:20:30+01:00') # Time | 
currency = Komoju::Currency::JPY # Currency | 
status = Komoju::DisbursementStatus::PENDING # DisbursementStatus | 

begin
  # Disbursement: Report
  api_instance.disbursement_report(start_time, end_time, currency, status)
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->disbursement_report: #{e}"
end
```

#### Using the disbursement_report_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> disbursement_report_with_http_info(start_time, end_time, currency, status)

```ruby
begin
  # Disbursement: Report
  data, status_code, headers = api_instance.disbursement_report_with_http_info(start_time, end_time, currency, status)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->disbursement_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** |  |  |
| **end_time** | **Time** |  |  |
| **currency** | [**Currency**](.md) |  |  |
| **status** | [**DisbursementStatus**](.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_disbursements

> <DisbursementList> list_disbursements(opts)

Disbursement: List

Lists disbursements.

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

api_instance = Komoju::DisbursementsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  currency: Komoju::Currency::JPY # Currency | 
}

begin
  # Disbursement: List
  result = api_instance.list_disbursements(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->list_disbursements: #{e}"
end
```

#### Using the list_disbursements_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DisbursementList>, Integer, Hash)> list_disbursements_with_http_info(opts)

```ruby
begin
  # Disbursement: List
  data, status_code, headers = api_instance.list_disbursements_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DisbursementList>
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->list_disbursements_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **currency** | [**Currency**](.md) |  | [optional] |

### Return type

[**DisbursementList**](DisbursementList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_disbursement

> <Disbursement> show_disbursement(id)

Disbursement: Show

Retrieves a disbursement.

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

api_instance = Komoju::DisbursementsApi.new
id = 'id_example' # String | 

begin
  # Disbursement: Show
  result = api_instance.show_disbursement(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->show_disbursement: #{e}"
end
```

#### Using the show_disbursement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Disbursement>, Integer, Hash)> show_disbursement_with_http_info(id)

```ruby
begin
  # Disbursement: Show
  data, status_code, headers = api_instance.show_disbursement_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Disbursement>
rescue Komoju::ApiError => e
  puts "Error when calling DisbursementsApi->show_disbursement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Disbursement**](Disbursement.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

