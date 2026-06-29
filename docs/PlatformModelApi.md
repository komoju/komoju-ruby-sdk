# Komoju::PlatformModelApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**balance_transfer**](PlatformModelApi.md#balance_transfer) | **POST** /balances/{currency}/transfer | Balance: Transfer |
| [**create_file**](PlatformModelApi.md#create_file) | **POST** /merchants/{merchant_id}/files | File: Create |
| [**create_merchant**](PlatformModelApi.md#create_merchant) | **POST** /merchants | Merchant: Create |
| [**create_merchant_balance_transfer**](PlatformModelApi.md#create_merchant_balance_transfer) | **POST** /merchants/{merchant_id}/balances/{currency}/transfer | Balance: Transfer |
| [**edit_merchant_balance_settings**](PlatformModelApi.md#edit_merchant_balance_settings) | **PUT** /merchants/{merchant_id}/balances/{currency}/settings | Balances: Edit Settings |
| [**list_live_application_payment_methods**](PlatformModelApi.md#list_live_application_payment_methods) | **GET** /live_application/{merchant_id}/payment_methods | Live Application: Payment Methods |
| [**list_merchants**](PlatformModelApi.md#list_merchants) | **GET** /merchants | Merchant: List |
| [**list_submerchant_payments**](PlatformModelApi.md#list_submerchant_payments) | **GET** /merchants/{merchant_id}/payments | Payment: List for Merchant |
| [**list_submerchant_settlements**](PlatformModelApi.md#list_submerchant_settlements) | **GET** /merchants/{merchant_id}/settlements | Settlement: List |
| [**merchant_balance_transactions**](PlatformModelApi.md#merchant_balance_transactions) | **GET** /merchants/{merchant_id}/balances/{currency}/transactions | Balance: Transactions |
| [**show_file**](PlatformModelApi.md#show_file) | **GET** /merchants/{merchant_id}/files/{id} | File: Show |
| [**show_live_application**](PlatformModelApi.md#show_live_application) | **GET** /live_application/{merchant_id} | Live Application: Show |
| [**show_live_application_payment_method**](PlatformModelApi.md#show_live_application_payment_method) | **GET** /live_application/{merchant_id}/payment_methods/{payment_method} | Live Application: Show Payment Method |
| [**show_merchant**](PlatformModelApi.md#show_merchant) | **GET** /merchants/{id} | Merchant: Show |
| [**show_merchant_balance**](PlatformModelApi.md#show_merchant_balance) | **GET** /merchants/{merchant_id}/balances/{currency} | Balance: Show |
| [**show_merchant_balance_settings**](PlatformModelApi.md#show_merchant_balance_settings) | **GET** /merchants/{merchant_id}/balances/{currency}/settings | Balance: Show Settings |
| [**show_merchant_balance_transaction**](PlatformModelApi.md#show_merchant_balance_transaction) | **GET** /merchants/{merchant_id}/balances/{currency}/transactions/{transaction_uuid} | Balance: Transaction |
| [**show_submerchant_settlement**](PlatformModelApi.md#show_submerchant_settlement) | **GET** /merchants/{merchant_id}/settlements/{id} | Settlement: Show |
| [**simulate_live_application_payment_method_status**](PlatformModelApi.md#simulate_live_application_payment_method_status) | **PATCH** /live_application/{merchant_id}/payment_methods/{payment_method}/simulate_status | Live Application: Simulate Payment Method Status |
| [**simulate_live_application_status**](PlatformModelApi.md#simulate_live_application_status) | **PATCH** /live_application/{merchant_id}/simulate_status | Live Application: Simulate Status |
| [**submerchant_settlement_csv**](PlatformModelApi.md#submerchant_settlement_csv) | **GET** /merchants/{merchant_id}/settlements/{id}/csv | Settlement: CSV |
| [**submerchant_settlement_pdf**](PlatformModelApi.md#submerchant_settlement_pdf) | **GET** /merchants/{merchant_id}/settlements/{id}/pdf | Settlement: PDF |
| [**submerchant_settlement_xls**](PlatformModelApi.md#submerchant_settlement_xls) | **GET** /merchants/{merchant_id}/settlements/{id}/xls | Settlement: XLS |
| [**update_live_application**](PlatformModelApi.md#update_live_application) | **PATCH** /live_application/{merchant_id} | Live Application: Update |
| [**update_live_application_payment_method**](PlatformModelApi.md#update_live_application_payment_method) | **PATCH** /live_application/{merchant_id}/payment_methods/{payment_method} | Live Application: Update Payment Method |
| [**update_merchant**](PlatformModelApi.md#update_merchant) | **PATCH** /merchants/{id} | Merchant: Update |

## Request Models

- [**BalanceTransferRequest**](BalanceTransferRequest.md) — used by `balance_transfer`
- [**CreateFileRequest**](CreateFileRequest.md) — used by `create_file`
- [**CreateMerchantRequest**](CreateMerchantRequest.md) — used by `create_merchant`
- [**CreateMerchantBalanceTransferRequest**](CreateMerchantBalanceTransferRequest.md) — used by `create_merchant_balance_transfer`
- [**EditMerchantBalanceSettingsRequest**](EditMerchantBalanceSettingsRequest.md) — used by `edit_merchant_balance_settings`
- [**SimulateLiveApplicationPaymentMethodStatusRequest**](SimulateLiveApplicationPaymentMethodStatusRequest.md) — used by `simulate_live_application_payment_method_status`
- [**SimulateLiveApplicationPaymentMethodStatusRequest**](SimulateLiveApplicationPaymentMethodStatusRequest.md) — used by `simulate_live_application_status`
- [**LiveApplicationRequest**](LiveApplicationRequest.md) — used by `update_live_application`
- [**UpdatePaymentMethodRequest**](UpdatePaymentMethodRequest.md) — used by `update_live_application_payment_method`
- [**UpdateMerchantRequest**](UpdateMerchantRequest.md) — used by `update_merchant`


## balance_transfer

> <Transfer> balance_transfer(currency, balance_transfer_request)

Balance: Transfer

Transfers funds from the currently authenticated merchant's balance to another associated merchant for the given `currency`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
create_file_request = Komoju::CreateFileRequest.new({paper: 'paper_example'}) # CreateFileRequest | 

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

> <SerializedSubmerchant> create_merchant(create_merchant_request)

Merchant: Create

Creates a new merchant.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
create_merchant_request = Komoju::CreateMerchantRequest.new({name: 'name_example', platform_role: Komoju::MerchantRole::SELLER}) # CreateMerchantRequest | 

begin
  # Merchant: Create
  result = api_instance.create_merchant(create_merchant_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant: #{e}"
end
```

#### Using the create_merchant_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SerializedSubmerchant>, Integer, Hash)> create_merchant_with_http_info(create_merchant_request)

```ruby
begin
  # Merchant: Create
  data, status_code, headers = api_instance.create_merchant_with_http_info(create_merchant_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SerializedSubmerchant>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_merchant_request** | [**CreateMerchantRequest**](CreateMerchantRequest.md) |  |  |

### Return type

[**SerializedSubmerchant**](SerializedSubmerchant.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_merchant_balance_transfer

> <BalanceTransferServiceRecord> create_merchant_balance_transfer(merchant_id, currency, create_merchant_balance_transfer_request)

Balance: Transfer

Creates a balance transfer between associated merchants for a given `amount` and `currency`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 
create_merchant_balance_transfer_request = Komoju::CreateMerchantBalanceTransferRequest.new({currency: Komoju::Currency::JPY, to: 'to_example', amount: 37}) # CreateMerchantBalanceTransferRequest | 

begin
  # Balance: Transfer
  result = api_instance.create_merchant_balance_transfer(merchant_id, currency, create_merchant_balance_transfer_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->create_merchant_balance_transfer: #{e}"
end
```

#### Using the create_merchant_balance_transfer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BalanceTransferServiceRecord>, Integer, Hash)> create_merchant_balance_transfer_with_http_info(merchant_id, currency, create_merchant_balance_transfer_request)

```ruby
begin
  # Balance: Transfer
  data, status_code, headers = api_instance.create_merchant_balance_transfer_with_http_info(merchant_id, currency, create_merchant_balance_transfer_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BalanceTransferServiceRecord>
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

[**BalanceTransferServiceRecord**](BalanceTransferServiceRecord.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## edit_merchant_balance_settings

> <MerchantBalance> edit_merchant_balance_settings(merchant_id, currency, edit_merchant_balance_settings_request)

Balances: Edit Settings

Given a currency, edit the payout settings of the currently authenticated merchant or one of its sub-merchants.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
currency = Komoju::Currency::JPY # Currency | 
edit_merchant_balance_settings_request = Komoju::EditMerchantBalanceSettingsRequest.new({currency: Komoju::Currency::JPY, frequency: Komoju::SettlementFrequency::WEEKLY, settlement_minimum_amount: 37}) # EditMerchantBalanceSettingsRequest | 

begin
  # Balances: Edit Settings
  result = api_instance.edit_merchant_balance_settings(merchant_id, currency, edit_merchant_balance_settings_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->edit_merchant_balance_settings: #{e}"
end
```

#### Using the edit_merchant_balance_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MerchantBalance>, Integer, Hash)> edit_merchant_balance_settings_with_http_info(merchant_id, currency, edit_merchant_balance_settings_request)

```ruby
begin
  # Balances: Edit Settings
  data, status_code, headers = api_instance.edit_merchant_balance_settings_with_http_info(merchant_id, currency, edit_merchant_balance_settings_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MerchantBalance>
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

[**MerchantBalance**](MerchantBalance.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_live_application_payment_methods

> <PaymentMethodsList> list_live_application_payment_methods(merchant_id, opts)

Live Application: Payment Methods

List submitted/unsubmitted payment methods

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
opts = {
  locale: Komoju::Locale::JA # Locale | 
}

begin
  # Live Application: Payment Methods
  result = api_instance.list_live_application_payment_methods(merchant_id, opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_live_application_payment_methods: #{e}"
end
```

#### Using the list_live_application_payment_methods_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentMethodsList>, Integer, Hash)> list_live_application_payment_methods_with_http_info(merchant_id, opts)

```ruby
begin
  # Live Application: Payment Methods
  data, status_code, headers = api_instance.list_live_application_payment_methods_with_http_info(merchant_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentMethodsList>
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

[**PaymentMethodsList**](PaymentMethodsList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_merchants

> <SubmerchantsList> list_merchants(opts)

Merchant: List

Retrieves a paginated list of sub-merchants. Results can be filtered by `live` status, `platform_role`, account `status`, and whether payments or payouts are enabled.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  live: true, # Boolean | 
  platform_role: Komoju::MerchantRole::SELLER, # MerchantRole | 
  status: 'status_example', # String | 
  payments_enabled: true, # Boolean | 
  payouts_enabled: true # Boolean | 
}

begin
  # Merchant: List
  result = api_instance.list_merchants(opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_merchants: #{e}"
end
```

#### Using the list_merchants_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubmerchantsList>, Integer, Hash)> list_merchants_with_http_info(opts)

```ruby
begin
  # Merchant: List
  data, status_code, headers = api_instance.list_merchants_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubmerchantsList>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_merchants_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **live** | **Boolean** |  | [optional] |
| **platform_role** | [**MerchantRole**](.md) |  | [optional] |
| **status** | **String** |  | [optional] |
| **payments_enabled** | **Boolean** |  | [optional] |
| **payouts_enabled** | **Boolean** |  | [optional] |

### Return type

[**SubmerchantsList**](SubmerchantsList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_submerchant_payments

> <PlatformMerchantPaymentList> list_submerchant_payments(merchant_id, opts)

Payment: List for Merchant

Retrieves a paginated list of payments. Pagination can be configured with `page` and `per_page` parameters.  Payments can be filtered by `currency`, `external_order_num`, and `status`.  A time range can be specified with `start_time`, and `end_time`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
opts = {
  start_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created after this time.
  end_time: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Query for records created before this time.
  per_page: 56, # Integer | How many objects per page.
  page: 56, # Integer | Page number to query for.
  currency: Komoju::Currency::JPY, # Currency | 
  external_order_num: 'external_order_num_example', # String | 
  status: Komoju::PaymentStatus::PENDING # PaymentStatus | 
}

begin
  # Payment: List for Merchant
  result = api_instance.list_submerchant_payments(merchant_id, opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_submerchant_payments: #{e}"
end
```

#### Using the list_submerchant_payments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PlatformMerchantPaymentList>, Integer, Hash)> list_submerchant_payments_with_http_info(merchant_id, opts)

```ruby
begin
  # Payment: List for Merchant
  data, status_code, headers = api_instance.list_submerchant_payments_with_http_info(merchant_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PlatformMerchantPaymentList>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->list_submerchant_payments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **start_time** | **Time** | Query for records created after this time. | [optional] |
| **end_time** | **Time** | Query for records created before this time. | [optional] |
| **per_page** | **Integer** | How many objects per page. | [optional] |
| **page** | **Integer** | Page number to query for. | [optional] |
| **currency** | [**Currency**](.md) |  | [optional] |
| **external_order_num** | **String** |  | [optional] |
| **status** | [**PaymentStatus**](.md) |  | [optional] |

### Return type

[**PlatformMerchantPaymentList**](PlatformMerchantPaymentList.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_submerchant_settlements

> <SettlementList> list_submerchant_settlements(merchant_id)

Settlement: List

Lists out past settlements from most-recent to least-recent.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

Given a currency, view the ledger transactions of the currently authenticated merchant or one of its sub-merchants. Will split ledger transactions into line items when appropriate.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
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


## show_file

> <MerchantFile> show_file(merchant_id, id)

File: Show

Retrieves an existing file of the current merchant.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <LiveApplicationWithSubmittedFields> show_live_application(merchant_id, opts)

Live Application: Show

Shows the live application status of the applicant merchant

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array(<LiveApplicationWithSubmittedFields>, Integer, Hash)> show_live_application_with_http_info(merchant_id, opts)

```ruby
begin
  # Live Application: Show
  data, status_code, headers = api_instance.show_live_application_with_http_info(merchant_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LiveApplicationWithSubmittedFields>
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

[**LiveApplicationWithSubmittedFields**](LiveApplicationWithSubmittedFields.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_live_application_payment_method

> <PaymentMethodApplicationWithSubmittedFields> show_live_application_payment_method(merchant_id, payment_method, opts)

Live Application: Show Payment Method

Shows the payment method status of the applicant merchant

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
payment_method = 'payment_method_example' # String | 
opts = {
  locale: Komoju::Locale::JA # Locale | 
}

begin
  # Live Application: Show Payment Method
  result = api_instance.show_live_application_payment_method(merchant_id, payment_method, opts)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_live_application_payment_method: #{e}"
end
```

#### Using the show_live_application_payment_method_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentMethodApplicationWithSubmittedFields>, Integer, Hash)> show_live_application_payment_method_with_http_info(merchant_id, payment_method, opts)

```ruby
begin
  # Live Application: Show Payment Method
  data, status_code, headers = api_instance.show_live_application_payment_method_with_http_info(merchant_id, payment_method, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentMethodApplicationWithSubmittedFields>
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

[**PaymentMethodApplicationWithSubmittedFields**](PaymentMethodApplicationWithSubmittedFields.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_merchant

> <SerializedSubmerchant> show_merchant(id)

Merchant: Show

Retrieves the details of a sub-merchant by its `id`, including account settings, payout configuration, and live status.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
id = 'id_example' # String | 

begin
  # Merchant: Show
  result = api_instance.show_merchant(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant: #{e}"
end
```

#### Using the show_merchant_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SerializedSubmerchant>, Integer, Hash)> show_merchant_with_http_info(id)

```ruby
begin
  # Merchant: Show
  data, status_code, headers = api_instance.show_merchant_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SerializedSubmerchant>
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->show_merchant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**SerializedSubmerchant**](SerializedSubmerchant.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_merchant_balance

> <BalanceShow> show_merchant_balance(merchant_id, currency)

Balance: Show

Given a currency, view the unsettled balance of the currently authenticated merchant or one of its sub-merchants.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array(<BalanceShow>, Integer, Hash)> show_merchant_balance_with_http_info(merchant_id, currency)

```ruby
begin
  # Balance: Show
  data, status_code, headers = api_instance.show_merchant_balance_with_http_info(merchant_id, currency)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BalanceShow>
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

[**BalanceShow**](BalanceShow.md)

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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array<Transaction>> show_merchant_balance_transaction(merchant_id, currency, transaction_uuid)

Balance: Transaction

Given a currency and a transaction UUID, view the corresponding ledger transaction of the currently authenticated merchant or one of its sub-merchants. Will return one entry per line item of the transaction.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array(<Array<Transaction>>, Integer, Hash)> show_merchant_balance_transaction_with_http_info(merchant_id, currency, transaction_uuid)

```ruby
begin
  # Balance: Transaction
  data, status_code, headers = api_instance.show_merchant_balance_transaction_with_http_info(merchant_id, currency, transaction_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Transaction>>
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

[**Array&lt;Transaction&gt;**](Transaction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## show_submerchant_settlement

> <SettlementShow> show_submerchant_settlement(merchant_id, id)

Settlement: Show

View a settlement given an `id`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <Array(<SettlementShow>, Integer, Hash)> show_submerchant_settlement_with_http_info(merchant_id, id)

```ruby
begin
  # Settlement: Show
  data, status_code, headers = api_instance.show_submerchant_settlement_with_http_info(merchant_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SettlementShow>
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

[**SettlementShow**](SettlementShow.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## simulate_live_application_payment_method_status

> <PaymentMethodStatus> simulate_live_application_payment_method_status(merchant_id, payment_method, simulate_live_application_payment_method_status_request)

Live Application: Simulate Payment Method Status

Simulate status change on payment method for test merchants

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
payment_method = 'payment_method_example' # String | 
simulate_live_application_payment_method_status_request = Komoju::SimulateLiveApplicationPaymentMethodStatusRequest.new # SimulateLiveApplicationPaymentMethodStatusRequest | 

begin
  # Live Application: Simulate Payment Method Status
  result = api_instance.simulate_live_application_payment_method_status(merchant_id, payment_method, simulate_live_application_payment_method_status_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->simulate_live_application_payment_method_status: #{e}"
end
```

#### Using the simulate_live_application_payment_method_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentMethodStatus>, Integer, Hash)> simulate_live_application_payment_method_status_with_http_info(merchant_id, payment_method, simulate_live_application_payment_method_status_request)

```ruby
begin
  # Live Application: Simulate Payment Method Status
  data, status_code, headers = api_instance.simulate_live_application_payment_method_status_with_http_info(merchant_id, payment_method, simulate_live_application_payment_method_status_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentMethodStatus>
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

[**PaymentMethodStatus**](PaymentMethodStatus.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## simulate_live_application_status

> <MerchantSubmissionStatus> simulate_live_application_status(merchant_id, simulate_live_application_payment_method_status_request)

Live Application: Simulate Status

Simulate status change on applications for test merchants. In order for status to be changed to \"accepted,\" at least one payment method must be approved.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
simulate_live_application_payment_method_status_request = Komoju::SimulateLiveApplicationPaymentMethodStatusRequest.new # SimulateLiveApplicationPaymentMethodStatusRequest | 

begin
  # Live Application: Simulate Status
  result = api_instance.simulate_live_application_status(merchant_id, simulate_live_application_payment_method_status_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->simulate_live_application_status: #{e}"
end
```

#### Using the simulate_live_application_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MerchantSubmissionStatus>, Integer, Hash)> simulate_live_application_status_with_http_info(merchant_id, simulate_live_application_payment_method_status_request)

```ruby
begin
  # Live Application: Simulate Status
  data, status_code, headers = api_instance.simulate_live_application_status_with_http_info(merchant_id, simulate_live_application_payment_method_status_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MerchantSubmissionStatus>
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

[**MerchantSubmissionStatus**](MerchantSubmissionStatus.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## submerchant_settlement_csv

> submerchant_settlement_csv(merchant_id, id)

Settlement: CSV

View a settlement in CSV format given an `id`.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
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

> <LiveApplication> update_live_application(merchant_id, live_application_request)

Live Application: Update

Updates the live application for the applicant merchant

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
live_application_request = Komoju::LiveApplicationRequest.new # LiveApplicationRequest | 

begin
  # Live Application: Update
  result = api_instance.update_live_application(merchant_id, live_application_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_live_application: #{e}"
end
```

#### Using the update_live_application_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LiveApplication>, Integer, Hash)> update_live_application_with_http_info(merchant_id, live_application_request)

```ruby
begin
  # Live Application: Update
  data, status_code, headers = api_instance.update_live_application_with_http_info(merchant_id, live_application_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LiveApplication>
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

[**LiveApplication**](LiveApplication.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_live_application_payment_method

> <PaymentMethodApplication> update_live_application_payment_method(merchant_id, payment_method, update_payment_method_request)

Live Application: Update Payment Method

Update the payment method application of the applicant merchant

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
merchant_id = 'merchant_id_example' # String | 
payment_method = 'payment_method_example' # String | 
update_payment_method_request = Komoju::UpdatePaymentMethodRequest.new # UpdatePaymentMethodRequest | 

begin
  # Live Application: Update Payment Method
  result = api_instance.update_live_application_payment_method(merchant_id, payment_method, update_payment_method_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_live_application_payment_method: #{e}"
end
```

#### Using the update_live_application_payment_method_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentMethodApplication>, Integer, Hash)> update_live_application_payment_method_with_http_info(merchant_id, payment_method, update_payment_method_request)

```ruby
begin
  # Live Application: Update Payment Method
  data, status_code, headers = api_instance.update_live_application_payment_method_with_http_info(merchant_id, payment_method, update_payment_method_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentMethodApplication>
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

[**PaymentMethodApplication**](PaymentMethodApplication.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_merchant

> <SerializedSubmerchant> update_merchant(id, update_merchant_request)

Merchant: Update

Updates a sub-merchant's settings, including payment and payout toggles, email notification preferences, and payment method expiry settings.

### Examples

```ruby
require 'time'
require 'komoju-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::PlatformModelApi.new
id = 'id_example' # String | 
update_merchant_request = Komoju::UpdateMerchantRequest.new # UpdateMerchantRequest | 

begin
  # Merchant: Update
  result = api_instance.update_merchant(id, update_merchant_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling PlatformModelApi->update_merchant: #{e}"
end
```

#### Using the update_merchant_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SerializedSubmerchant>, Integer, Hash)> update_merchant_with_http_info(id, update_merchant_request)

```ruby
begin
  # Merchant: Update
  data, status_code, headers = api_instance.update_merchant_with_http_info(id, update_merchant_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SerializedSubmerchant>
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

[**SerializedSubmerchant**](SerializedSubmerchant.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

