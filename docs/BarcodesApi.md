# Komoju::BarcodesApi

All URIs are relative to *https://komoju.com/api/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**show_barcode**](BarcodesApi.md#show_barcode) | **GET** /barcodes/{payment_id} | Barcode: Show |


## show_barcode

> <ShowBarcode200Response> show_barcode(payment_id)

Barcode: Show

Fetches the latest barcode for a konbini payment.  Barcodes can be displayed in your client application to give your customers a more convenient way to pay. Not all konbini payments are compatible with barcodes. If a payment is compatible, it will have a `barcode_url` field in its `payment_details` object, which is a reference to this endpoint.  Newly created payments may not have a barcode available immediately. If the barcode is still being generated, the response will have a `status` of `pending` and a `retry_after` field indicating how many seconds to wait before you may retry the request.  The barcodes can only be used for payment for a limited amount of time, by default this is 10 minutes. Subsequent requests to this endpoint will return the same barcode as long as it is still valid. After expiration, a new barcode will be generated and returned.  <details> <summary>Fetching barcodes in JavaScript</summary>  If you're integrating barcodes on your website, the following JavaScript function can be used to fetch barcode data, handling the pending status and retrying. The `barcode_url` parameter is returned from Payments APIs when the payment is compatible with barcodes.  ```javascript async function fetchBarcode(barcode_url) {   const response = await fetch(barcode_url);   if (!response.ok) {     throw new Error(       `Error fetching barcode: ${response.status} ${response.statusText}`     );   }    const { status, retry_after, ...barcode } = await response.json();   if (status === 'ready') {     return barcode;   } else if (status === 'pending') {     await new Promise(resolve => setTimeout(resolve, retry_after * 1000));     return fetchBarcode(barcode_url);   } else {     throw new Error(`Error fetching barcode: unexpected status ${status}`);   } } ``` </details>

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

api_instance = Komoju::BarcodesApi.new
payment_id = 'payment_id_example' # String | Payment unique identifier

begin
  # Barcode: Show
  result = api_instance.show_barcode(payment_id)
  p result
rescue Komoju::ApiError => e
  puts "Error when calling BarcodesApi->show_barcode: #{e}"
end
```

#### Using the show_barcode_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShowBarcode200Response>, Integer, Hash)> show_barcode_with_http_info(payment_id)

```ruby
begin
  # Barcode: Show
  data, status_code, headers = api_instance.show_barcode_with_http_info(payment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShowBarcode200Response>
rescue Komoju::ApiError => e
  puts "Error when calling BarcodesApi->show_barcode_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payment_id** | **String** | Payment unique identifier |  |

### Return type

[**ShowBarcode200Response**](ShowBarcode200Response.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

