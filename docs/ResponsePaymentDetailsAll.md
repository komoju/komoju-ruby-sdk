# Komoju::ResponsePaymentDetailsAll

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ResponsePaymentDetailsAll.openapi_one_of
# =>
# [
#   :'ResponsePaymentDetailsAU',
#   :'ResponsePaymentDetailsAlipay',
#   :'ResponsePaymentDetailsAlipayHK',
#   :'ResponsePaymentDetailsAupay',
#   :'ResponsePaymentDetailsBancontact',
#   :'ResponsePaymentDetailsBankTransfer',
#   :'ResponsePaymentDetailsBitCash',
#   :'ResponsePaymentDetailsBlik',
#   :'ResponsePaymentDetailsCVS',
#   :'ResponsePaymentDetailsCreditCard',
#   :'ResponsePaymentDetailsCreditCardBrazil',
#   :'ResponsePaymentDetailsCreditCardKorea',
#   :'ResponsePaymentDetailsCreditCardTerminal',
#   :'ResponsePaymentDetailsCultureVoucher',
#   :'ResponsePaymentDetailsDana',
#   :'ResponsePaymentDetailsDocomo',
#   :'ResponsePaymentDetailsDokuWallet',
#   :'ResponsePaymentDetailsDospara',
#   :'ResponsePaymentDetailsDragonpay',
#   :'ResponsePaymentDetailsEnets',
#   :'ResponsePaymentDetailsEpospay',
#   :'ResponsePaymentDetailsEps',
#   :'ResponsePaymentDetailsFpx',
#   :'ResponsePaymentDetailsGCash',
#   :'ResponsePaymentDetailsGiropay',
#   :'ResponsePaymentDetailsGrabpayotp',
#   :'ResponsePaymentDetailsHappyMoney',
#   :'ResponsePaymentDetailsIdeal',
#   :'ResponsePaymentDetailsKakaopay',
#   :'ResponsePaymentDetailsKonbini',
#   :'ResponsePaymentDetailsMerpay',
#   :'ResponsePaymentDetailsMobile',
#   :'ResponsePaymentDetailsMobileJapan',
#   :'ResponsePaymentDetailsMultibanco',
#   :'ResponsePaymentDetailsMybank',
#   :'ResponsePaymentDetailsNarvesen',
#   :'ResponsePaymentDetailsNaverpay',
#   :'ResponsePaymentDetailsNetCash',
#   :'ResponsePaymentDetailsOvo',
#   :'ResponsePaymentDetailsPaidy',
#   :'ResponsePaymentDetailsPayEasy',
#   :'ResponsePaymentDetailsPayPay',
#   :'ResponsePaymentDetailsPayco',
#   :'ResponsePaymentDetailsPaypost',
#   :'ResponsePaymentDetailsPaysafeCard',
#   :'ResponsePaymentDetailsPaysafeCash',
#   :'ResponsePaymentDetailsPaysera',
#   :'ResponsePaymentDetailsPayu',
#   :'ResponsePaymentDetailsPerlas',
#   :'ResponsePaymentDetailsPix',
#   :'ResponsePaymentDetailsPoli',
#   :'ResponsePaymentDetailsPrzelewy24',
#   :'ResponsePaymentDetailsRakutenpay',
#   :'ResponsePaymentDetailsSepaTransfer',
#   :'ResponsePaymentDetailsSofortbanking',
#   :'ResponsePaymentDetailsSoftbank',
#   :'ResponsePaymentDetailsTNG',
#   :'ResponsePaymentDetailsToss',
#   :'ResponsePaymentDetailsTruemoney',
#   :'ResponsePaymentDetailsUnionpay',
#   :'ResponsePaymentDetailsWebMoney',
#   :'ResponsePaymentDetailsWechatpay'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ResponsePaymentDetailsAll.openapi_discriminator_name
# => :'type'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ResponsePaymentDetailsAll.openapi_discriminator_mapping
# =>
# {
#   :'alipay' => :'ResponsePaymentDetailsAlipay',
#   :'alipay_hk' => :'ResponsePaymentDetailsAlipayHK',
#   :'au' => :'ResponsePaymentDetailsAU',
#   :'aupay' => :'ResponsePaymentDetailsAupay',
#   :'bancontact' => :'ResponsePaymentDetailsBancontact',
#   :'bank_transfer' => :'ResponsePaymentDetailsBankTransfer',
#   :'bit_cash' => :'ResponsePaymentDetailsBitCash',
#   :'blik' => :'ResponsePaymentDetailsBlik',
#   :'credit_card' => :'ResponsePaymentDetailsCreditCard',
#   :'credit_card_brazil' => :'ResponsePaymentDetailsCreditCardBrazil',
#   :'credit_card_korea' => :'ResponsePaymentDetailsCreditCardKorea',
#   :'credit_card_terminal' => :'ResponsePaymentDetailsCreditCardTerminal',
#   :'culture_voucher' => :'ResponsePaymentDetailsCultureVoucher',
#   :'cvs' => :'ResponsePaymentDetailsCVS',
#   :'dana' => :'ResponsePaymentDetailsDana',
#   :'docomo' => :'ResponsePaymentDetailsDocomo',
#   :'doku_wallet' => :'ResponsePaymentDetailsDokuWallet',
#   :'dospara' => :'ResponsePaymentDetailsDospara',
#   :'dragonpay' => :'ResponsePaymentDetailsDragonpay',
#   :'enets' => :'ResponsePaymentDetailsEnets',
#   :'epospay' => :'ResponsePaymentDetailsEpospay',
#   :'eps' => :'ResponsePaymentDetailsEps',
#   :'fpx' => :'ResponsePaymentDetailsFpx',
#   :'gcash' => :'ResponsePaymentDetailsGCash',
#   :'giropay' => :'ResponsePaymentDetailsGiropay',
#   :'grabpayotp' => :'ResponsePaymentDetailsGrabpayotp',
#   :'happy_money' => :'ResponsePaymentDetailsHappyMoney',
#   :'ideal' => :'ResponsePaymentDetailsIdeal',
#   :'japan_mobile' => :'ResponsePaymentDetailsMobileJapan',
#   :'kakaopay' => :'ResponsePaymentDetailsKakaopay',
#   :'konbini' => :'ResponsePaymentDetailsKonbini',
#   :'merpay' => :'ResponsePaymentDetailsMerpay',
#   :'mobile' => :'ResponsePaymentDetailsMobile',
#   :'multibanco' => :'ResponsePaymentDetailsMultibanco',
#   :'mybank' => :'ResponsePaymentDetailsMybank',
#   :'narvesen' => :'ResponsePaymentDetailsNarvesen',
#   :'naverpay' => :'ResponsePaymentDetailsNaverpay',
#   :'net_cash' => :'ResponsePaymentDetailsNetCash',
#   :'ovo' => :'ResponsePaymentDetailsOvo',
#   :'paidy' => :'ResponsePaymentDetailsPaidy',
#   :'pay_easy' => :'ResponsePaymentDetailsPayEasy',
#   :'payco' => :'ResponsePaymentDetailsPayco',
#   :'paypay' => :'ResponsePaymentDetailsPayPay',
#   :'paypost' => :'ResponsePaymentDetailsPaypost',
#   :'paysafe_card' => :'ResponsePaymentDetailsPaysafeCard',
#   :'paysafe_cash' => :'ResponsePaymentDetailsPaysafeCash',
#   :'paysera' => :'ResponsePaymentDetailsPaysera',
#   :'payu' => :'ResponsePaymentDetailsPayu',
#   :'perlas' => :'ResponsePaymentDetailsPerlas',
#   :'pix' => :'ResponsePaymentDetailsPix',
#   :'poli' => :'ResponsePaymentDetailsPoli',
#   :'przelewy24' => :'ResponsePaymentDetailsPrzelewy24',
#   :'rakutenpay' => :'ResponsePaymentDetailsRakutenpay',
#   :'sepa_transfer' => :'ResponsePaymentDetailsSepaTransfer',
#   :'sofortbanking' => :'ResponsePaymentDetailsSofortbanking',
#   :'softbank' => :'ResponsePaymentDetailsSoftbank',
#   :'tng' => :'ResponsePaymentDetailsTNG',
#   :'toss' => :'ResponsePaymentDetailsToss',
#   :'truemoney' => :'ResponsePaymentDetailsTruemoney',
#   :'unionpay' => :'ResponsePaymentDetailsUnionpay',
#   :'web_money' => :'ResponsePaymentDetailsWebMoney',
#   :'wechatpay' => :'ResponsePaymentDetailsWechatpay'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ResponsePaymentDetailsAll.build(data)
# => #<ResponsePaymentDetailsAU:0x00007fdd4aab02a0>

