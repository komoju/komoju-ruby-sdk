# Komoju::SettlementsApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**balance_transactions**](SettlementsApi.md#balance_transactions) | **GET** /balances/{currency}/transactions | Balance: Transactions |
| [**list_settlements**](SettlementsApi.md#list_settlements) | **GET** /settlements | Settlement: Index |
| [**show_balance**](SettlementsApi.md#show_balance) | **GET** /balances/{currency} | Balance: Show |
| [**show_settlement**](SettlementsApi.md#show_settlement) | **GET** /settlements/{id} | Settlement: Show |
| [**show_settlement_csv**](SettlementsApi.md#show_settlement_csv) | **GET** /settlements/{id}/csv | Settlement: CSV |
| [**show_settlement_pdf**](SettlementsApi.md#show_settlement_pdf) | **GET** /settlements/{id}/pdf | Settlement: PDF |
| [**show_settlement_xls**](SettlementsApi.md#show_settlement_xls) | **GET** /settlements/{id}/xls | Settlement: XLS |
| [**show_transaction**](SettlementsApi.md#show_transaction) | **GET** /balances/{currency}/transactions/{transaction_uuid} | Balance: Transaction |

## Request Models



## balance_transactions

> <BalanceTransactionList> balance_transactions(currency, opts)

Balance: Transactions

Given a currency, view the ledger transactions of the currently authenticated merchant. Will split ledger transactions into line items when appropriate.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SettlementsApi.new
currency = Komoju::Currency::JPY # Currency | 
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  type: 'type_example' # String | 
}

begin
  # Balance: Transactions
  result = api_instance.balance_transactions(currency, opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->balance_transactions: #{e}"
end
```

#### Using the balance_transactions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BalanceTransactionList>, Integer, Hash)> balance_transactions_with_http_info(currency, opts)

```ruby
begin
  # Balance: Transactions
  data, status_code, headers = api_instance.balance_transactions_with_http_info(currency, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BalanceTransactionList>
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->balance_transactions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](.md) |  |  |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **type** | **String** |  | [optional] |

### Return type

[**BalanceTransactionList**](BalanceTransactionList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_settlements

> <SettlementList> list_settlements(opts)

Settlement: Index

Retrieves a paginated list of settlements from most-recent to least-recent. Pagination can be configured with `page` and `per_page` parameters.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SettlementsApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
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
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |

### Return type

[**SettlementList**](SettlementList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_balance

> <ShowBalance200Response> show_balance(currency)

Balance: Show

Given a currency, view the unsettled balance of the currently authenticated merchant.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SettlementsApi.new
currency = Komoju::Currency::JPY # Currency | 

begin
  # Balance: Show
  result = api_instance.show_balance(currency)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_balance: #{e}"
end
```

#### Using the show_balance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShowBalance200Response>, Integer, Hash)> show_balance_with_http_info(currency)

```ruby
begin
  # Balance: Show
  data, status_code, headers = api_instance.show_balance_with_http_info(currency)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShowBalance200Response>
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_balance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](.md) |  |  |

### Return type

[**ShowBalance200Response**](ShowBalance200Response.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_settlement

> <SettlementShow> show_settlement(id)

Settlement: Show

Retrieves a single settlement by its `id`, including a breakdown of payments, refunds, fees, corrections, and disbursements.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array(<SettlementShow>, Integer, Hash)> show_settlement_with_http_info(id)

```ruby
begin
  # Settlement: Show
  data, status_code, headers = api_instance.show_settlement_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SettlementShow>
rescue Komoju::ApiError => e
  puts "Error when calling SettlementsApi->show_settlement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**SettlementShow**](SettlementShow.md)

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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array<Transaction>> show_transaction(currency, transaction_uuid)

Balance: Transaction

Retrieves a single ledger transaction by its UUID for the given currency. Will return one entry per line item of the transaction.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array(<Array<Transaction>>, Integer, Hash)> show_transaction_with_http_info(currency, transaction_uuid)

```ruby
begin
  # Balance: Transaction
  data, status_code, headers = api_instance.show_transaction_with_http_info(currency, transaction_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Transaction>>
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

[**Array&lt;Transaction&gt;**](Transaction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

