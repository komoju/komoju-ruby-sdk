# Komoju::LiveApplicationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **locale** | [**Locale**](Locale.md) |  | [optional] |
| **service_agreement_agreed_to_tos** | **Boolean** |  | [optional] |
| **company_information_company_name** | **String** |  | [optional] |
| **company_information_company_phone** | **String** |  | [optional] |
| **company_information_company_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **company_information_corporation_type** | **String** |  | [optional] |
| **company_information_company_postal_code** | **String** |  | [optional] |
| **company_information_company_prefecture_state** | **String** |  | [optional] |
| **company_information_company_prefecture_state_kana** | **String** |  | [optional] |
| **company_information_company_city** | **String** |  | [optional] |
| **company_information_company_city_kana** | **String** |  | [optional] |
| **company_information_company_address** | **String** |  | [optional] |
| **company_information_industry_description** | **String** |  | [optional] |
| **company_information_business_description** | **String** |  | [optional] |
| **company_information_employee_number** | **String** |  | [optional] |
| **company_information_establishment_date** | **String** |  | [optional] |
| **company_information_office_name** | **String** |  | [optional] |
| **company_information_contact_email** | **String** |  | [optional] |
| **company_information_contact_phone** | **String** |  | [optional] |
| **company_information_incorporation_certificates** | **Array&lt;String&gt;** |  | [optional] |
| **company_information_registration_number** | **String** |  | [optional] |
| **company_information_share_capital_amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **company_information_share_capital_currency** | [**Currency**](Currency.md) |  | [optional] |
| **company_information_sole_proprietor_proofs** | **Array&lt;String&gt;** |  | [optional] |
| **company_information_company_name_kana** | **String** |  | [optional] |
| **company_information_company_name_alphabet** | **String** |  | [optional] |
| **company_information_company_url** | **String** |  | [optional] |
| **company_information_company_address_kana** | **String** |  | [optional] |
| **company_information_company_address_building_name** | **String** |  | [optional] |
| **company_information_company_address_building_name_kana** | **String** |  | [optional] |
| **representative_director_information_first_name** | **String** |  | [optional] |
| **representative_director_information_first_name_kana** | **String** |  | [optional] |
| **representative_director_information_last_name** | **String** |  | [optional] |
| **representative_director_information_last_name_kana** | **String** |  | [optional] |
| **representative_director_information_date_of_birth** | **String** |  | [optional] |
| **representative_director_information_gender** | **String** |  | [optional] |
| **representative_director_information_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **representative_director_information_postal_code** | **String** |  | [optional] |
| **representative_director_information_prefecture_state** | **String** |  | [optional] |
| **representative_director_information_prefecture_state_kana** | **String** |  | [optional] |
| **representative_director_information_city** | **String** |  | [optional] |
| **representative_director_information_city_kana** | **String** |  | [optional] |
| **representative_director_information_address** | **String** |  | [optional] |
| **representative_director_information_address_kana** | **String** |  | [optional] |
| **representative_director_information_address_building_name** | **String** |  | [optional] |
| **representative_director_information_address_building_name_kana** | **String** |  | [optional] |
| **representative_director_information_phone** | **String** |  | [optional] |
| **applicant_information_first_name** | **String** |  | [optional] |
| **applicant_information_first_name_kana** | **String** |  | [optional] |
| **applicant_information_last_name** | **String** |  | [optional] |
| **applicant_information_last_name_kana** | **String** |  | [optional] |
| **applicant_information_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **applicant_information_gender** | **String** |  | [optional] |
| **applicant_information_date_of_birth** | **String** |  | [optional] |
| **applicant_information_identity_document_type** | **String** |  | [optional] |
| **applicant_information_identity_front** | **String** |  | [optional] |
| **applicant_information_identity_back** | **String** |  | [optional] |
| **site_information_site_name** | **String** |  | [optional] |
| **site_information_site_name_kana** | **String** |  | [optional] |
| **site_information_site_name_alphabet** | **String** |  | [optional] |
| **site_information_site_url** | **String** |  | [optional] |
| **site_information_establishment_date** | **String** |  | [optional] |
| **site_information_store_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **site_information_store_postal_code** | **String** |  | [optional] |
| **site_information_store_prefecture_state** | **String** |  | [optional] |
| **site_information_store_prefecture_state_kana** | **String** |  | [optional] |
| **site_information_store_city** | **String** |  | [optional] |
| **site_information_store_city_kana** | **String** |  | [optional] |
| **site_information_store_address** | **String** |  | [optional] |
| **site_information_store_address_kana** | **String** |  | [optional] |
| **site_information_store_building_name** | **String** |  | [optional] |
| **site_information_store_building_name_kana** | **String** |  | [optional] |
| **site_information_site_product_description** | **String** |  | [optional] |
| **site_information_site_annual_sales** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **site_information_site_annual_sales_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_site_average_transactional_value** | **String** |  | [optional] |
| **site_information_site_average_transactional_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_site_minimum_product_pricing_cents** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **site_information_site_minimum_product_pricing_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_site_maximum_product_pricing_cents** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **site_information_site_maximum_product_pricing_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_sctl_url** | **String** |  | [optional] |
| **site_information_sales_permit_required** | **Boolean** |  | [optional] |
| **site_information_aup_accepted** | **Boolean** |  | [optional] |
| **site_information_industry_type** | [**IndustryType**](IndustryType.md) |  | [optional] |
| **site_information_sales_permits** | **Array&lt;String&gt;** |  | [optional] |
| **bank_account_information_zengin_bank_name** | **String** |  | [optional] |
| **bank_account_information_zengin_bank_code** | **String** |  | [optional] |
| **bank_account_information_zengin_branch_name** | **String** |  | [optional] |
| **bank_account_information_zengin_branch_code** | **String** |  | [optional] |
| **bank_account_information_zengin_account_type** | **String** |  | [optional] |
| **bank_account_information_zengin_account_number** | **String** |  | [optional] |
| **bank_account_information_zengin_account_holder_kana** | **String** |  | [optional] |
| **bank_account_information_transfer_type** | **String** |  | [optional] |
| **bank_account_information_currency** | [**Currency**](Currency.md) |  | [optional] |
| **bank_account_information_default_frequency** | [**SettlementFrequency**](SettlementFrequency.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::LiveApplicationRequest.new(
  locale: null,
  service_agreement_agreed_to_tos: null,
  company_information_company_name: null,
  company_information_company_phone: null,
  company_information_company_country: null,
  company_information_corporation_type: null,
  company_information_company_postal_code: null,
  company_information_company_prefecture_state: null,
  company_information_company_prefecture_state_kana: null,
  company_information_company_city: null,
  company_information_company_city_kana: null,
  company_information_company_address: null,
  company_information_industry_description: null,
  company_information_business_description: null,
  company_information_employee_number: null,
  company_information_establishment_date: null,
  company_information_office_name: null,
  company_information_contact_email: null,
  company_information_contact_phone: null,
  company_information_incorporation_certificates: null,
  company_information_registration_number: null,
  company_information_share_capital_amount: null,
  company_information_share_capital_currency: null,
  company_information_sole_proprietor_proofs: null,
  company_information_company_name_kana: null,
  company_information_company_name_alphabet: null,
  company_information_company_url: null,
  company_information_company_address_kana: null,
  company_information_company_address_building_name: null,
  company_information_company_address_building_name_kana: null,
  representative_director_information_first_name: null,
  representative_director_information_first_name_kana: null,
  representative_director_information_last_name: null,
  representative_director_information_last_name_kana: null,
  representative_director_information_date_of_birth: null,
  representative_director_information_gender: null,
  representative_director_information_country: null,
  representative_director_information_postal_code: null,
  representative_director_information_prefecture_state: null,
  representative_director_information_prefecture_state_kana: null,
  representative_director_information_city: null,
  representative_director_information_city_kana: null,
  representative_director_information_address: null,
  representative_director_information_address_kana: null,
  representative_director_information_address_building_name: null,
  representative_director_information_address_building_name_kana: null,
  representative_director_information_phone: null,
  applicant_information_first_name: null,
  applicant_information_first_name_kana: null,
  applicant_information_last_name: null,
  applicant_information_last_name_kana: null,
  applicant_information_country: null,
  applicant_information_gender: null,
  applicant_information_date_of_birth: null,
  applicant_information_identity_document_type: null,
  applicant_information_identity_front: null,
  applicant_information_identity_back: null,
  site_information_site_name: null,
  site_information_site_name_kana: null,
  site_information_site_name_alphabet: null,
  site_information_site_url: null,
  site_information_establishment_date: null,
  site_information_store_country: null,
  site_information_store_postal_code: null,
  site_information_store_prefecture_state: null,
  site_information_store_prefecture_state_kana: null,
  site_information_store_city: null,
  site_information_store_city_kana: null,
  site_information_store_address: null,
  site_information_store_address_kana: null,
  site_information_store_building_name: null,
  site_information_store_building_name_kana: null,
  site_information_site_product_description: null,
  site_information_site_annual_sales: null,
  site_information_site_annual_sales_currency: null,
  site_information_site_average_transactional_value: null,
  site_information_site_average_transactional_currency: null,
  site_information_site_minimum_product_pricing_cents: null,
  site_information_site_minimum_product_pricing_currency: null,
  site_information_site_maximum_product_pricing_cents: null,
  site_information_site_maximum_product_pricing_currency: null,
  site_information_sctl_url: null,
  site_information_sales_permit_required: null,
  site_information_aup_accepted: null,
  site_information_industry_type: null,
  site_information_sales_permits: null,
  bank_account_information_zengin_bank_name: null,
  bank_account_information_zengin_bank_code: null,
  bank_account_information_zengin_branch_name: null,
  bank_account_information_zengin_branch_code: null,
  bank_account_information_zengin_account_type: null,
  bank_account_information_zengin_account_number: null,
  bank_account_information_zengin_account_holder_kana: null,
  bank_account_information_transfer_type: null,
  bank_account_information_currency: null,
  bank_account_information_default_frequency: null
)
```