Komoju::ResponsePaymentDetailsAll.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `ResponsePaymentDetailsAU`
- `ResponsePaymentDetailsAlipay`
- `ResponsePaymentDetailsAlipayHK`
- `ResponsePaymentDetailsAupay`
- `ResponsePaymentDetailsBancontact`
- `ResponsePaymentDetailsBankTransfer`
- `ResponsePaymentDetailsBitCash`
- `ResponsePaymentDetailsBlik`
- `ResponsePaymentDetailsCVS`
- `ResponsePaymentDetailsCreditCard`
- `ResponsePaymentDetailsCreditCardBrazil`
- `ResponsePaymentDetailsCreditCardKorea`
- `ResponsePaymentDetailsCreditCardTerminal`
- `ResponsePaymentDetailsCultureVoucher`
- `ResponsePaymentDetailsDana`
- `ResponsePaymentDetailsDocomo`
- `ResponsePaymentDetailsDokuWallet`
- `ResponsePaymentDetailsDospara`
- `ResponsePaymentDetailsDragonpay`
- `ResponsePaymentDetailsEnets`
- `ResponsePaymentDetailsEpospay`
- `ResponsePaymentDetailsEps`
- `ResponsePaymentDetailsFpx`
- `ResponsePaymentDetailsGCash`
- `ResponsePaymentDetailsGiropay`
- `ResponsePaymentDetailsGrabpayotp`
- `ResponsePaymentDetailsHappyMoney`
- `ResponsePaymentDetailsIdeal`
- `ResponsePaymentDetailsKakaopay`
- `ResponsePaymentDetailsKonbini`
- `ResponsePaymentDetailsMerpay`
- `ResponsePaymentDetailsMobile`
- `ResponsePaymentDetailsMobileJapan`
- `ResponsePaymentDetailsMultibanco`
- `ResponsePaymentDetailsMybank`
- `ResponsePaymentDetailsNarvesen`
- `ResponsePaymentDetailsNaverpay`
- `ResponsePaymentDetailsNetCash`
- `ResponsePaymentDetailsOvo`
- `ResponsePaymentDetailsPaidy`
- `ResponsePaymentDetailsPayEasy`
- `ResponsePaymentDetailsPayPay`
- `ResponsePaymentDetailsPayco`
- `ResponsePaymentDetailsPaypost`
- `ResponsePaymentDetailsPaysafeCard`
- `ResponsePaymentDetailsPaysafeCash`
- `ResponsePaymentDetailsPaysera`
- `ResponsePaymentDetailsPayu`
- `ResponsePaymentDetailsPerlas`
- `ResponsePaymentDetailsPix`
- `ResponsePaymentDetailsPoli`
- `ResponsePaymentDetailsPrzelewy24`
- `ResponsePaymentDetailsRakutenpay`
- `ResponsePaymentDetailsSepaTransfer`
- `ResponsePaymentDetailsSofortbanking`
- `ResponsePaymentDetailsSoftbank`
- `ResponsePaymentDetailsTNG`
- `ResponsePaymentDetailsToss`
- `ResponsePaymentDetailsTruemoney`
- `ResponsePaymentDetailsUnionpay`
- `ResponsePaymentDetailsWebMoney`
- `ResponsePaymentDetailsWechatpay`
- `nil` (if no type matches)

