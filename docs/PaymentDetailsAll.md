# Komoju::PaymentDetailsAll

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-client'

Komoju::PaymentDetailsAll.openapi_one_of
# =>
# [
#   :'PaymentDetailsAU',
#   :'PaymentDetailsAlipay',
#   :'PaymentDetailsAlipayHK',
#   :'PaymentDetailsAupay',
#   :'PaymentDetailsBancontact',
#   :'PaymentDetailsBankTransfer',
#   :'PaymentDetailsBlik',
#   :'PaymentDetailsCVS',
#   :'PaymentDetailsCreditCard',
#   :'PaymentDetailsCreditCardBrazil',
#   :'PaymentDetailsCreditCardKorea',
#   :'PaymentDetailsCreditCardTerminal',
#   :'PaymentDetailsCultureVoucher',
#   :'PaymentDetailsDana',
#   :'PaymentDetailsDocomo',
#   :'PaymentDetailsDokuWallet',
#   :'PaymentDetailsDospara',
#   :'PaymentDetailsDragonpay',
#   :'PaymentDetailsEnets',
#   :'PaymentDetailsEpospay',
#   :'PaymentDetailsEps',
#   :'PaymentDetailsFpx',
#   :'PaymentDetailsGCash',
#   :'PaymentDetailsGiropay',
#   :'PaymentDetailsGrabpayotp',
#   :'PaymentDetailsHappyMoney',
#   :'PaymentDetailsIdeal',
#   :'PaymentDetailsJapanMobile',
#   :'PaymentDetailsKakaopay',
#   :'PaymentDetailsKomojuPay',
#   :'PaymentDetailsKonbini',
#   :'PaymentDetailsMerpay',
#   :'PaymentDetailsMobile',
#   :'PaymentDetailsMultibanco',
#   :'PaymentDetailsMybank',
#   :'PaymentDetailsNarvesen',
#   :'PaymentDetailsNaverpay',
#   :'PaymentDetailsOvo',
#   :'PaymentDetailsPaidy',
#   :'PaymentDetailsPayEasy',
#   :'PaymentDetailsPayPay',
#   :'PaymentDetailsPayco',
#   :'PaymentDetailsPaypost',
#   :'PaymentDetailsPaysafeCard',
#   :'PaymentDetailsPaysafeCash',
#   :'PaymentDetailsPaysera',
#   :'PaymentDetailsPayu',
#   :'PaymentDetailsPerlas',
#   :'PaymentDetailsPix',
#   :'PaymentDetailsPoli',
#   :'PaymentDetailsPrzelewy24',
#   :'PaymentDetailsRakutenpay',
#   :'PaymentDetailsSepaTransfer',
#   :'PaymentDetailsSofortbanking',
#   :'PaymentDetailsSoftbank',
#   :'PaymentDetailsSteamPrepaidCard',
#   :'PaymentDetailsTNG',
#   :'PaymentDetailsToss',
#   :'PaymentDetailsTruemoney',
#   :'PaymentDetailsUnionpay',
#   :'PaymentDetailsWebMoney',
#   :'PaymentDetailsWechatpay'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'komoju-ruby-client'

Komoju::PaymentDetailsAll.openapi_discriminator_name
# => :'type'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-ruby-client'

