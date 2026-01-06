# Komoju::PlatformModelApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**balance_transfer**](PlatformModelApi.md#balance_transfer) | **POST** /balances/{currency}/transfer | Balance: Transfer |
| [**create_file**](PlatformModelApi.md#create_file) | **POST** /merchants/{merchant_id}/files | File: Create |
| [**create_merchant**](PlatformModelApi.md#create_merchant) | **POST** /merchants | Merchant: Create |
| [**create_merchant_balance_transfer**](PlatformModelApi.md#create_merchant_balance_transfer) | **POST** /balances/{merchant_id}/balances/{currency}/transfer | Balance: Transfer |
| [**edit_merchant_balance_settings**](PlatformModelApi.md#edit_merchant_balance_settings) | **PATCH** /balances/{merchant_id}/balances/{currency}/settings | Balances: Edit Settings |
| [**list_live_application_payment_methods**](PlatformModelApi.md#list_live_application_payment_methods) | **GET** /live_application/{merchant_id}/payment_methods | Live Application: Payment Methods |
| [**list_merchants**](PlatformModelApi.md#list_merchants) | **GET** /merchants | Merchant: List |
| [**list_submerchant_payments**](PlatformModelApi.md#list_submerchant_payments) | **GET** /merchants/{merchant_id}/payments | Payment: List for Merchant |
| [**list_submerchant_settlements**](PlatformModelApi.md#list_submerchant_settlements) | **GET** /merchants/{merchant_id}/settlements | Settlement: List |
| [**merchant_balance_transactions**](PlatformModelApi.md#merchant_balance_transactions) | **GET** /balances/{merchant_id}/balances/{currency}/transactions | Balance: Transactions |
| [**show_file**](PlatformModelApi.md#show_file) | **GET** /merchants/{merchant_id}/files/{id} | File: Show |
| [**show_live_application**](PlatformModelApi.md#show_live_application) | **GET** /live_application/{merchant_id} | Live Application: Show |
| [**show_live_application_payment_method**](PlatformModelApi.md#show_live_application_payment_method) | **GET** /live_application/{merchant_id}/payment_methods/{payment_method} | Live Application: Show Payment Method |
| [**show_merchant**](PlatformModelApi.md#show_merchant) | **GET** /merchants/{id} | Merchant: Show |
| [**show_merchant_balance**](PlatformModelApi.md#show_merchant_balance) | **GET** /balances/{merchant_id}/balances/{currency} | Balance: Show |
| [**show_merchant_balance_settings**](PlatformModelApi.md#show_merchant_balance_settings) | **GET** /balances/{merchant_id}/balances/{currency}/settings | Balance: Show Settings |
| [**show_merchant_balance_transaction**](PlatformModelApi.md#show_merchant_balance_transaction) | **GET** /balances/{merchant_id}/balances/{currency}/transactions/{transaction_uuid} | Balance: Transaction |
| [**show_submerchant_settlement**](PlatformModelApi.md#show_submerchant_settlement) | **GET** /merchants/{merchant_id}/settlements/{id} | Settlement: Show |
| [**simulate_live_application_payment_method_status**](PlatformModelApi.md#simulate_live_application_payment_method_status) | **PATCH** /live_application/{merchant_id}/payment_methods/{payment_method}/simulate_status | Live Application: Simulate Payment Method Status |
| [**simulate_live_application_status**](PlatformModelApi.md#simulate_live_application_status) | **PATCH** /live_application/{merchant_id}/simulate_status | Live Application: Simulate Status |
| [**submerchant_settlement_csv**](PlatformModelApi.md#submerchant_settlement_csv) | **GET** /merchants/{merchant_id}/settlements/{id}/csv | Settlement: CSV |
| [**submerchant_settlement_pdf**](PlatformModelApi.md#submerchant_settlement_pdf) | **GET** /merchants/{merchant_id}/settlements/{id}/pdf | Settlement: PDF |
| [**submerchant_settlement_xls**](PlatformModelApi.md#submerchant_settlement_xls) | **GET** /merchants/{merchant_id}/settlements/{id}/xls | Settlement: XLS |
| [**update_live_application**](PlatformModelApi.md#update_live_application) | **PATCH** /live_application/{merchant_id} | Live Application: Update |
| [**update_live_application_payment_method**](PlatformModelApi.md#update_live_application_payment_method) | **PATCH** /live_application/{merchant_id}/payment_methods/{payment_method} | Live Application: Update Payment Method |
| [**update_merchant**](PlatformModelApi.md#update_merchant) | **PATCH** /merchants/{id} | Merchant: Update |


## balance_transfer

> <Transfer> balance_transfer(currency, balance_transfer_request)

Balance: Transfer



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

api_instance = Komoju::PlatformModelApi.new
currency = Komoju::Currency::JPY # Currency | 
balance_transfer_request = Komoju::BalanceTransferRequest.new({amount: 37, to: 'to_example'}) # BalanceTransferRequest | 

begin
  # Balance: Transfer
  result = api_instance.balance_transfer(currency, balance_transfer_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->balance_transfer: #{e}"
end
```

#### Using the balance_transfer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Transfer>, Integer, Hash)> balance_transfer_with_http_info(currency, balance_transfer_request)

```ruby
begin
  # Balance: Transfer
  data, status_code, headers = api_instance.balance_transfer_with_http_info(currency, balance_transfer_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Transfer>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->balance_transfer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](.md) |  |  |
| **balance_transfer_request** | [**BalanceTransferRequest**](BalanceTransferRequest.md) |  |  |

### Return type

[**Transfer**](Transfer.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_file

> <MerchantFile> create_file(merchant_id, create_file_request)

File: Create

Creates a new file for the current merchant.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
create_file_request = Komoju::CreateFileRequest.new({merchant_id: 'merchant_id_example'}) # CreateFileRequest | 

begin
  # File: Create
  result = api_instance.create_file(merchant_id, create_file_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_file: #{e}"
end
```

#### Using the create_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MerchantFile>, Integer, Hash)> create_file_with_http_info(merchant_id, create_file_request)

```ruby
begin
  # File: Create
  data, status_code, headers = api_instance.create_file_with_http_info(merchant_id, create_file_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MerchantFile>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **create_file_request** | [**CreateFileRequest**](CreateFileRequest.md) |  |  |

### Return type

[**MerchantFile**](MerchantFile.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_merchant

> create_merchant(create_merchant_request)

Merchant: Create

Creates a new merchant.

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

api_instance = Komoju::PlatformModelApi.new
create_merchant_request = Komoju::CreateMerchantRequest.new({name: 'name_example', platform_role: Komoju::MerchantRole::SELLER}) # CreateMerchantRequest | 

begin
  # Merchant: Create
  api_instance.create_merchant(create_merchant_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant: #{e}"
end
```

#### Using the create_merchant_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> create_merchant_with_http_info(create_merchant_request)

```ruby
begin
  # Merchant: Create
  data, status_code, headers = api_instance.create_merchant_with_http_info(create_merchant_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_merchant_request** | [**CreateMerchantRequest**](CreateMerchantRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## create_merchant_balance_transfer

> create_merchant_balance_transfer(merchant_id, currency, create_merchant_balance_transfer_request)

Balance: Transfer

Creates a balance transfer between associated merchants for a given `amount` and `currency`.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 
create_merchant_balance_transfer_request = Komoju::CreateMerchantBalanceTransferRequest.new({currency: Komoju::Currency::JPY, to: 'to_example', amount: 37}) # CreateMerchantBalanceTransferRequest | 

begin
  # Balance: Transfer
  api_instance.create_merchant_balance_transfer(merchant_id, currency, create_merchant_balance_transfer_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant_balance_transfer: #{e}"
end
```

#### Using the create_merchant_balance_transfer_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> create_merchant_balance_transfer_with_http_info(merchant_id, currency, create_merchant_balance_transfer_request)

```ruby
begin
  # Balance: Transfer
  data, status_code, headers = api_instance.create_merchant_balance_transfer_with_http_info(merchant_id, currency, create_merchant_balance_transfer_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant_balance_transfer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **currency** | [**Currency**](.md) |  |  |
| **create_merchant_balance_transfer_request** | [**CreateMerchantBalanceTransferRequest**](CreateMerchantBalanceTransferRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## edit_merchant_balance_settings

> edit_merchant_balance_settings(merchant_id, currency, edit_merchant_balance_settings_request)

Balances: Edit Settings

Given a currency, edit the payout settings of the currently authenticated merchant or one of its sub-merchants.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 
edit_merchant_balance_settings_request = Komoju::EditMerchantBalanceSettingsRequest.new({currency: Komoju::Currency::JPY, frequency: Komoju::SettlementFrequency::WEEKLY, settlement_minimum_amount: 37}) # EditMerchantBalanceSettingsRequest | 

begin
  # Balances: Edit Settings
  api_instance.edit_merchant_balance_settings(merchant_id, currency, edit_merchant_balance_settings_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->edit_merchant_balance_settings: #{e}"
end
```

#### Using the edit_merchant_balance_settings_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> edit_merchant_balance_settings_with_http_info(merchant_id, currency, edit_merchant_balance_settings_request)

```ruby
begin
  # Balances: Edit Settings
  data, status_code, headers = api_instance.edit_merchant_balance_settings_with_http_info(merchant_id, currency, edit_merchant_balance_settings_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->edit_merchant_balance_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **currency** | [**Currency**](.md) |  |  |
| **edit_merchant_balance_settings_request** | [**EditMerchantBalanceSettingsRequest**](EditMerchantBalanceSettingsRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## list_live_application_payment_methods

> list_live_application_payment_methods(merchant_id, opts)

Live Application: Payment Methods

List submitted/unsubmitted payment methods

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
opts = {
  locale: Komoju::Locale::JA # Locale | 
}

begin
  # Live Application: Payment Methods
  api_instance.list_live_application_payment_methods(merchant_id, opts)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_live_application_payment_methods: #{e}"
end
```

#### Using the list_live_application_payment_methods_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_live_application_payment_methods_with_http_info(merchant_id, opts)

```ruby
begin
  # Live Application: Payment Methods
  data, status_code, headers = api_instance.list_live_application_payment_methods_with_http_info(merchant_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_live_application_payment_methods_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **locale** | [**Locale**](.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_merchants

> list_merchants(opts)

Merchant: List

Sub-merchants List

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

api_instance = Komoju::PlatformModelApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records before after this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  live: true, # Boolean | 
  platform_role: Komoju::MerchantRole::SELLER, # MerchantRole | 
  application_status: 'application_status_example', # String | 
  payments_enabled: true, # Boolean | 
  payouts_enabled: true # Boolean | 
}

begin
  # Merchant: List
  api_instance.list_merchants(opts)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_merchants: #{e}"
end
```

#### Using the list_merchants_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_merchants_with_http_info(opts)

```ruby
begin
  # Merchant: List
  data, status_code, headers = api_instance.list_merchants_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_merchants_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records before after this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **live** | **Boolean** |  | [optional] |
| **platform_role** | [**MerchantRole**](.md) |  | [optional] |
| **application_status** | **String** |  | [optional] |
| **payments_enabled** | **Boolean** |  | [optional] |
| **payouts_enabled** | **Boolean** |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_submerchant_payments

> list_submerchant_payments(merchant_id, opts)

Payment: List for Merchant

Retrieves a paginated list of payments. Pagination can be configured with `page` and `per_page` parameters.  Payments can be filtered by `currency`, `external_order_num`, and `status`.  A time range can be specified with `start_time`, and `end_time`.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records before after this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  currency: Komoju::Currency::JPY, # Currency | 
  external_order_num: 'external_order_num_example', # String | 
  status: Komoju::PaymentStatus::PENDING # PaymentStatus | 
}

begin
  # Payment: List for Merchant
  api_instance.list_submerchant_payments(merchant_id, opts)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_submerchant_payments: #{e}"
end
```

#### Using the list_submerchant_payments_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_submerchant_payments_with_http_info(merchant_id, opts)

```ruby
begin
  # Payment: List for Merchant
  data, status_code, headers = api_instance.list_submerchant_payments_with_http_info(merchant_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_submerchant_payments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records before after this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **currency** | [**Currency**](.md) |  | [optional] |
| **external_order_num** | **String** |  | [optional] |
| **status** | [**PaymentStatus**](.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_submerchant_settlements

> <SettlementList> list_submerchant_settlements(merchant_id)

Settlement: List

Lists out past settlements from most-recent to least-recent.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 

begin
  # Settlement: List
  result = api_instance.list_submerchant_settlements(merchant_id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_submerchant_settlements: #{e}"
end
```

#### Using the list_submerchant_settlements_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SettlementList>, Integer, Hash)> list_submerchant_settlements_with_http_info(merchant_id)

```ruby
begin
  # Settlement: List
  data, status_code, headers = api_instance.list_submerchant_settlements_with_http_info(merchant_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SettlementList>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_submerchant_settlements_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |

### Return type

[**SettlementList**](SettlementList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## merchant_balance_transactions

> <BalanceTransactionList> merchant_balance_transactions(merchant_id, currency, opts)

Balance: Transactions

Given a currency, view the ledger transactions of the currently authenticated merchant or one of its sub-merchants.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records before after this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  type: 'type_example' # String | 
}

begin
  # Balance: Transactions
  result = api_instance.merchant_balance_transactions(merchant_id, currency, opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->merchant_balance_transactions: #{e}"
end
```

#### Using the merchant_balance_transactions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BalanceTransactionList>, Integer, Hash)> merchant_balance_transactions_with_http_info(merchant_id, currency, opts)

```ruby
begin
  # Balance: Transactions
  data, status_code, headers = api_instance.merchant_balance_transactions_with_http_info(merchant_id, currency, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BalanceTransactionList>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->merchant_balance_transactions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **currency** | [**Currency**](.md) |  |  |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records before after this time. | [optional] |
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


## show_file

> <MerchantFile> show_file(merchant_id, id)

File: Show

Retrieves an existing file of the current merchant.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
id = 'id_example' # String | 

begin
  # File: Show
  result = api_instance.show_file(merchant_id, id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_file: #{e}"
end
```

#### Using the show_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MerchantFile>, Integer, Hash)> show_file_with_http_info(merchant_id, id)

```ruby
begin
  # File: Show
  data, status_code, headers = api_instance.show_file_with_http_info(merchant_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MerchantFile>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **id** | **String** |  |  |

### Return type

[**MerchantFile**](MerchantFile.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_live_application

> <LiveApplication> show_live_application(merchant_id, opts)

Live Application: Show

Shows the live application status of the applicant merchant

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
opts = {
  locale: Komoju::Locale::JA # Locale | 
}

begin
  # Live Application: Show
  result = api_instance.show_live_application(merchant_id, opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_live_application: #{e}"
end
```

#### Using the show_live_application_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LiveApplication>, Integer, Hash)> show_live_application_with_http_info(merchant_id, opts)

```ruby
begin
  # Live Application: Show
  data, status_code, headers = api_instance.show_live_application_with_http_info(merchant_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LiveApplication>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_live_application_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **locale** | [**Locale**](.md) |  | [optional] |

### Return type

[**LiveApplication**](LiveApplication.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_live_application_payment_method

> show_live_application_payment_method(merchant_id, payment_method, opts)

Live Application: Show Payment Method

Shows the payment method status of the applicant merchant

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
payment_method = 'payment_method_example' # String | 
opts = {
  locale: Komoju::Locale::JA # Locale | 
}

begin
  # Live Application: Show Payment Method
  api_instance.show_live_application_payment_method(merchant_id, payment_method, opts)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_live_application_payment_method: #{e}"
end
```

#### Using the show_live_application_payment_method_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> show_live_application_payment_method_with_http_info(merchant_id, payment_method, opts)

```ruby
begin
  # Live Application: Show Payment Method
  data, status_code, headers = api_instance.show_live_application_payment_method_with_http_info(merchant_id, payment_method, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_live_application_payment_method_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **payment_method** | **String** |  |  |
| **locale** | [**Locale**](.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## show_merchant

> show_merchant(id)

Merchant: Show

Sub-merchant Detail

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

api_instance = Komoju::PlatformModelApi.new
id = 'id_example' # String | 

begin
  # Merchant: Show
  api_instance.show_merchant(id)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant: #{e}"
end
```

#### Using the show_merchant_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> show_merchant_with_http_info(id)

```ruby
begin
  # Merchant: Show
  data, status_code, headers = api_instance.show_merchant_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_with_http_info: #{e}"
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


## show_merchant_balance

> <Balance> show_merchant_balance(merchant_id, currency)

Balance: Show

Given a currency, view the unsettled balance of the currently authenticated merchant or one of its sub-merchants.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 

begin
  # Balance: Show
  result = api_instance.show_merchant_balance(merchant_id, currency)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_balance: #{e}"
end
```

#### Using the show_merchant_balance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Balance>, Integer, Hash)> show_merchant_balance_with_http_info(merchant_id, currency)

```ruby
begin
  # Balance: Show
  data, status_code, headers = api_instance.show_merchant_balance_with_http_info(merchant_id, currency)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Balance>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_balance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **currency** | [**Currency**](.md) |  |  |

### Return type

[**Balance**](Balance.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_merchant_balance_settings

> <BalanceSettings> show_merchant_balance_settings(merchant_id, currency)

Balance: Show Settings

Given a currency, view the payout settings of the currently authenticated merchant or one of its sub-merchants.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 

begin
  # Balance: Show Settings
  result = api_instance.show_merchant_balance_settings(merchant_id, currency)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_balance_settings: #{e}"
end
```

#### Using the show_merchant_balance_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BalanceSettings>, Integer, Hash)> show_merchant_balance_settings_with_http_info(merchant_id, currency)

```ruby
begin
  # Balance: Show Settings
  data, status_code, headers = api_instance.show_merchant_balance_settings_with_http_info(merchant_id, currency)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BalanceSettings>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_balance_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **currency** | [**Currency**](.md) |  |  |

### Return type

[**BalanceSettings**](BalanceSettings.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_merchant_balance_transaction

> <Transaction> show_merchant_balance_transaction(merchant_id, currency, transaction_uuid)

Balance: Transaction

Given a currency and a transaction UUID, view the corresponding ledger transaction of the currently authenticated merchant or one of its sub-merchants.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 
transaction_uuid = 'transaction_uuid_example' # String | 

begin
  # Balance: Transaction
  result = api_instance.show_merchant_balance_transaction(merchant_id, currency, transaction_uuid)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_balance_transaction: #{e}"
end
```

#### Using the show_merchant_balance_transaction_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Transaction>, Integer, Hash)> show_merchant_balance_transaction_with_http_info(merchant_id, currency, transaction_uuid)

```ruby
begin
  # Balance: Transaction
  data, status_code, headers = api_instance.show_merchant_balance_transaction_with_http_info(merchant_id, currency, transaction_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Transaction>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_balance_transaction_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **currency** | [**Currency**](.md) |  |  |
| **transaction_uuid** | **String** |  |  |

### Return type

[**Transaction**](Transaction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_submerchant_settlement

> <Settlement> show_submerchant_settlement(merchant_id, id)

Settlement: Show

View a settlement given an `id`.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
id = 'id_example' # String | 

begin
  # Settlement: Show
  result = api_instance.show_submerchant_settlement(merchant_id, id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_submerchant_settlement: #{e}"
end
```

#### Using the show_submerchant_settlement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Settlement>, Integer, Hash)> show_submerchant_settlement_with_http_info(merchant_id, id)

```ruby
begin
  # Settlement: Show
  data, status_code, headers = api_instance.show_submerchant_settlement_with_http_info(merchant_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Settlement>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_submerchant_settlement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **id** | **String** |  |  |

### Return type

[**Settlement**](Settlement.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## simulate_live_application_payment_method_status

> simulate_live_application_payment_method_status(merchant_id, payment_method, simulate_live_application_payment_method_status_request)

Live Application: Simulate Payment Method Status

Simulate status change on payment method for test merchants

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
payment_method = 'payment_method_example' # String | 
simulate_live_application_payment_method_status_request = Komoju::SimulateLiveApplicationPaymentMethodStatusRequest.new # SimulateLiveApplicationPaymentMethodStatusRequest | 

begin
  # Live Application: Simulate Payment Method Status
  api_instance.simulate_live_application_payment_method_status(merchant_id, payment_method, simulate_live_application_payment_method_status_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->simulate_live_application_payment_method_status: #{e}"
end
```

#### Using the simulate_live_application_payment_method_status_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> simulate_live_application_payment_method_status_with_http_info(merchant_id, payment_method, simulate_live_application_payment_method_status_request)

```ruby
begin
  # Live Application: Simulate Payment Method Status
  data, status_code, headers = api_instance.simulate_live_application_payment_method_status_with_http_info(merchant_id, payment_method, simulate_live_application_payment_method_status_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->simulate_live_application_payment_method_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **payment_method** | **String** |  |  |
| **simulate_live_application_payment_method_status_request** | [**SimulateLiveApplicationPaymentMethodStatusRequest**](SimulateLiveApplicationPaymentMethodStatusRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## simulate_live_application_status

> simulate_live_application_status(merchant_id, simulate_live_application_payment_method_status_request)

Live Application: Simulate Status

Simulate status change on applications for test merchants

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
simulate_live_application_payment_method_status_request = Komoju::SimulateLiveApplicationPaymentMethodStatusRequest.new # SimulateLiveApplicationPaymentMethodStatusRequest | 

begin
  # Live Application: Simulate Status
  api_instance.simulate_live_application_status(merchant_id, simulate_live_application_payment_method_status_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->simulate_live_application_status: #{e}"
end
```

#### Using the simulate_live_application_status_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> simulate_live_application_status_with_http_info(merchant_id, simulate_live_application_payment_method_status_request)

```ruby
begin
  # Live Application: Simulate Status
  data, status_code, headers = api_instance.simulate_live_application_status_with_http_info(merchant_id, simulate_live_application_payment_method_status_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->simulate_live_application_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **simulate_live_application_payment_method_status_request** | [**SimulateLiveApplicationPaymentMethodStatusRequest**](SimulateLiveApplicationPaymentMethodStatusRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## submerchant_settlement_csv

> submerchant_settlement_csv(merchant_id, id)

Settlement: CSV

View a settlement in CSV format given an `id`.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
id = 'id_example' # String | 

begin
  # Settlement: CSV
  api_instance.submerchant_settlement_csv(merchant_id, id)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->submerchant_settlement_csv: #{e}"
end
```

#### Using the submerchant_settlement_csv_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> submerchant_settlement_csv_with_http_info(merchant_id, id)

```ruby
begin
  # Settlement: CSV
  data, status_code, headers = api_instance.submerchant_settlement_csv_with_http_info(merchant_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->submerchant_settlement_csv_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## submerchant_settlement_pdf

> submerchant_settlement_pdf(merchant_id, id)

Settlement: PDF

View a settlement in PDF format given an `id`.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
id = 'id_example' # String | 

begin
  # Settlement: PDF
  api_instance.submerchant_settlement_pdf(merchant_id, id)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->submerchant_settlement_pdf: #{e}"
end
```

#### Using the submerchant_settlement_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> submerchant_settlement_pdf_with_http_info(merchant_id, id)

```ruby
begin
  # Settlement: PDF
  data, status_code, headers = api_instance.submerchant_settlement_pdf_with_http_info(merchant_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->submerchant_settlement_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## submerchant_settlement_xls

> submerchant_settlement_xls(merchant_id, id)

Settlement: XLS

View a settlement in XLS format given an `id`.

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
id = 'id_example' # String | 

begin
  # Settlement: XLS
  api_instance.submerchant_settlement_xls(merchant_id, id)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->submerchant_settlement_xls: #{e}"
end
```

#### Using the submerchant_settlement_xls_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> submerchant_settlement_xls_with_http_info(merchant_id, id)

```ruby
begin
  # Settlement: XLS
  data, status_code, headers = api_instance.submerchant_settlement_xls_with_http_info(merchant_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->submerchant_settlement_xls_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## update_live_application

> update_live_application(merchant_id, live_application_request)

Live Application: Update

Updates the live application for the applicant merchant

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
live_application_request = Komoju::LiveApplicationRequest.new # LiveApplicationRequest | 

begin
  # Live Application: Update
  api_instance.update_live_application(merchant_id, live_application_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_live_application: #{e}"
end
```

#### Using the update_live_application_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_live_application_with_http_info(merchant_id, live_application_request)

```ruby
begin
  # Live Application: Update
  data, status_code, headers = api_instance.update_live_application_with_http_info(merchant_id, live_application_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_live_application_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **live_application_request** | [**LiveApplicationRequest**](LiveApplicationRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## update_live_application_payment_method

> update_live_application_payment_method(merchant_id, payment_method, update_payment_method_request)

Live Application: Update Payment Method

Update the payment method application of the applicant merchant

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

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
payment_method = 'payment_method_example' # String | 
update_payment_method_request = Komoju::UpdatePaymentMethodRequest.new # UpdatePaymentMethodRequest | 

begin
  # Live Application: Update Payment Method
  api_instance.update_live_application_payment_method(merchant_id, payment_method, update_payment_method_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_live_application_payment_method: #{e}"
end
```

#### Using the update_live_application_payment_method_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_live_application_payment_method_with_http_info(merchant_id, payment_method, update_payment_method_request)

```ruby
begin
  # Live Application: Update Payment Method
  data, status_code, headers = api_instance.update_live_application_payment_method_with_http_info(merchant_id, payment_method, update_payment_method_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_live_application_payment_method_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **payment_method** | **String** |  |  |
| **update_payment_method_request** | [**UpdatePaymentMethodRequest**](UpdatePaymentMethodRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## update_merchant

> update_merchant(id, update_merchant_request)

Merchant: Update

Updates merchant.

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

api_instance = Komoju::PlatformModelApi.new
id = 'id_example' # String | 
update_merchant_request = Komoju::UpdateMerchantRequest.new # UpdateMerchantRequest | 

begin
  # Merchant: Update
  api_instance.update_merchant(id, update_merchant_request)
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_merchant: #{e}"
end
```

#### Using the update_merchant_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_merchant_with_http_info(id, update_merchant_request)

```ruby
begin
  # Merchant: Update
  data, status_code, headers = api_instance.update_merchant_with_http_info(id, update_merchant_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_merchant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **update_merchant_request** | [**UpdateMerchantRequest**](UpdateMerchantRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

