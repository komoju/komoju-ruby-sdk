# Komoju::LiveApplicationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **locale** | [**Locale**](Locale.md) |  | [optional] |
| **service_agreement_agreed_to_tos** | **Boolean** | Whether the merchant has agreed to KOMOJU&#39;s terms of service. | [optional] |
| **company_information_company_name** | **String** | Registered legal name of the company. | [optional] |
| **company_information_company_phone** | **String** | Company contact phone number. | [optional] |
| **company_information_company_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **company_information_corporation_type** | **String** | Whether the business is a sole proprietorship or corporation. | [optional] |
| **company_information_company_postal_code** | **String** | Postal code of the company&#39;s registered address. | [optional] |
| **company_information_company_prefecture_state** | **String** | Prefecture or state of the company&#39;s registered address. | [optional] |
| **company_information_company_prefecture_state_kana** | **String** | Prefecture or state in katakana. | [optional] |
| **company_information_company_city** | **String** | City of the company&#39;s registered address. | [optional] |
| **company_information_company_city_kana** | **String** | City name in katakana. | [optional] |
| **company_information_company_address** | **String** | Street address of the company. | [optional] |
| **company_information_industry_description** | **String** | Description of the industry the company operates in. | [optional] |
| **company_information_business_description** | **String** | Description of the company&#39;s business activities and products/services sold. | [optional] |
| **company_information_employee_number** | **String** | Number of employees at the company. | [optional] |
| **company_information_establishment_date** | **String** | Date the company was established (YYYY-MM-DD format). | [optional] |
| **company_information_office_name** | **String** | Name of the specific office or branch. | [optional] |
| **company_information_contact_email** | **String** | Primary contact email address for the company. | [optional] |
| **company_information_contact_phone** | **String** | Primary contact phone number for the company. | [optional] |
| **company_information_incorporation_certificates** | **Array&lt;String&gt;** | File IDs of uploaded incorporation certificate documents. | [optional] |
| **company_information_registration_number** | **String** | Company registration number. | [optional] |
| **company_information_share_capital_amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **company_information_share_capital_currency** | [**Currency**](Currency.md) |  | [optional] |
| **company_information_sole_proprietor_proofs** | **Array&lt;String&gt;** | File IDs of uploaded sole proprietorship proof documents. | [optional] |
| **company_information_company_name_kana** | **String** | Company name in katakana. | [optional] |
| **company_information_company_name_alphabet** | **String** | Company name in alphanumeric (Roman) characters. | [optional] |
| **company_information_company_url** | **String** | URL of the company&#39;s website. | [optional] |
| **company_information_company_address_kana** | **String** | Street address in katakana. | [optional] |
| **company_information_company_address_building_name** | **String** | Building name portion of the company address. | [optional] |
| **company_information_company_address_building_name_kana** | **String** | Building name in katakana. | [optional] |
| **representative_director_information_first_name** | **String** | Representative director&#39;s first name. | [optional] |
| **representative_director_information_first_name_kana** | **String** | Representative director&#39;s first name in katakana. | [optional] |
| **representative_director_information_last_name** | **String** | Representative director&#39;s last name. | [optional] |
| **representative_director_information_last_name_kana** | **String** | Representative director&#39;s last name in katakana. | [optional] |
| **representative_director_information_date_of_birth** | **String** | Representative director&#39;s date of birth (YYYY-MM-DD format). | [optional] |
| **representative_director_information_gender** | **String** | Representative director&#39;s gender. | [optional] |
| **representative_director_information_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **representative_director_information_postal_code** | **String** | Postal code of the representative director&#39;s address. | [optional] |
| **representative_director_information_prefecture_state** | **String** | Prefecture or state of the representative director&#39;s address. | [optional] |
| **representative_director_information_prefecture_state_kana** | **String** | Prefecture or state in katakana. | [optional] |
| **representative_director_information_city** | **String** | City of the representative director&#39;s address. | [optional] |
| **representative_director_information_city_kana** | **String** | City name in katakana. | [optional] |
| **representative_director_information_address** | **String** | Street address of the representative director. | [optional] |
| **representative_director_information_address_kana** | **String** | Street address in katakana. | [optional] |
| **representative_director_information_address_building_name** | **String** | Building name portion of the representative director&#39;s address. | [optional] |
| **representative_director_information_address_building_name_kana** | **String** | Building name in katakana. | [optional] |
| **representative_director_information_phone** | **String** | Representative director&#39;s phone number. | [optional] |
| **applicant_information_first_name** | **String** | Applicant&#39;s first name. | [optional] |
| **applicant_information_first_name_kana** | **String** | Applicant&#39;s first name in katakana. | [optional] |
| **applicant_information_last_name** | **String** | Applicant&#39;s last name. | [optional] |
| **applicant_information_last_name_kana** | **String** | Applicant&#39;s last name in katakana. | [optional] |
| **applicant_information_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **applicant_information_gender** | **String** | Applicant&#39;s gender. | [optional] |
| **applicant_information_date_of_birth** | **String** | Applicant&#39;s date of birth (YYYY-MM-DD format). | [optional] |
| **applicant_information_identity_document_type** | **String** | Type of identity document submitted for verification. | [optional] |
| **applicant_information_identity_front** | **String** | File ID of the front side of the uploaded identity document. | [optional] |
| **applicant_information_identity_back** | **String** | File ID of the back side of the uploaded identity document. | [optional] |
| **site_information_site_name** | **String** | Name of the merchant&#39;s website or online store. | [optional] |
| **site_information_site_name_kana** | **String** | Site name in katakana. | [optional] |
| **site_information_site_name_alphabet** | **String** | Site name in alphanumeric (Roman) characters. | [optional] |
| **site_information_site_url** | **String** | URL of the merchant&#39;s online store. | [optional] |
| **site_information_establishment_date** | **String** | Date the online store was established (YYYY-MM-DD format). | [optional] |
| **site_information_store_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **site_information_store_postal_code** | **String** | Postal code of the store&#39;s physical location. | [optional] |
| **site_information_store_prefecture_state** | **String** | Prefecture or state of the store&#39;s physical location. | [optional] |
| **site_information_store_prefecture_state_kana** | **String** | Prefecture or state in katakana. | [optional] |
| **site_information_store_city** | **String** | City of the store&#39;s physical location. | [optional] |
| **site_information_store_city_kana** | **String** | City name in katakana. | [optional] |
| **site_information_store_address** | **String** | Street address of the store&#39;s physical location. | [optional] |
| **site_information_store_address_kana** | **String** | Store street address in katakana. | [optional] |
| **site_information_store_building_name** | **String** | Building name for the store&#39;s address. | [optional] |
| **site_information_store_building_name_kana** | **String** | Building name in katakana. | [optional] |
| **site_information_site_product_description** | **String** | Description of the products or services sold on the site. | [optional] |
| **site_information_site_annual_sales** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **site_information_site_annual_sales_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_site_average_transactional_value** | **String** | Average transaction value as a formatted string. | [optional] |
| **site_information_site_average_transactional_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_site_minimum_product_pricing_cents** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **site_information_site_minimum_product_pricing_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_site_maximum_product_pricing_cents** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **site_information_site_maximum_product_pricing_currency** | [**Currency**](Currency.md) |  | [optional] |
| **site_information_sctl_url** | **String** | URL of the merchant&#39;s Specified Commercial Transaction Law disclosure page. | [optional] |
| **site_information_sales_permit_required** | **Boolean** | Whether a sales permit is required for the merchant&#39;s business type. | [optional] |
| **site_information_aup_accepted** | **Boolean** | Whether the merchant has accepted the Acceptable Use Policy. | [optional] |
| **site_information_industry_type** | [**IndustryType**](IndustryType.md) |  | [optional] |
| **site_information_sales_permits** | **Array&lt;String&gt;** | File IDs of uploaded sales permit documents. | [optional] |
| **bank_account_information_zengin_bank_name** | **String** | Name of the merchant&#39;s bank (Zengin network). | [optional] |
| **bank_account_information_zengin_bank_code** | **String** | 4-digit bank code in the Zengin network. | [optional] |
| **bank_account_information_zengin_branch_name** | **String** | Name of the bank branch. | [optional] |
| **bank_account_information_zengin_branch_code** | **String** | 3-digit branch code. | [optional] |
| **bank_account_information_zengin_account_type** | **String** | Type of bank account (ordinary or checking). | [optional] |
| **bank_account_information_zengin_account_number** | **String** | Bank account number. | [optional] |
| **bank_account_information_zengin_account_holder_kana** | **String** | Account holder name in katakana as registered with the bank. | [optional] |
| **bank_account_information_transfer_type** | **String** | Type of bank transfer supported (currently only \&quot;domestic\&quot;). | [optional] |
| **bank_account_information_currency** | [**Currency**](Currency.md) |  | [optional] |
| **bank_account_information_default_frequency** | [**SettlementFrequency**](SettlementFrequency.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

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

