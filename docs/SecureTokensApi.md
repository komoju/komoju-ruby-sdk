# Komoju::SecureTokensApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_secure_token**](SecureTokensApi.md#create_secure_token) | **POST** /secure_tokens | SecureToken: Create |
| [**show_secure_token**](SecureTokensApi.md#show_secure_token) | **GET** /secure_tokens/{id} | SecureToken: Show |

## Request Models

- [**CreateSecureTokenRequest**](CreateSecureTokenRequest.md) — used by `create_secure_token`


## create_secure_token

> <SecureToken> create_secure_token(create_secure_token_request)

SecureToken: Create

Creates a SecureToken with the given credit card `payment_details` or `customer` ID.  There are two ways to create a SecureToken:  - Using `payment_details` with credit card information. - Using `customer` ID, which is a unique identifier for a customer created via the [Customer: Create](https://doc.komoju.com/reference/createcustomer) endpoint. Customer's saved payment details will be used as `payment_details`.  It is recommended to have a client application make this request directly so that sensitive payment information (e.g. credit card number) doesn't hit your server. Receiving credit card numbers requires your business to be PCI-DSS compliant. Once you create a secure token using a customer's credit card details, you can redirect the customer to the authentication url to perform 3DS authentication. Once a secure token has been authenticated, the secure token id can safely be sent to your server and used as `payment_details` to a future KOMOJU API request.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SecureTokensApi.new
create_secure_token_request = Komoju::CreateSecureTokenRequestWithCustomer.new({amount: 37, currency: Komoju::Currency::JPY, customer: 'cust14ur4hvws08idzacf6et8', return_url: 'return_url_example'}) # CreateSecureTokenRequest | 

begin
  # SecureToken: Create
  result = api_instance.create_secure_token(create_secure_token_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SecureTokensApi->create_secure_token: #{e}"
end
```

#### Using the create_secure_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SecureToken>, Integer, Hash)> create_secure_token_with_http_info(create_secure_token_request)

```ruby
begin
  # SecureToken: Create
  data, status_code, headers = api_instance.create_secure_token_with_http_info(create_secure_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SecureToken>
rescue Komoju::ApiError => e
  puts "Error when calling SecureTokensApi->create_secure_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_secure_token_request** | [**CreateSecureTokenRequest**](CreateSecureTokenRequest.md) |  |  |

### Return type

[**SecureToken**](SecureToken.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## show_secure_token

> <SecureToken> show_secure_token(id)

SecureToken: Show

Retrieves a single SecureToken object by its `id`.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::SecureTokensApi.new
id = 'id_example' # String | A unique identifier for the SecureToken.

begin
  # SecureToken: Show
  result = api_instance.show_secure_token(id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling SecureTokensApi->show_secure_token: #{e}"
end
```

#### Using the show_secure_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SecureToken>, Integer, Hash)> show_secure_token_with_http_info(id)

```ruby
begin
  # SecureToken: Show
  data, status_code, headers = api_instance.show_secure_token_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SecureToken>
rescue Komoju::ApiError => e
  puts "Error when calling SecureTokensApi->show_secure_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique identifier for the SecureToken. |  |

### Return type

[**SecureToken**](SecureToken.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

