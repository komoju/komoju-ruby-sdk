# Komoju::SettlementsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_settlements**](SettlementsApi.md#list_settlements) | **GET** /settlements | Settlement: Index |
| [**show_settlement**](SettlementsApi.md#show_settlement) | **GET** /settlements/{id} | Settlement: Show |
| [**show_settlement_csv**](SettlementsApi.md#show_settlement_csv) | **GET** /settlements/{id}/csv | Settlement: CSV |
| [**show_settlement_pdf**](SettlementsApi.md#show_settlement_pdf) | **GET** /settlements/{id}/pdf | Settlement: PDF |
| [**show_settlement_xls**](SettlementsApi.md#show_settlement_xls) | **GET** /settlements/{id}/xls | Settlement: XLS |
| [**show_transaction**](SettlementsApi.md#show_transaction) | **GET** /balances/{currency}/transactions/{transaction_uuid} | Balance: Transaction |


## list_settlements

> <SettlementList> list_settlements(opts)

Settlement: Index



### Examples

```ruby
require 'time'
require 'komoju-ruby-client'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::SettlementsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records before after this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56 # Integer | Page number to query for.
}

begin
  # Settlement: Index
  result = api_instance.list_settlements(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->list_settlements: #{e}"
end
```

#### Using the list_settlements_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SettlementList>, Integer, Hash)> list_settlements_with_http_info(opts)

```ruby
begin
  # Settlement: Index
  data, status_code, headers = api_instance.list_settlements_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SettlementList>
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->list_settlements_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records before after this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |

### Return type

[**SettlementList**](SettlementList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_settlement

> <Settlement> show_settlement(id)

Settlement: Show



### Examples

```ruby
require 'time'
require 'komoju-ruby-client'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::SettlementsApi.new
id = 'id_example' # String | 

begin
  # Settlement: Show
  result = api_instance.show_settlement(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement: #{e}"
end
```

#### Using the show_settlement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Settlement>, Integer, Hash)> show_settlement_with_http_info(id)

```ruby
begin
  # Settlement: Show
  data, status_code, headers = api_instance.show_settlement_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Settlement>
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Settlement**](Settlement.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_settlement_csv

> show_settlement_csv(id)

Settlement: CSV

Retrieves the settlement in CSV format.

### Examples

```ruby
require 'time'
require 'komoju-ruby-client'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::SettlementsApi.new
id = 'id_example' # String | 

begin
  # Settlement: CSV
  api_instance.show_settlement_csv(id)
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_csv: #{e}"
end
```

#### Using the show_settlement_csv_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> show_settlement_csv_with_http_info(id)

```ruby
begin
  # Settlement: CSV
  data, status_code, headers = api_instance.show_settlement_csv_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_csv_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## show_settlement_pdf

> show_settlement_pdf(id)

Settlement: PDF

Retrieves the settlement in PDF format.

### Examples

```ruby
require 'time'
require 'komoju-ruby-client'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::SettlementsApi.new
id = 'id_example' # String | 

begin
  # Settlement: PDF
  api_instance.show_settlement_pdf(id)
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_pdf: #{e}"
end
```

#### Using the show_settlement_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> show_settlement_pdf_with_http_info(id)

```ruby
begin
  # Settlement: PDF
  data, status_code, headers = api_instance.show_settlement_pdf_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## show_settlement_xls

> show_settlement_xls(id)

Settlement: XLS

Retrieves the settlement in XLS format.

### Examples

```ruby
require 'time'
require 'komoju-ruby-client'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::SettlementsApi.new
id = 'id_example' # String | 

begin
  # Settlement: XLS
  api_instance.show_settlement_xls(id)
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_xls: #{e}"
end
```

#### Using the show_settlement_xls_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> show_settlement_xls_with_http_info(id)

```ruby
begin
  # Settlement: XLS
  data, status_code, headers = api_instance.show_settlement_xls_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_xls_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## show_transaction

> <Transaction> show_transaction(currency, transaction_uuid)

Balance: Transaction



### Examples

```ruby
require 'time'
require 'komoju-ruby-client'
# setup authorization
Komoju.configure do |config|
  # Configure HTTP basic authorization: api_key
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = Komoju::SettlementsApi.new
currency = Komoju::Currency::JPY # Currency | 
transaction_uuid = 'transaction_uuid_example' # String | 

begin
  # Balance: Transaction
  result = api_instance.show_transaction(currency, transaction_uuid)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_transaction: #{e}"
end
```

#### Using the show_transaction_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Transaction>, Integer, Hash)> show_transaction_with_http_info(currency, transaction_uuid)

```ruby
begin
  # Balance: Transaction
  data, status_code, headers = api_instance.show_transaction_with_http_info(currency, transaction_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Transaction>
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_transaction_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](.md) |  |  |
| **transaction_uuid** | **String** |  |  |

### Return type

[**Transaction**](Transaction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

