# Komoju::UpdatePaymentMethodRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **locale** | [**Locale**](Locale.md) |  | [optional] |
| **shared_payment_method_data_open_time** | **String** |  | [optional] |
| **shared_payment_method_data_close_time** | **String** |  | [optional] |
| **shared_payment_method_data_privacy_policy_url** | **String** |  | [optional] |
| **shared_payment_method_data_terms_of_service_url** | **String** |  | [optional] |
| **shared_payment_method_data_pci_compliance_proofs** | **Array&lt;String&gt;** |  | [optional] |
| **shared_payment_method_data_shareholder_registers** | **Array&lt;String&gt;** |  | [optional] |
| **shared_payment_method_data_has_processed_cc_before** | **Boolean** |  | [optional] |
| **shared_payment_method_data_processes_card_info** | **Boolean** |  | [optional] |
| **shared_payment_method_data_conducts_door_to_door_sales** | **Boolean** |  | [optional] |
| **shared_payment_method_data_conducts_telemarketing** | **Boolean** |  | [optional] |
| **shared_payment_method_data_conducts_mlm_scheme** | **Boolean** |  | [optional] |
| **shared_payment_method_data_conducts_business_opportunity_scheme** | **Boolean** |  | [optional] |
| **shared_payment_method_data_provides_specified_continuous_services** | **Boolean** |  | [optional] |
| **shared_payment_method_data_violated_consumer_contract_act** | **Boolean** |  | [optional] |
| **shared_payment_method_data_violated_commercial_transaction_act** | **Boolean** |  | [optional] |
| **linepay_accepted_line_tos** | **Boolean** |  | [optional] |
| **linepay_fields** | **String** |  | [optional] |
| **paypay_accepted_paypay_tos** | **Boolean** |  | [optional] |
| **paypay_fields** | **String** |  | [optional] |
| **merpay_accepted_merpay_tos** | **Boolean** |  | [optional] |
| **merpay_fields** | **String** |  | [optional] |
| **convenience_store_expected_number_of_payments** | **Integer** |  | [optional] |
| **convenience_store_fields** | **String** |  | [optional] |
| **seven_eleven_site_is_public** | **Boolean** |  | [optional] |
| **seven_eleven_no_direct_delivery_from_producer** | **Boolean** |  | [optional] |
| **seven_eleven_no_ticket_sales** | **Boolean** |  | [optional] |
| **seven_eleven_correct_flow_for_order_items** | **Boolean** |  | [optional] |
| **seven_eleven_delivery_within_two_months** | **Boolean** |  | [optional] |
| **seven_eleven_all_items_are_cheaper_than_konbini_limit** | **Boolean** |  | [optional] |
| **seven_eleven_display_sales_permit_number** | **Boolean** |  | [optional] |
| **seven_eleven_order_fee_is_displayed** | **Boolean** |  | [optional] |
| **seven_eleven_no_international_transaction** | **Boolean** |  | [optional] |
| **seven_eleven_provided_info_matches_sctl** | **Boolean** |  | [optional] |
| **seven_eleven_sctl_page_has_phone_number** | **Boolean** |  | [optional] |
| **seven_eleven_product_pages_are_public** | **Boolean** |  | [optional] |
| **seven_eleven_have_sold_as_regular_price** | **Boolean** |  | [optional] |
| **seven_eleven_note** | **String** |  | [optional] |
| **seven_eleven_fields** | **String** |  | [optional] |
| **visa_mastercard_credit_card_access_restrictions** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_mfa_implementation** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_account_lock** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_public_directories** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_file_extension_restrictions** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_vulnerability_assessments** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_sql_injection_and_xss** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_source_code_review** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_anti_virus_software** | **Boolean** |  | [optional] |
| **visa_mastercard_credit_card_fields** | **String** |  | [optional] |
| **jcb_amex_diners_credit_card_access_restrictions** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_mfa_implementation** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_account_lock** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_public_directories** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_file_extension_restrictions** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_vulnerability_assessments** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_sql_injection_and_xss** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_source_code_review** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_anti_virus_software** | **Boolean** |  | [optional] |
| **jcb_amex_diners_credit_card_fields** | **String** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::UpdatePaymentMethodRequest.new(
  locale: null,
  shared_payment_method_data_open_time: null,
  shared_payment_method_data_close_time: null,
  shared_payment_method_data_privacy_policy_url: null,
  shared_payment_method_data_terms_of_service_url: null,
  shared_payment_method_data_pci_compliance_proofs: null,
  shared_payment_method_data_shareholder_registers: null,
  shared_payment_method_data_has_processed_cc_before: null,
  shared_payment_method_data_processes_card_info: null,
  shared_payment_method_data_conducts_door_to_door_sales: null,
  shared_payment_method_data_conducts_telemarketing: null,
  shared_payment_method_data_conducts_mlm_scheme: null,
  shared_payment_method_data_conducts_business_opportunity_scheme: null,
  shared_payment_method_data_provides_specified_continuous_services: null,
  shared_payment_method_data_violated_consumer_contract_act: null,
  shared_payment_method_data_violated_commercial_transaction_act: null,
  linepay_accepted_line_tos: null,
  linepay_fields: null,
  paypay_accepted_paypay_tos: null,
  paypay_fields: null,
  merpay_accepted_merpay_tos: null,
  merpay_fields: null,
  convenience_store_expected_number_of_payments: null,
  convenience_store_fields: null,
  seven_eleven_site_is_public: null,
  seven_eleven_no_direct_delivery_from_producer: null,
  seven_eleven_no_ticket_sales: null,
  seven_eleven_correct_flow_for_order_items: null,
  seven_eleven_delivery_within_two_months: null,
  seven_eleven_all_items_are_cheaper_than_konbini_limit: null,
  seven_eleven_display_sales_permit_number: null,
  seven_eleven_order_fee_is_displayed: null,
  seven_eleven_no_international_transaction: null,
  seven_eleven_provided_info_matches_sctl: null,
  seven_eleven_sctl_page_has_phone_number: null,
  seven_eleven_product_pages_are_public: null,
  seven_eleven_have_sold_as_regular_price: null,
  seven_eleven_note: null,
  seven_eleven_fields: null,
  visa_mastercard_credit_card_access_restrictions: null,
  visa_mastercard_credit_card_mfa_implementation: null,
  visa_mastercard_credit_card_account_lock: null,
  visa_mastercard_credit_card_public_directories: null,
  visa_mastercard_credit_card_file_extension_restrictions: null,
  visa_mastercard_credit_card_vulnerability_assessments: null,
  visa_mastercard_credit_card_sql_injection_and_xss: null,
  visa_mastercard_credit_card_source_code_review: null,
  visa_mastercard_credit_card_anti_virus_software: null,
  visa_mastercard_credit_card_fields: null,
  jcb_amex_diners_credit_card_access_restrictions: null,
  jcb_amex_diners_credit_card_mfa_implementation: null,
  jcb_amex_diners_credit_card_account_lock: null,
  jcb_amex_diners_credit_card_public_directories: null,
  jcb_amex_diners_credit_card_file_extension_restrictions: null,
  jcb_amex_diners_credit_card_vulnerability_assessments: null,
  jcb_amex_diners_credit_card_sql_injection_and_xss: null,
  jcb_amex_diners_credit_card_source_code_review: null,
  jcb_amex_diners_credit_card_anti_virus_software: null,
  jcb_amex_diners_credit_card_fields: null
)
```

