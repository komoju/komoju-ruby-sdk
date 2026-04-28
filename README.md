# komoju-ruby-sdk

Ruby gem for the KOMOJU API — Full featured access to the KOMOJU payments system.

## Installation

Add to your Gemfile:

```ruby
gem 'komoju-ruby-sdk', '~> 1.0.0'
```

Then run `bundle install`.

## Quick Start

```ruby
require 'komoju-ruby-sdk'

Komoju.configure do |config|
  config.api_key = 'YOUR_SECRET_KEY'
  # Use a test key during development
end
```

Get your API keys from the [KOMOJU Merchant Settings](https://komoju.com/merchant/settings).

### Accept a Payment

Charge a customer directly with their payment details:

```ruby
payments_api = Komoju::PaymentsApi.new

begin
  payment = payments_api.create_payment(
    Komoju::CreatePaymentRequestWithPaymentDetails.new(
      amount: 1000,
      currency: 'JPY',
      payment_details: {
        type: 'credit_card',
        number: '4111111111111111',
        month: 12,
        year: 2025,
        verification_value: '123'
      }
    )
  )
  puts "Payment created: #{payment.id} (#{payment.status})"

  # Capture an authorized payment
  captured = payments_api.capture_payment(payment.id, Komoju::CapturePaymentRequest.new)
  puts "Payment captured: #{captured.captured_at}"
rescue Komoju::ApiError => e
  puts "Error #{e.code}: #{e.message}"
end
```

### Hosted Payment Page (Sessions)

Redirect customers to a KOMOJU-hosted checkout page:

```ruby
sessions_api = Komoju::SessionsApi.new

begin
  session = sessions_api.create_session(
    Komoju::CreateSessionRequestWithPaymentMode.new(
      mode: 'payment',
      amount: 5000,
      currency: 'JPY',
      return_url: 'https://example.com/thank-you',
      default_locale: 'ja'
    )
  )
  puts "Redirect customer to: #{session.session_url}"
rescue Komoju::ApiError => e
  puts "Error #{e.code}: #{e.message}"
end
```

## Error Handling

All API errors raise `Komoju::ApiError`:

```ruby
begin
  payment = payments_api.show_payment('pay_xxx')
rescue Komoju::ApiError => e
  puts e.code     # HTTP status code (e.g. 404, 422)
  puts e.message  # Human-readable error description
end
```

## Documentation

Full API reference is auto-generated in the `docs/` folder of this gem.

All URIs are relative to *https://komoju.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*Komoju::BarcodesApi* | [**show_barcode**](docs/BarcodesApi.md#show_barcode) | **GET** /barcodes/{payment_id} | Barcode: Show
*Komoju::DisbursementsApi* | [**cancel_disbursement**](docs/DisbursementsApi.md#cancel_disbursement) | **POST** /disbursements/{id}/cancel | Disbursement: Cancel
*Komoju::DisbursementsApi* | [**create_disbursement**](docs/DisbursementsApi.md#create_disbursement) | **POST** /disbursements | Disbursement: Create
*Komoju::DisbursementsApi* | [**disbursement_report**](docs/DisbursementsApi.md#disbursement_report) | **GET** /disbursements/report | Disbursement: Report
*Komoju::DisbursementsApi* | [**list_disbursements**](docs/DisbursementsApi.md#list_disbursements) | **GET** /disbursements | Disbursement: List
*Komoju::DisbursementsApi* | [**show_disbursement**](docs/DisbursementsApi.md#show_disbursement) | **GET** /disbursements/{id} | Disbursement: Show
*Komoju::EventsApi* | [**list_events**](docs/EventsApi.md#list_events) | **GET** /events | Event: List
*Komoju::EventsApi* | [**show_event**](docs/EventsApi.md#show_event) | **GET** /events/{id} | Event Show
*Komoju::OneClickApi* | [**delete_external_customer**](docs/OneClickApi.md#delete_external_customer) | **DELETE** /external_customers/{id} | External Customer: Destroy
*Komoju::PaymentsApi* | [**cancel_payment**](docs/PaymentsApi.md#cancel_payment) | **POST** /payments/{id}/cancel | Payment: Cancel
*Komoju::PaymentsApi* | [**capture_payment**](docs/PaymentsApi.md#capture_payment) | **POST** /payments/{id}/capture | Payment: Capture
*Komoju::PaymentsApi* | [**create_payment**](docs/PaymentsApi.md#create_payment) | **POST** /payments | Payment: Create
*Komoju::PaymentsApi* | [**create_refund_request**](docs/PaymentsApi.md#create_refund_request) | **POST** /payments/{id}/refund_request | Payment: Refund Request
*Komoju::PaymentsApi* | [**finalize_payment**](docs/PaymentsApi.md#finalize_payment) | **POST** /payments/{id}/finalize | Payment: Finalize
*Komoju::PaymentsApi* | [**list_payment_methods**](docs/PaymentsApi.md#list_payment_methods) | **GET** /payment_methods | Payment Method: List
*Komoju::PaymentsApi* | [**list_payments**](docs/PaymentsApi.md#list_payments) | **GET** /payments | Payment: List
*Komoju::PaymentsApi* | [**refund_payment**](docs/PaymentsApi.md#refund_payment) | **POST** /payments/{id}/refund | Payment: Refund
*Komoju::PaymentsApi* | [**show_payment**](docs/PaymentsApi.md#show_payment) | **GET** /payments/{id} | Payment: Show
*Komoju::PaymentsApi* | [**update_payment**](docs/PaymentsApi.md#update_payment) | **PATCH** /payments/{id} | Payment: Update
*Komoju::PlatformModelApi* | [**balance_transfer**](docs/PlatformModelApi.md#balance_transfer) | **POST** /balances/{currency}/transfer | Balance: Transfer
*Komoju::PlatformModelApi* | [**create_file**](docs/PlatformModelApi.md#create_file) | **POST** /merchants/{merchant_id}/files | File: Create
*Komoju::PlatformModelApi* | [**create_merchant**](docs/PlatformModelApi.md#create_merchant) | **POST** /merchants | Merchant: Create
*Komoju::PlatformModelApi* | [**create_merchant_balance_transfer**](docs/PlatformModelApi.md#create_merchant_balance_transfer) | **POST** /merchants/{merchant_id}/balances/{currency}/transfer | Balance: Transfer
*Komoju::PlatformModelApi* | [**edit_merchant_balance_settings**](docs/PlatformModelApi.md#edit_merchant_balance_settings) | **PATCH** /merchants/{merchant_id}/balances/{currency}/settings | Balances: Edit Settings
*Komoju::PlatformModelApi* | [**list_live_application_payment_methods**](docs/PlatformModelApi.md#list_live_application_payment_methods) | **GET** /live_application/{merchant_id}/payment_methods | Live Application: Payment Methods
*Komoju::PlatformModelApi* | [**list_merchants**](docs/PlatformModelApi.md#list_merchants) | **GET** /merchants | Merchant: List
*Komoju::PlatformModelApi* | [**list_submerchant_payments**](docs/PlatformModelApi.md#list_submerchant_payments) | **GET** /merchants/{merchant_id}/payments | Payment: List for Merchant
*Komoju::PlatformModelApi* | [**list_submerchant_settlements**](docs/PlatformModelApi.md#list_submerchant_settlements) | **GET** /merchants/{merchant_id}/settlements | Settlement: List
*Komoju::PlatformModelApi* | [**merchant_balance_transactions**](docs/PlatformModelApi.md#merchant_balance_transactions) | **GET** /merchants/{merchant_id}/balances/{currency}/transactions | Balance: Transactions
*Komoju::PlatformModelApi* | [**show_file**](docs/PlatformModelApi.md#show_file) | **GET** /merchants/{merchant_id}/files/{id} | File: Show
*Komoju::PlatformModelApi* | [**show_live_application**](docs/PlatformModelApi.md#show_live_application) | **GET** /live_application/{merchant_id} | Live Application: Show
*Komoju::PlatformModelApi* | [**show_live_application_payment_method**](docs/PlatformModelApi.md#show_live_application_payment_method) | **GET** /live_application/{merchant_id}/payment_methods/{payment_method} | Live Application: Show Payment Method
*Komoju::PlatformModelApi* | [**show_merchant**](docs/PlatformModelApi.md#show_merchant) | **GET** /merchants/{id} | Merchant: Show
*Komoju::PlatformModelApi* | [**show_merchant_balance**](docs/PlatformModelApi.md#show_merchant_balance) | **GET** /merchants/{merchant_id}/balances/{currency} | Balance: Show
*Komoju::PlatformModelApi* | [**show_merchant_balance_settings**](docs/PlatformModelApi.md#show_merchant_balance_settings) | **GET** /merchants/{merchant_id}/balances/{currency}/settings | Balance: Show Settings
*Komoju::PlatformModelApi* | [**show_merchant_balance_transaction**](docs/PlatformModelApi.md#show_merchant_balance_transaction) | **GET** /merchants/{merchant_id}/balances/{currency}/transactions/{transaction_uuid} | Balance: Transaction
*Komoju::PlatformModelApi* | [**show_submerchant_settlement**](docs/PlatformModelApi.md#show_submerchant_settlement) | **GET** /merchants/{merchant_id}/settlements/{id} | Settlement: Show
*Komoju::PlatformModelApi* | [**simulate_live_application_payment_method_status**](docs/PlatformModelApi.md#simulate_live_application_payment_method_status) | **PATCH** /live_application/{merchant_id}/payment_methods/{payment_method}/simulate_status | Live Application: Simulate Payment Method Status
*Komoju::PlatformModelApi* | [**simulate_live_application_status**](docs/PlatformModelApi.md#simulate_live_application_status) | **PATCH** /live_application/{merchant_id}/simulate_status | Live Application: Simulate Status
*Komoju::PlatformModelApi* | [**submerchant_settlement_csv**](docs/PlatformModelApi.md#submerchant_settlement_csv) | **GET** /merchants/{merchant_id}/settlements/{id}/csv | Settlement: CSV
*Komoju::PlatformModelApi* | [**submerchant_settlement_pdf**](docs/PlatformModelApi.md#submerchant_settlement_pdf) | **GET** /merchants/{merchant_id}/settlements/{id}/pdf | Settlement: PDF
*Komoju::PlatformModelApi* | [**submerchant_settlement_xls**](docs/PlatformModelApi.md#submerchant_settlement_xls) | **GET** /merchants/{merchant_id}/settlements/{id}/xls | Settlement: XLS
*Komoju::PlatformModelApi* | [**update_live_application**](docs/PlatformModelApi.md#update_live_application) | **PATCH** /live_application/{merchant_id} | Live Application: Update
*Komoju::PlatformModelApi* | [**update_live_application_payment_method**](docs/PlatformModelApi.md#update_live_application_payment_method) | **PATCH** /live_application/{merchant_id}/payment_methods/{payment_method} | Live Application: Update Payment Method
*Komoju::PlatformModelApi* | [**update_merchant**](docs/PlatformModelApi.md#update_merchant) | **PATCH** /merchants/{id} | Merchant: Update
*Komoju::SecureTokensApi* | [**create_secure_token**](docs/SecureTokensApi.md#create_secure_token) | **POST** /secure_tokens | SecureToken: Create
*Komoju::SecureTokensApi* | [**show_secure_token**](docs/SecureTokensApi.md#show_secure_token) | **GET** /secure_tokens/{id} | SecureToken: Show
*Komoju::SessionsApi* | [**cancel_session**](docs/SessionsApi.md#cancel_session) | **POST** /sessions/{id}/cancel | Session: Cancel
*Komoju::SessionsApi* | [**create_session**](docs/SessionsApi.md#create_session) | **POST** /sessions | Session: Create
*Komoju::SessionsApi* | [**pay_session**](docs/SessionsApi.md#pay_session) | **POST** /sessions/{id}/pay | Session: Pay
*Komoju::SessionsApi* | [**show_session**](docs/SessionsApi.md#show_session) | **GET** /sessions/{id} | Session: Show
*Komoju::SettlementsApi* | [**list_settlements**](docs/SettlementsApi.md#list_settlements) | **GET** /settlements | Settlement: Index
*Komoju::SettlementsApi* | [**show_settlement**](docs/SettlementsApi.md#show_settlement) | **GET** /settlements/{id} | Settlement: Show
*Komoju::SettlementsApi* | [**show_settlement_csv**](docs/SettlementsApi.md#show_settlement_csv) | **GET** /settlements/{id}/csv | Settlement: CSV
*Komoju::SettlementsApi* | [**show_settlement_pdf**](docs/SettlementsApi.md#show_settlement_pdf) | **GET** /settlements/{id}/pdf | Settlement: PDF
*Komoju::SettlementsApi* | [**show_settlement_xls**](docs/SettlementsApi.md#show_settlement_xls) | **GET** /settlements/{id}/xls | Settlement: XLS
*Komoju::SettlementsApi* | [**show_transaction**](docs/SettlementsApi.md#show_transaction) | **GET** /balances/{currency}/transactions/{transaction_uuid} | Balance: Transaction
*Komoju::SubscriptionsApi* | [**create_customer**](docs/SubscriptionsApi.md#create_customer) | **POST** /customers | Customer: Create
*Komoju::SubscriptionsApi* | [**create_subscription**](docs/SubscriptionsApi.md#create_subscription) | **POST** /subscriptions | Subscription: Create
*Komoju::SubscriptionsApi* | [**delete_customer**](docs/SubscriptionsApi.md#delete_customer) | **DELETE** /customers/{id} | Customer: Destroy
*Komoju::SubscriptionsApi* | [**delete_subscription**](docs/SubscriptionsApi.md#delete_subscription) | **DELETE** /subscriptions/{id} | Subscription: Destroy
*Komoju::SubscriptionsApi* | [**list_customers**](docs/SubscriptionsApi.md#list_customers) | **GET** /customers | Customer: List
*Komoju::SubscriptionsApi* | [**list_subscriptions**](docs/SubscriptionsApi.md#list_subscriptions) | **GET** /subscriptions | Subscription: List
*Komoju::SubscriptionsApi* | [**show_customer**](docs/SubscriptionsApi.md#show_customer) | **GET** /customers/{id} | Customer: Show
*Komoju::SubscriptionsApi* | [**show_subscription**](docs/SubscriptionsApi.md#show_subscription) | **GET** /subscriptions/{id} | Subscription: Show
*Komoju::SubscriptionsApi* | [**update_customer**](docs/SubscriptionsApi.md#update_customer) | **PATCH** /customers/{id} | Customer: Update
*Komoju::TokensApi* | [**create_token**](docs/TokensApi.md#create_token) | **POST** /tokens | Token: Create


## Models

 - [Komoju::APIError](docs/APIError.md)
 - [Komoju::APIErrorError](docs/APIErrorError.md)
 - [Komoju::Address](docs/Address.md)
 - [Komoju::Auto](docs/Auto.md)
 - [Komoju::AvailablePaymentMethod](docs/AvailablePaymentMethod.md)
 - [Komoju::Balance](docs/Balance.md)
 - [Komoju::BalanceSettings](docs/BalanceSettings.md)
 - [Komoju::BalanceShow](docs/BalanceShow.md)
 - [Komoju::BalanceTransactionList](docs/BalanceTransactionList.md)
 - [Komoju::BalanceTransferRequest](docs/BalanceTransferRequest.md)
 - [Komoju::BalanceTransferServiceRecord](docs/BalanceTransferServiceRecord.md)
 - [Komoju::BarcodePendingResponse](docs/BarcodePendingResponse.md)
 - [Komoju::BarcodeReadyResponse](docs/BarcodeReadyResponse.md)
 - [Komoju::CancelDisbursementRequest](docs/CancelDisbursementRequest.md)
 - [Komoju::CapturePaymentRequest](docs/CapturePaymentRequest.md)
 - [Komoju::CapturePaymentRequestTax](docs/CapturePaymentRequestTax.md)
 - [Komoju::CountryCode](docs/CountryCode.md)
 - [Komoju::CreateCustomerRequest](docs/CreateCustomerRequest.md)
 - [Komoju::CreateDisbursementRequest](docs/CreateDisbursementRequest.md)
 - [Komoju::CreateFileRequest](docs/CreateFileRequest.md)
 - [Komoju::CreateMerchantBalanceTransferRequest](docs/CreateMerchantBalanceTransferRequest.md)
 - [Komoju::CreateMerchantRequest](docs/CreateMerchantRequest.md)
 - [Komoju::CreatePaymentRequest](docs/CreatePaymentRequest.md)
 - [Komoju::CreatePaymentRequestWithCustomer](docs/CreatePaymentRequestWithCustomer.md)
 - [Komoju::CreatePaymentRequestWithPaymentDetails](docs/CreatePaymentRequestWithPaymentDetails.md)
 - [Komoju::CreatePaymentRequestWithPaymentDetailsTax](docs/CreatePaymentRequestWithPaymentDetailsTax.md)
 - [Komoju::CreateRefundRequestRequest](docs/CreateRefundRequestRequest.md)
 - [Komoju::CreateSecureTokenRequest](docs/CreateSecureTokenRequest.md)
 - [Komoju::CreateSecureTokenRequestWithCustomer](docs/CreateSecureTokenRequestWithCustomer.md)
 - [Komoju::CreateSecureTokenRequestWithPaymentDetails](docs/CreateSecureTokenRequestWithPaymentDetails.md)
 - [Komoju::CreateSessionRequest](docs/CreateSessionRequest.md)
 - [Komoju::CreateSessionRequestWithCustomerMode](docs/CreateSessionRequestWithCustomerMode.md)
 - [Komoju::CreateSessionRequestWithCustomerPaymentMode](docs/CreateSessionRequestWithCustomerPaymentMode.md)
 - [Komoju::CreateSessionRequestWithPaymentMode](docs/CreateSessionRequestWithPaymentMode.md)
 - [Komoju::CreateSubscriptionRequest](docs/CreateSubscriptionRequest.md)
 - [Komoju::CreateTokenRequest](docs/CreateTokenRequest.md)
 - [Komoju::Currency](docs/Currency.md)
 - [Komoju::Customer](docs/Customer.md)
 - [Komoju::CustomerList](docs/CustomerList.md)
 - [Komoju::CustomerMetadata](docs/CustomerMetadata.md)
 - [Komoju::CustomerSource](docs/CustomerSource.md)
 - [Komoju::DeleteExternalCustomer204Response](docs/DeleteExternalCustomer204Response.md)
 - [Komoju::Disbursement](docs/Disbursement.md)
 - [Komoju::DisbursementList](docs/DisbursementList.md)
 - [Komoju::DisbursementStatus](docs/DisbursementStatus.md)
 - [Komoju::EditMerchantBalanceSettingsRequest](docs/EditMerchantBalanceSettingsRequest.md)
 - [Komoju::ErroredField](docs/ErroredField.md)
 - [Komoju::Event](docs/Event.md)
 - [Komoju::EventList](docs/EventList.md)
 - [Komoju::Field](docs/Field.md)
 - [Komoju::FieldFieldProperties](docs/FieldFieldProperties.md)
 - [Komoju::FinalizePaymentRequest](docs/FinalizePaymentRequest.md)
 - [Komoju::FraudDetails](docs/FraudDetails.md)
 - [Komoju::IndustryType](docs/IndustryType.md)
 - [Komoju::Installments](docs/Installments.md)
 - [Komoju::Intent](docs/Intent.md)
 - [Komoju::LineItem](docs/LineItem.md)
 - [Komoju::LiveApplication](docs/LiveApplication.md)
 - [Komoju::LiveApplicationRequest](docs/LiveApplicationRequest.md)
 - [Komoju::LiveApplicationStatus](docs/LiveApplicationStatus.md)
 - [Komoju::LiveApplicationWithSubmittedFields](docs/LiveApplicationWithSubmittedFields.md)
 - [Komoju::Locale](docs/Locale.md)
 - [Komoju::MerchantBalance](docs/MerchantBalance.md)
 - [Komoju::MerchantData](docs/MerchantData.md)
 - [Komoju::MerchantFile](docs/MerchantFile.md)
 - [Komoju::MerchantRole](docs/MerchantRole.md)
 - [Komoju::MerchantSubmissionStatus](docs/MerchantSubmissionStatus.md)
 - [Komoju::PaySessionRequest](docs/PaySessionRequest.md)
 - [Komoju::PaySessionResponse](docs/PaySessionResponse.md)
 - [Komoju::PaySessionResponseCustomer](docs/PaySessionResponseCustomer.md)
 - [Komoju::Payment](docs/Payment.md)
 - [Komoju::PaymentData](docs/PaymentData.md)
 - [Komoju::PaymentDataRequest](docs/PaymentDataRequest.md)
 - [Komoju::PaymentDetailsAU](docs/PaymentDetailsAU.md)
 - [Komoju::PaymentDetailsAlipay](docs/PaymentDetailsAlipay.md)
 - [Komoju::PaymentDetailsAlipayHK](docs/PaymentDetailsAlipayHK.md)
 - [Komoju::PaymentDetailsAll](docs/PaymentDetailsAll.md)
 - [Komoju::PaymentDetailsAupay](docs/PaymentDetailsAupay.md)
 - [Komoju::PaymentDetailsBancontact](docs/PaymentDetailsBancontact.md)
 - [Komoju::PaymentDetailsBankTransfer](docs/PaymentDetailsBankTransfer.md)
 - [Komoju::PaymentDetailsBitCash](docs/PaymentDetailsBitCash.md)
 - [Komoju::PaymentDetailsBlik](docs/PaymentDetailsBlik.md)
 - [Komoju::PaymentDetailsCVS](docs/PaymentDetailsCVS.md)
 - [Komoju::PaymentDetailsCreditCard](docs/PaymentDetailsCreditCard.md)
 - [Komoju::PaymentDetailsCreditCardBrazil](docs/PaymentDetailsCreditCardBrazil.md)
 - [Komoju::PaymentDetailsCreditCardKorea](docs/PaymentDetailsCreditCardKorea.md)
 - [Komoju::PaymentDetailsCreditCardKoreaSocialId](docs/PaymentDetailsCreditCardKoreaSocialId.md)
 - [Komoju::PaymentDetailsCreditCardTerminal](docs/PaymentDetailsCreditCardTerminal.md)
 - [Komoju::PaymentDetailsCultureVoucher](docs/PaymentDetailsCultureVoucher.md)
 - [Komoju::PaymentDetailsDana](docs/PaymentDetailsDana.md)
 - [Komoju::PaymentDetailsDocomo](docs/PaymentDetailsDocomo.md)
 - [Komoju::PaymentDetailsDokuWallet](docs/PaymentDetailsDokuWallet.md)
 - [Komoju::PaymentDetailsDospara](docs/PaymentDetailsDospara.md)
 - [Komoju::PaymentDetailsDragonpay](docs/PaymentDetailsDragonpay.md)
 - [Komoju::PaymentDetailsEnets](docs/PaymentDetailsEnets.md)
 - [Komoju::PaymentDetailsEpospay](docs/PaymentDetailsEpospay.md)
 - [Komoju::PaymentDetailsEps](docs/PaymentDetailsEps.md)
 - [Komoju::PaymentDetailsFpx](docs/PaymentDetailsFpx.md)
 - [Komoju::PaymentDetailsGCash](docs/PaymentDetailsGCash.md)
 - [Komoju::PaymentDetailsGiropay](docs/PaymentDetailsGiropay.md)
 - [Komoju::PaymentDetailsGrabpayotp](docs/PaymentDetailsGrabpayotp.md)
 - [Komoju::PaymentDetailsHappyMoney](docs/PaymentDetailsHappyMoney.md)
 - [Komoju::PaymentDetailsIdeal](docs/PaymentDetailsIdeal.md)
 - [Komoju::PaymentDetailsKakaopay](docs/PaymentDetailsKakaopay.md)
 - [Komoju::PaymentDetailsKonbini](docs/PaymentDetailsKonbini.md)
 - [Komoju::PaymentDetailsMerpay](docs/PaymentDetailsMerpay.md)
 - [Komoju::PaymentDetailsMobile](docs/PaymentDetailsMobile.md)
 - [Komoju::PaymentDetailsMobileJapan](docs/PaymentDetailsMobileJapan.md)
 - [Komoju::PaymentDetailsMultibanco](docs/PaymentDetailsMultibanco.md)
 - [Komoju::PaymentDetailsMybank](docs/PaymentDetailsMybank.md)
 - [Komoju::PaymentDetailsNarvesen](docs/PaymentDetailsNarvesen.md)
 - [Komoju::PaymentDetailsNaverpay](docs/PaymentDetailsNaverpay.md)
 - [Komoju::PaymentDetailsNetCash](docs/PaymentDetailsNetCash.md)
 - [Komoju::PaymentDetailsOnlyCreditCards](docs/PaymentDetailsOnlyCreditCards.md)
 - [Komoju::PaymentDetailsOvo](docs/PaymentDetailsOvo.md)
 - [Komoju::PaymentDetailsPaidy](docs/PaymentDetailsPaidy.md)
 - [Komoju::PaymentDetailsPayEasy](docs/PaymentDetailsPayEasy.md)
 - [Komoju::PaymentDetailsPayPay](docs/PaymentDetailsPayPay.md)
 - [Komoju::PaymentDetailsPayco](docs/PaymentDetailsPayco.md)
 - [Komoju::PaymentDetailsPaypost](docs/PaymentDetailsPaypost.md)
 - [Komoju::PaymentDetailsPaysafeCard](docs/PaymentDetailsPaysafeCard.md)
 - [Komoju::PaymentDetailsPaysafeCash](docs/PaymentDetailsPaysafeCash.md)
 - [Komoju::PaymentDetailsPaysera](docs/PaymentDetailsPaysera.md)
 - [Komoju::PaymentDetailsPayu](docs/PaymentDetailsPayu.md)
 - [Komoju::PaymentDetailsPerlas](docs/PaymentDetailsPerlas.md)
 - [Komoju::PaymentDetailsPix](docs/PaymentDetailsPix.md)
 - [Komoju::PaymentDetailsPoli](docs/PaymentDetailsPoli.md)
 - [Komoju::PaymentDetailsPrzelewy24](docs/PaymentDetailsPrzelewy24.md)
 - [Komoju::PaymentDetailsRakutenpay](docs/PaymentDetailsRakutenpay.md)
 - [Komoju::PaymentDetailsSepaTransfer](docs/PaymentDetailsSepaTransfer.md)
 - [Komoju::PaymentDetailsSofortbanking](docs/PaymentDetailsSofortbanking.md)
 - [Komoju::PaymentDetailsSoftbank](docs/PaymentDetailsSoftbank.md)
 - [Komoju::PaymentDetailsTNG](docs/PaymentDetailsTNG.md)
 - [Komoju::PaymentDetailsToss](docs/PaymentDetailsToss.md)
 - [Komoju::PaymentDetailsTruemoney](docs/PaymentDetailsTruemoney.md)
 - [Komoju::PaymentDetailsUnionpay](docs/PaymentDetailsUnionpay.md)
 - [Komoju::PaymentDetailsWebMoney](docs/PaymentDetailsWebMoney.md)
 - [Komoju::PaymentDetailsWechatpay](docs/PaymentDetailsWechatpay.md)
 - [Komoju::PaymentList](docs/PaymentList.md)
 - [Komoju::PaymentMethod](docs/PaymentMethod.md)
 - [Komoju::PaymentMethodBrands](docs/PaymentMethodBrands.md)
 - [Komoju::PaymentMethodInstallmentsInner](docs/PaymentMethodInstallmentsInner.md)
 - [Komoju::PaymentMethodStatus](docs/PaymentMethodStatus.md)
 - [Komoju::PaymentMethodsList](docs/PaymentMethodsList.md)
 - [Komoju::PaymentStatus](docs/PaymentStatus.md)
 - [Komoju::PaymentType](docs/PaymentType.md)
 - [Komoju::PlatformDetails](docs/PlatformDetails.md)
 - [Komoju::PlatformMerchantPaymentList](docs/PlatformMerchantPaymentList.md)
 - [Komoju::PlatformPayment](docs/PlatformPayment.md)
 - [Komoju::PrepaidCards](docs/PrepaidCards.md)
 - [Komoju::ProcessingMerchant](docs/ProcessingMerchant.md)
 - [Komoju::Refund](docs/Refund.md)
 - [Komoju::RefundPaymentRequest](docs/RefundPaymentRequest.md)
 - [Komoju::RefundRequest](docs/RefundRequest.md)
 - [Komoju::RefundRequestStatus](docs/RefundRequestStatus.md)
 - [Komoju::ResponsePaymentDetailsAU](docs/ResponsePaymentDetailsAU.md)
 - [Komoju::ResponsePaymentDetailsAlipay](docs/ResponsePaymentDetailsAlipay.md)
 - [Komoju::ResponsePaymentDetailsAlipayHK](docs/ResponsePaymentDetailsAlipayHK.md)
 - [Komoju::ResponsePaymentDetailsAll](docs/ResponsePaymentDetailsAll.md)
 - [Komoju::ResponsePaymentDetailsAupay](docs/ResponsePaymentDetailsAupay.md)
 - [Komoju::ResponsePaymentDetailsBancontact](docs/ResponsePaymentDetailsBancontact.md)
 - [Komoju::ResponsePaymentDetailsBankTransfer](docs/ResponsePaymentDetailsBankTransfer.md)
 - [Komoju::ResponsePaymentDetailsBitCash](docs/ResponsePaymentDetailsBitCash.md)
 - [Komoju::ResponsePaymentDetailsBlik](docs/ResponsePaymentDetailsBlik.md)
 - [Komoju::ResponsePaymentDetailsCVS](docs/ResponsePaymentDetailsCVS.md)
 - [Komoju::ResponsePaymentDetailsCreditCard](docs/ResponsePaymentDetailsCreditCard.md)
 - [Komoju::ResponsePaymentDetailsCreditCardBrazil](docs/ResponsePaymentDetailsCreditCardBrazil.md)
 - [Komoju::ResponsePaymentDetailsCreditCardKorea](docs/ResponsePaymentDetailsCreditCardKorea.md)
 - [Komoju::ResponsePaymentDetailsCreditCardTerminal](docs/ResponsePaymentDetailsCreditCardTerminal.md)
 - [Komoju::ResponsePaymentDetailsCultureVoucher](docs/ResponsePaymentDetailsCultureVoucher.md)
 - [Komoju::ResponsePaymentDetailsDana](docs/ResponsePaymentDetailsDana.md)
 - [Komoju::ResponsePaymentDetailsDocomo](docs/ResponsePaymentDetailsDocomo.md)
 - [Komoju::ResponsePaymentDetailsDokuWallet](docs/ResponsePaymentDetailsDokuWallet.md)
 - [Komoju::ResponsePaymentDetailsDospara](docs/ResponsePaymentDetailsDospara.md)
 - [Komoju::ResponsePaymentDetailsDragonpay](docs/ResponsePaymentDetailsDragonpay.md)
 - [Komoju::ResponsePaymentDetailsEnets](docs/ResponsePaymentDetailsEnets.md)
 - [Komoju::ResponsePaymentDetailsEpospay](docs/ResponsePaymentDetailsEpospay.md)
 - [Komoju::ResponsePaymentDetailsEps](docs/ResponsePaymentDetailsEps.md)
 - [Komoju::ResponsePaymentDetailsFpx](docs/ResponsePaymentDetailsFpx.md)
 - [Komoju::ResponsePaymentDetailsGCash](docs/ResponsePaymentDetailsGCash.md)
 - [Komoju::ResponsePaymentDetailsGiropay](docs/ResponsePaymentDetailsGiropay.md)
 - [Komoju::ResponsePaymentDetailsGrabpayotp](docs/ResponsePaymentDetailsGrabpayotp.md)
 - [Komoju::ResponsePaymentDetailsHappyMoney](docs/ResponsePaymentDetailsHappyMoney.md)
 - [Komoju::ResponsePaymentDetailsIdeal](docs/ResponsePaymentDetailsIdeal.md)
 - [Komoju::ResponsePaymentDetailsKakaopay](docs/ResponsePaymentDetailsKakaopay.md)
 - [Komoju::ResponsePaymentDetailsKonbini](docs/ResponsePaymentDetailsKonbini.md)
 - [Komoju::ResponsePaymentDetailsMerpay](docs/ResponsePaymentDetailsMerpay.md)
 - [Komoju::ResponsePaymentDetailsMobile](docs/ResponsePaymentDetailsMobile.md)
 - [Komoju::ResponsePaymentDetailsMobileJapan](docs/ResponsePaymentDetailsMobileJapan.md)
 - [Komoju::ResponsePaymentDetailsMultibanco](docs/ResponsePaymentDetailsMultibanco.md)
 - [Komoju::ResponsePaymentDetailsMybank](docs/ResponsePaymentDetailsMybank.md)
 - [Komoju::ResponsePaymentDetailsNarvesen](docs/ResponsePaymentDetailsNarvesen.md)
 - [Komoju::ResponsePaymentDetailsNaverpay](docs/ResponsePaymentDetailsNaverpay.md)
 - [Komoju::ResponsePaymentDetailsNetCash](docs/ResponsePaymentDetailsNetCash.md)
 - [Komoju::ResponsePaymentDetailsOvo](docs/ResponsePaymentDetailsOvo.md)
 - [Komoju::ResponsePaymentDetailsPaidy](docs/ResponsePaymentDetailsPaidy.md)
 - [Komoju::ResponsePaymentDetailsPayEasy](docs/ResponsePaymentDetailsPayEasy.md)
 - [Komoju::ResponsePaymentDetailsPayPay](docs/ResponsePaymentDetailsPayPay.md)
 - [Komoju::ResponsePaymentDetailsPayco](docs/ResponsePaymentDetailsPayco.md)
 - [Komoju::ResponsePaymentDetailsPaypost](docs/ResponsePaymentDetailsPaypost.md)
 - [Komoju::ResponsePaymentDetailsPaysafeCard](docs/ResponsePaymentDetailsPaysafeCard.md)
 - [Komoju::ResponsePaymentDetailsPaysafeCash](docs/ResponsePaymentDetailsPaysafeCash.md)
 - [Komoju::ResponsePaymentDetailsPaysera](docs/ResponsePaymentDetailsPaysera.md)
 - [Komoju::ResponsePaymentDetailsPayu](docs/ResponsePaymentDetailsPayu.md)
 - [Komoju::ResponsePaymentDetailsPerlas](docs/ResponsePaymentDetailsPerlas.md)
 - [Komoju::ResponsePaymentDetailsPix](docs/ResponsePaymentDetailsPix.md)
 - [Komoju::ResponsePaymentDetailsPoli](docs/ResponsePaymentDetailsPoli.md)
 - [Komoju::ResponsePaymentDetailsPrzelewy24](docs/ResponsePaymentDetailsPrzelewy24.md)
 - [Komoju::ResponsePaymentDetailsRakutenpay](docs/ResponsePaymentDetailsRakutenpay.md)
 - [Komoju::ResponsePaymentDetailsSepaTransfer](docs/ResponsePaymentDetailsSepaTransfer.md)
 - [Komoju::ResponsePaymentDetailsSofortbanking](docs/ResponsePaymentDetailsSofortbanking.md)
 - [Komoju::ResponsePaymentDetailsSoftbank](docs/ResponsePaymentDetailsSoftbank.md)
 - [Komoju::ResponsePaymentDetailsTNG](docs/ResponsePaymentDetailsTNG.md)
 - [Komoju::ResponsePaymentDetailsToss](docs/ResponsePaymentDetailsToss.md)
 - [Komoju::ResponsePaymentDetailsTruemoney](docs/ResponsePaymentDetailsTruemoney.md)
 - [Komoju::ResponsePaymentDetailsUnionpay](docs/ResponsePaymentDetailsUnionpay.md)
 - [Komoju::ResponsePaymentDetailsWebMoney](docs/ResponsePaymentDetailsWebMoney.md)
 - [Komoju::ResponsePaymentDetailsWechatpay](docs/ResponsePaymentDetailsWechatpay.md)
 - [Komoju::SecureToken](docs/SecureToken.md)
 - [Komoju::SerializedSubmerchant](docs/SerializedSubmerchant.md)
 - [Komoju::SerializedSubmerchantActivePaymentMethodsInner](docs/SerializedSubmerchantActivePaymentMethodsInner.md)
 - [Komoju::SerializedSubmerchantExpirySettingsInner](docs/SerializedSubmerchantExpirySettingsInner.md)
 - [Komoju::Session](docs/Session.md)
 - [Komoju::SessionMode](docs/SessionMode.md)
 - [Komoju::SessionStatus](docs/SessionStatus.md)
 - [Komoju::Settlement](docs/Settlement.md)
 - [Komoju::SettlementDownload](docs/SettlementDownload.md)
 - [Komoju::SettlementFrequency](docs/SettlementFrequency.md)
 - [Komoju::SettlementList](docs/SettlementList.md)
 - [Komoju::SettlementShow](docs/SettlementShow.md)
 - [Komoju::SharedDetails](docs/SharedDetails.md)
 - [Komoju::SharedDetailsCorrections](docs/SharedDetailsCorrections.md)
 - [Komoju::SharedDetailsDisbursements](docs/SharedDetailsDisbursements.md)
 - [Komoju::SharedDetailsMisc](docs/SharedDetailsMisc.md)
 - [Komoju::SharedDetailsPayments](docs/SharedDetailsPayments.md)
 - [Komoju::SharedDetailsPlatformModel](docs/SharedDetailsPlatformModel.md)
 - [Komoju::SharedDetailsRefunds](docs/SharedDetailsRefunds.md)
 - [Komoju::ShowBarcode200Response](docs/ShowBarcode200Response.md)
 - [Komoju::SimulateLiveApplicationPaymentMethodStatusRequest](docs/SimulateLiveApplicationPaymentMethodStatusRequest.md)
 - [Komoju::StatementDescriptor](docs/StatementDescriptor.md)
 - [Komoju::Status](docs/Status.md)
 - [Komoju::Submerchant](docs/Submerchant.md)
 - [Komoju::SubmerchantListItem](docs/SubmerchantListItem.md)
 - [Komoju::SubmerchantsList](docs/SubmerchantsList.md)
 - [Komoju::SubmittedField](docs/SubmittedField.md)
 - [Komoju::SubmittedFieldAllOfValue](docs/SubmittedFieldAllOfValue.md)
 - [Komoju::Subscription](docs/Subscription.md)
 - [Komoju::SubscriptionCustomer](docs/SubscriptionCustomer.md)
 - [Komoju::SubscriptionList](docs/SubscriptionList.md)
 - [Komoju::SubscriptionPaymentDetails](docs/SubscriptionPaymentDetails.md)
 - [Komoju::SubscriptionPeriod](docs/SubscriptionPeriod.md)
 - [Komoju::TerminalError](docs/TerminalError.md)
 - [Komoju::TerminalErrorError](docs/TerminalErrorError.md)
 - [Komoju::ThreeDsAuthResult](docs/ThreeDsAuthResult.md)
 - [Komoju::Token](docs/Token.md)
 - [Komoju::TokenPaymentDetails](docs/TokenPaymentDetails.md)
 - [Komoju::Transaction](docs/Transaction.md)
 - [Komoju::Transfer](docs/Transfer.md)
 - [Komoju::UpdateCustomerRequest](docs/UpdateCustomerRequest.md)
 - [Komoju::UpdateMerchantRequest](docs/UpdateMerchantRequest.md)
 - [Komoju::UpdateMerchantRequestExpirySettingsInner](docs/UpdateMerchantRequestExpirySettingsInner.md)
 - [Komoju::UpdatePaymentMethodRequest](docs/UpdatePaymentMethodRequest.md)
 - [Komoju::UpdatePaymentRequest](docs/UpdatePaymentRequest.md)


## Authorization


Authentication schemes defined for the API:
### api_key

- **Type**: HTTP basic authentication (API key as username, blank password)

## Support

- [KOMOJU Developer Documentation](https://docs.komoju.com)
- [KOMOJU Merchant Dashboard](https://komoju.com/merchant)
- For SDK issues, open an issue on GitHub