Komoju::PaymentDetailsAll.openapi_discriminator_mapping
# =>
# {
#   :'alipay' => :'PaymentDetailsAlipay',
#   :'alipay_hk' => :'PaymentDetailsAlipayHK',
#   :'au' => :'PaymentDetailsAU',
#   :'aupay' => :'PaymentDetailsAupay',
#   :'bancontact' => :'PaymentDetailsBancontact',
#   :'bank_transfer' => :'PaymentDetailsBankTransfer',
#   :'blik' => :'PaymentDetailsBlik',
#   :'credit_card' => :'PaymentDetailsCreditCard',
#   :'credit_card_brazil' => :'PaymentDetailsCreditCardBrazil',
#   :'credit_card_korea' => :'PaymentDetailsCreditCardKorea',
#   :'credit_card_terminal' => :'PaymentDetailsCreditCardTerminal',
#   :'culture_voucher' => :'PaymentDetailsCultureVoucher',
#   :'cvs' => :'PaymentDetailsCVS',
#   :'dana' => :'PaymentDetailsDana',
#   :'docomo' => :'PaymentDetailsDocomo',
#   :'doku_wallet' => :'PaymentDetailsDokuWallet',
#   :'dospara' => :'PaymentDetailsDospara',
#   :'dragonpay' => :'PaymentDetailsDragonpay',
#   :'enets' => :'PaymentDetailsEnets',
#   :'epospay' => :'PaymentDetailsEpospay',
#   :'eps' => :'PaymentDetailsEps',
#   :'fpx' => :'PaymentDetailsFpx',
#   :'gcash' => :'PaymentDetailsGCash',
#   :'giropay' => :'PaymentDetailsGiropay',
#   :'grabpayotp' => :'PaymentDetailsGrabpayotp',
#   :'happy_money' => :'PaymentDetailsHappyMoney',
#   :'ideal' => :'PaymentDetailsIdeal',
#   :'japan_mobile' => :'PaymentDetailsJapanMobile',
#   :'kakaopay' => :'PaymentDetailsKakaopay',
#   :'komoju_pay' => :'PaymentDetailsKomojuPay',
#   :'konbini' => :'PaymentDetailsKonbini',
#   :'merpay' => :'PaymentDetailsMerpay',
#   :'mobile' => :'PaymentDetailsMobile',
#   :'multibanco' => :'PaymentDetailsMultibanco',
#   :'mybank' => :'PaymentDetailsMybank',
#   :'narvesen' => :'PaymentDetailsNarvesen',
#   :'naverpay' => :'PaymentDetailsNaverpay',
#   :'ovo' => :'PaymentDetailsOvo',
#   :'paidy' => :'PaymentDetailsPaidy',
#   :'pay_easy' => :'PaymentDetailsPayEasy',
#   :'payco' => :'PaymentDetailsPayco',
#   :'paypay' => :'PaymentDetailsPayPay',
#   :'paypost' => :'PaymentDetailsPaypost',
#   :'paysafe_card' => :'PaymentDetailsPaysafeCard',
#   :'paysafe_cash' => :'PaymentDetailsPaysafeCash',
#   :'paysera' => :'PaymentDetailsPaysera',
#   :'payu' => :'PaymentDetailsPayu',
#   :'perlas' => :'PaymentDetailsPerlas',
#   :'pix' => :'PaymentDetailsPix',
#   :'poli' => :'PaymentDetailsPoli',
#   :'przelewy24' => :'PaymentDetailsPrzelewy24',
#   :'rakutenpay' => :'PaymentDetailsRakutenpay',
#   :'sepa_transfer' => :'PaymentDetailsSepaTransfer',
#   :'sofortbanking' => :'PaymentDetailsSofortbanking',
#   :'softbank' => :'PaymentDetailsSoftbank',
#   :'steam_prepaid_card' => :'PaymentDetailsSteamPrepaidCard',
#   :'tng' => :'PaymentDetailsTNG',
#   :'toss' => :'PaymentDetailsToss',
#   :'truemoney' => :'PaymentDetailsTruemoney',
#   :'unionpay' => :'PaymentDetailsUnionpay',
#   :'web_money' => :'PaymentDetailsWebMoney',
#   :'wechatpay' => :'PaymentDetailsWechatpay'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-client'

Komoju::PaymentDetailsAll.build(data)
# => #<PaymentDetailsAU:0x00007fdd4aab02a0>

Komoju::PaymentDetailsAll.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `PaymentDetailsAU`
- `PaymentDetailsAlipay`
- `PaymentDetailsAlipayHK`
- `PaymentDetailsAupay`
- `PaymentDetailsBancontact`
- `PaymentDetailsBankTransfer`
- `PaymentDetailsBlik`
- `PaymentDetailsCVS`
- `PaymentDetailsCreditCard`
- `PaymentDetailsCreditCardBrazil`
- `PaymentDetailsCreditCardKorea`
- `PaymentDetailsCreditCardTerminal`
- `PaymentDetailsCultureVoucher`
- `PaymentDetailsDana`
- `PaymentDetailsDocomo`
- `PaymentDetailsDokuWallet`
- `PaymentDetailsDospara`
- `PaymentDetailsDragonpay`
- `PaymentDetailsEnets`
- `PaymentDetailsEpospay`
- `PaymentDetailsEps`
- `PaymentDetailsFpx`
- `PaymentDetailsGCash`
- `PaymentDetailsGiropay`
- `PaymentDetailsGrabpayotp`
- `PaymentDetailsHappyMoney`
- `PaymentDetailsIdeal`
- `PaymentDetailsJapanMobile`
- `PaymentDetailsKakaopay`
- `PaymentDetailsKomojuPay`
- `PaymentDetailsKonbini`
- `PaymentDetailsMerpay`
- `PaymentDetailsMobile`
- `PaymentDetailsMultibanco`
- `PaymentDetailsMybank`
- `PaymentDetailsNarvesen`
- `PaymentDetailsNaverpay`
- `PaymentDetailsOvo`
- `PaymentDetailsPaidy`
- `PaymentDetailsPayEasy`
- `PaymentDetailsPayPay`
- `PaymentDetailsPayco`
- `PaymentDetailsPaypost`
- `PaymentDetailsPaysafeCard`
- `PaymentDetailsPaysafeCash`
- `PaymentDetailsPaysera`
- `PaymentDetailsPayu`
- `PaymentDetailsPerlas`
- `PaymentDetailsPix`
- `PaymentDetailsPoli`
- `PaymentDetailsPrzelewy24`
- `PaymentDetailsRakutenpay`
- `PaymentDetailsSepaTransfer`
- `PaymentDetailsSofortbanking`
- `PaymentDetailsSoftbank`
- `PaymentDetailsSteamPrepaidCard`
- `PaymentDetailsTNG`
- `PaymentDetailsToss`
- `PaymentDetailsTruemoney`
- `PaymentDetailsUnionpay`
- `PaymentDetailsWebMoney`
- `PaymentDetailsWechatpay`
- `nil` (if no type matches)

