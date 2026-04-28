# Komoju::TokensApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_token**](TokensApi.md#create_token) | **POST** /tokens | Token: Create |

## Request Models

- [**CreateTokenRequest**](CreateTokenRequest.md) — used by `create_token`


## create_token

> <Token> create_token(create_token_request)

Token: Create

Creates a token with the given `payment_details`.  It is recommended to have a client application make this request directly so that sensitive payment information (e.g. credit card number) doesn't hit your server. Receiving credit card numbers requires your business to be PCI-DSS compliant. Once you turn your customer's details into a token, the token string can safely be sent to your server and used as `payment_details` to a future KOMOJU API request.  A `currency` may be optionally specified. When `currency` is provided, KOMOJU will ensure that the payment made using the new token is in the same currency.

### Examples

```ruby
require 'time'
require 'komoju-ruby-sdk'
# setup authorization
Komoju.configure do |config|
  # Configure your KOMOJU API key
  config.api_key = 'YOUR_API_KEY'
end

api_instance = Komoju::TokensApi.new
create_token_request = Komoju::CreateTokenRequest.new({payment_details: Komoju::PaymentDetailsCreditCard.new({type: 'credit_card', number: '4111111111111111', month: 10, year: 2031})}) # CreateTokenRequest | 

begin
  # Token: Create
  result = api_instance.create_token(create_token_request)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling TokensApi->create_token: #{e}"
end
```

#### Using the create_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Token>, Integer, Hash)> create_token_with_http_info(create_token_request)

```ruby
begin
  # Token: Create
  data, status_code, headers = api_instance.create_token_with_http_info(create_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Token>
rescue Komoju::ApiError => e
  puts "Error when calling TokensApi->create_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_token_request** | [**CreateTokenRequest**](CreateTokenRequest.md) |  |  |

### Return type

[**Token**](Token.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

