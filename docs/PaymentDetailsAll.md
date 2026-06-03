# Komoju::PaymentDetailsAll

## Concrete types

Use one of the following classes when constructing a `PaymentDetailsAll`:

- [**PaymentDetailsAU**](PaymentDetailsAU.md)
- [**PaymentDetailsAlipay**](PaymentDetailsAlipay.md)
- [**PaymentDetailsAlipayHK**](PaymentDetailsAlipayHK.md)
- [**PaymentDetailsAupay**](PaymentDetailsAupay.md)
- [**PaymentDetailsBancontact**](PaymentDetailsBancontact.md)
- [**PaymentDetailsBankTransfer**](PaymentDetailsBankTransfer.md)
- [**PaymentDetailsBitCash**](PaymentDetailsBitCash.md)
- [**PaymentDetailsBlik**](PaymentDetailsBlik.md)
- [**PaymentDetailsCVS**](PaymentDetailsCVS.md)
- [**PaymentDetailsCreditCard**](PaymentDetailsCreditCard.md)
- [**PaymentDetailsCreditCardBrazil**](PaymentDetailsCreditCardBrazil.md)
- [**PaymentDetailsCreditCardKorea**](PaymentDetailsCreditCardKorea.md)
- [**PaymentDetailsCreditCardTerminal**](PaymentDetailsCreditCardTerminal.md)
- [**PaymentDetailsCultureVoucher**](PaymentDetailsCultureVoucher.md)
- [**PaymentDetailsDana**](PaymentDetailsDana.md)
- [**PaymentDetailsDocomo**](PaymentDetailsDocomo.md)
- [**PaymentDetailsDokuWallet**](PaymentDetailsDokuWallet.md)
- [**PaymentDetailsDospara**](PaymentDetailsDospara.md)
- [**PaymentDetailsDragonpay**](PaymentDetailsDragonpay.md)
- [**PaymentDetailsEnets**](PaymentDetailsEnets.md)
- [**PaymentDetailsEpospay**](PaymentDetailsEpospay.md)
- [**PaymentDetailsEps**](PaymentDetailsEps.md)
- [**PaymentDetailsFpx**](PaymentDetailsFpx.md)
- [**PaymentDetailsGCash**](PaymentDetailsGCash.md)
- [**PaymentDetailsGiropay**](PaymentDetailsGiropay.md)
- [**PaymentDetailsHappyMoney**](PaymentDetailsHappyMoney.md)
- [**PaymentDetailsIdeal**](PaymentDetailsIdeal.md)
- [**PaymentDetailsKakaopay**](PaymentDetailsKakaopay.md)
- [**PaymentDetailsKonbini**](PaymentDetailsKonbini.md)
- [**PaymentDetailsMerpay**](PaymentDetailsMerpay.md)
- [**PaymentDetailsMobile**](PaymentDetailsMobile.md)
- [**PaymentDetailsMobileJapan**](PaymentDetailsMobileJapan.md)
- [**PaymentDetailsMultibanco**](PaymentDetailsMultibanco.md)
- [**PaymentDetailsMybank**](PaymentDetailsMybank.md)
- [**PaymentDetailsNarvesen**](PaymentDetailsNarvesen.md)
- [**PaymentDetailsNaverpay**](PaymentDetailsNaverpay.md)
- [**PaymentDetailsNetCash**](PaymentDetailsNetCash.md)
- [**PaymentDetailsOvo**](PaymentDetailsOvo.md)
- [**PaymentDetailsPaidy**](PaymentDetailsPaidy.md)
- [**PaymentDetailsPayEasy**](PaymentDetailsPayEasy.md)
- [**PaymentDetailsPayPay**](PaymentDetailsPayPay.md)
- [**PaymentDetailsPayco**](PaymentDetailsPayco.md)
- [**PaymentDetailsPaypost**](PaymentDetailsPaypost.md)
- [**PaymentDetailsPaysafeCard**](PaymentDetailsPaysafeCard.md)
- [**PaymentDetailsPaysafeCash**](PaymentDetailsPaysafeCash.md)
- [**PaymentDetailsPaysera**](PaymentDetailsPaysera.md)
- [**PaymentDetailsPayu**](PaymentDetailsPayu.md)
- [**PaymentDetailsPerlas**](PaymentDetailsPerlas.md)
- [**PaymentDetailsPix**](PaymentDetailsPix.md)
- [**PaymentDetailsPoli**](PaymentDetailsPoli.md)
- [**PaymentDetailsPrzelewy24**](PaymentDetailsPrzelewy24.md)
- [**PaymentDetailsRakutenpay**](PaymentDetailsRakutenpay.md)
- [**PaymentDetailsSepaTransfer**](PaymentDetailsSepaTransfer.md)
- [**PaymentDetailsSofortbanking**](PaymentDetailsSofortbanking.md)
- [**PaymentDetailsSoftbank**](PaymentDetailsSoftbank.md)
- [**PaymentDetailsTNG**](PaymentDetailsTNG.md)
- [**PaymentDetailsToss**](PaymentDetailsToss.md)
- [**PaymentDetailsTruemoney**](PaymentDetailsTruemoney.md)
- [**PaymentDetailsUnionpay**](PaymentDetailsUnionpay.md)
- [**PaymentDetailsWebMoney**](PaymentDetailsWebMoney.md)
- [**PaymentDetailsWechatpay**](PaymentDetailsWechatpay.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-sdk'

Komoju::PaymentDetailsAll.openapi_one_of
# =>
# [
#   :'PaymentDetailsAU',
#   :'PaymentDetailsAlipay',
#   :'PaymentDetailsAlipayHK',
#   :'PaymentDetailsAupay',
#   :'PaymentDetailsBancontact',
#   :'PaymentDetailsBankTransfer',
#   :'PaymentDetailsBitCash',
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
#   :'PaymentDetailsHappyMoney',
#   :'PaymentDetailsIdeal',
#   :'PaymentDetailsKakaopay',
#   :'PaymentDetailsKonbini',
#   :'PaymentDetailsMerpay',
#   :'PaymentDetailsMobile',
#   :'PaymentDetailsMobileJapan',
#   :'PaymentDetailsMultibanco',
#   :'PaymentDetailsMybank',
#   :'PaymentDetailsNarvesen',
#   :'PaymentDetailsNaverpay',
#   :'PaymentDetailsNetCash',
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
require 'komoju-sdk'

Komoju::PaymentDetailsAll.openapi_discriminator_name
# => :'type'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-sdk'

Komoju::PaymentDetailsAll.openapi_discriminator_mapping
# =>
# {
#   :'alipay' => :'PaymentDetailsAlipay',
#   :'alipay_hk' => :'PaymentDetailsAlipayHK',
#   :'au' => :'PaymentDetailsAU',
#   :'aupay' => :'PaymentDetailsAupay',
#   :'bancontact' => :'PaymentDetailsBancontact',
#   :'bank_transfer' => :'PaymentDetailsBankTransfer',
#   :'bit_cash' => :'PaymentDetailsBitCash',
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
#   :'happy_money' => :'PaymentDetailsHappyMoney',
#   :'ideal' => :'PaymentDetailsIdeal',
#   :'japan_mobile' => :'PaymentDetailsMobileJapan',
#   :'kakaopay' => :'PaymentDetailsKakaopay',
#   :'konbini' => :'PaymentDetailsKonbini',
#   :'merpay' => :'PaymentDetailsMerpay',
#   :'mobile' => :'PaymentDetailsMobile',
#   :'multibanco' => :'PaymentDetailsMultibanco',
#   :'mybank' => :'PaymentDetailsMybank',
#   :'narvesen' => :'PaymentDetailsNarvesen',
#   :'naverpay' => :'PaymentDetailsNaverpay',
#   :'net_cash' => :'PaymentDetailsNetCash',
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
require 'komoju-sdk'

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

- [PaymentDetailsAU](PaymentDetailsAU.md)
- [PaymentDetailsAlipay](PaymentDetailsAlipay.md)
- [PaymentDetailsAlipayHK](PaymentDetailsAlipayHK.md)
- [PaymentDetailsAupay](PaymentDetailsAupay.md)
- [PaymentDetailsBancontact](PaymentDetailsBancontact.md)
- [PaymentDetailsBankTransfer](PaymentDetailsBankTransfer.md)
- [PaymentDetailsBitCash](PaymentDetailsBitCash.md)
- [PaymentDetailsBlik](PaymentDetailsBlik.md)
- [PaymentDetailsCVS](PaymentDetailsCVS.md)
- [PaymentDetailsCreditCard](PaymentDetailsCreditCard.md)
- [PaymentDetailsCreditCardBrazil](PaymentDetailsCreditCardBrazil.md)
- [PaymentDetailsCreditCardKorea](PaymentDetailsCreditCardKorea.md)
- [PaymentDetailsCreditCardTerminal](PaymentDetailsCreditCardTerminal.md)
- [PaymentDetailsCultureVoucher](PaymentDetailsCultureVoucher.md)
- [PaymentDetailsDana](PaymentDetailsDana.md)
- [PaymentDetailsDocomo](PaymentDetailsDocomo.md)
- [PaymentDetailsDokuWallet](PaymentDetailsDokuWallet.md)
- [PaymentDetailsDospara](PaymentDetailsDospara.md)
- [PaymentDetailsDragonpay](PaymentDetailsDragonpay.md)
- [PaymentDetailsEnets](PaymentDetailsEnets.md)
- [PaymentDetailsEpospay](PaymentDetailsEpospay.md)
- [PaymentDetailsEps](PaymentDetailsEps.md)
- [PaymentDetailsFpx](PaymentDetailsFpx.md)
- [PaymentDetailsGCash](PaymentDetailsGCash.md)
- [PaymentDetailsGiropay](PaymentDetailsGiropay.md)
- [PaymentDetailsHappyMoney](PaymentDetailsHappyMoney.md)
- [PaymentDetailsIdeal](PaymentDetailsIdeal.md)
- [PaymentDetailsKakaopay](PaymentDetailsKakaopay.md)
- [PaymentDetailsKonbini](PaymentDetailsKonbini.md)
- [PaymentDetailsMerpay](PaymentDetailsMerpay.md)
- [PaymentDetailsMobile](PaymentDetailsMobile.md)
- [PaymentDetailsMobileJapan](PaymentDetailsMobileJapan.md)
- [PaymentDetailsMultibanco](PaymentDetailsMultibanco.md)
- [PaymentDetailsMybank](PaymentDetailsMybank.md)
- [PaymentDetailsNarvesen](PaymentDetailsNarvesen.md)
- [PaymentDetailsNaverpay](PaymentDetailsNaverpay.md)
- [PaymentDetailsNetCash](PaymentDetailsNetCash.md)
- [PaymentDetailsOvo](PaymentDetailsOvo.md)
- [PaymentDetailsPaidy](PaymentDetailsPaidy.md)
- [PaymentDetailsPayEasy](PaymentDetailsPayEasy.md)
- [PaymentDetailsPayPay](PaymentDetailsPayPay.md)
- [PaymentDetailsPayco](PaymentDetailsPayco.md)
- [PaymentDetailsPaypost](PaymentDetailsPaypost.md)
- [PaymentDetailsPaysafeCard](PaymentDetailsPaysafeCard.md)
- [PaymentDetailsPaysafeCash](PaymentDetailsPaysafeCash.md)
- [PaymentDetailsPaysera](PaymentDetailsPaysera.md)
- [PaymentDetailsPayu](PaymentDetailsPayu.md)
- [PaymentDetailsPerlas](PaymentDetailsPerlas.md)
- [PaymentDetailsPix](PaymentDetailsPix.md)
- [PaymentDetailsPoli](PaymentDetailsPoli.md)
- [PaymentDetailsPrzelewy24](PaymentDetailsPrzelewy24.md)
- [PaymentDetailsRakutenpay](PaymentDetailsRakutenpay.md)
- [PaymentDetailsSepaTransfer](PaymentDetailsSepaTransfer.md)
- [PaymentDetailsSofortbanking](PaymentDetailsSofortbanking.md)
- [PaymentDetailsSoftbank](PaymentDetailsSoftbank.md)
- [PaymentDetailsTNG](PaymentDetailsTNG.md)
- [PaymentDetailsToss](PaymentDetailsToss.md)
- [PaymentDetailsTruemoney](PaymentDetailsTruemoney.md)
- [PaymentDetailsUnionpay](PaymentDetailsUnionpay.md)
- [PaymentDetailsWebMoney](PaymentDetailsWebMoney.md)
- [PaymentDetailsWechatpay](PaymentDetailsWechatpay.md)
- `nil` (if no type matches)

