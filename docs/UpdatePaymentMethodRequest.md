# Komoju::UpdatePaymentMethodRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **locale** | [**Locale**](Locale.md) |  | [optional] |
| **shared_payment_method_data_open_time** | **String** | Business opening time for this merchant&#39;s store. | [optional] |
| **shared_payment_method_data_close_time** | **String** | Business closing time for this merchant&#39;s store. | [optional] |
| **shared_payment_method_data_privacy_policy_url** | **String** | URL to the merchant&#39;s privacy policy page. | [optional] |
| **shared_payment_method_data_terms_of_service_url** | **String** | URL to the merchant&#39;s terms of service page. | [optional] |
| **shared_payment_method_data_pci_compliance_proofs** | **Array&lt;String&gt;** | File IDs of uploaded PCI compliance proof documents. | [optional] |
| **shared_payment_method_data_shareholder_registers** | **Array&lt;String&gt;** | File IDs of uploaded shareholder register documents. | [optional] |
| **shared_payment_method_data_has_processed_cc_before** | **Boolean** | Whether the merchant has previously processed credit card payments. | [optional] |
| **shared_payment_method_data_processes_card_info** | **Boolean** | Whether the merchant directly handles or stores card information. | [optional] |
| **shared_payment_method_data_conducts_door_to_door_sales** | **Boolean** | Whether the merchant conducts door-to-door sales. | [optional] |
| **shared_payment_method_data_conducts_telemarketing** | **Boolean** | Whether the merchant conducts telemarketing activities. | [optional] |
| **shared_payment_method_data_conducts_mlm_scheme** | **Boolean** | Whether the merchant operates a multi-level marketing scheme. | [optional] |
| **shared_payment_method_data_conducts_business_opportunity_scheme** | **Boolean** | Whether the merchant offers business opportunity schemes. | [optional] |
| **shared_payment_method_data_provides_specified_continuous_services** | **Boolean** | Whether the merchant provides services subject to the Specified Commercial Transaction Act. | [optional] |
| **shared_payment_method_data_violated_consumer_contract_act** | **Boolean** | Whether the merchant has violated the Consumer Contract Act. | [optional] |
| **shared_payment_method_data_violated_commercial_transaction_act** | **Boolean** | Whether the merchant has violated the Commercial Transaction Act. | [optional] |
| **linepay_accepted_line_tos** | **Boolean** | Whether the merchant has accepted LINE Pay&#39;s terms of service. | [optional] |
| **linepay_fields** | **String** | Serialized form fields for the LINE Pay application. | [optional] |
| **paypay_accepted_paypay_tos** | **Boolean** | Whether the merchant has accepted PayPay&#39;s terms of service. | [optional] |
| **paypay_fields** | **String** | Serialized form fields for the PayPay application. | [optional] |
| **merpay_accepted_merpay_tos** | **Boolean** | Whether the merchant has accepted Merpay&#39;s terms of service. | [optional] |
| **merpay_fields** | **String** | Serialized form fields for the Merpay application. | [optional] |
| **convenience_store_expected_number_of_payments** | **Integer** | Estimated monthly number of convenience store payments. | [optional] |
| **convenience_store_fields** | **String** | Serialized form fields for the convenience store application. | [optional] |
| **seven_eleven_site_is_public** | **Boolean** | Whether the merchant&#39;s website is publicly accessible. | [optional] |
| **seven_eleven_no_direct_delivery_from_producer** | **Boolean** | Confirmation that products are not delivered directly from producers. | [optional] |
| **seven_eleven_no_ticket_sales** | **Boolean** | Confirmation that the merchant does not sell tickets. | [optional] |
| **seven_eleven_correct_flow_for_order_items** | **Boolean** | Confirmation that the order flow matches Seven-Eleven&#39;s requirements. | [optional] |
| **seven_eleven_delivery_within_two_months** | **Boolean** | Confirmation that all ordered items will be delivered within two months. | [optional] |
| **seven_eleven_all_items_are_cheaper_than_konbini_limit** | **Boolean** | Confirmation that all items are priced below the konbini payment limit. | [optional] |
| **seven_eleven_display_sales_permit_number** | **Boolean** | Confirmation that any required sales permit numbers are displayed. | [optional] |
| **seven_eleven_order_fee_is_displayed** | **Boolean** | Confirmation that the order fee is clearly displayed to customers. | [optional] |
| **seven_eleven_no_international_transaction** | **Boolean** | Confirmation that transactions are domestic only. | [optional] |
| **seven_eleven_provided_info_matches_sctl** | **Boolean** | Confirmation that site info matches the Specified Commercial Transaction Law disclosure page. | [optional] |
| **seven_eleven_sctl_page_has_phone_number** | **Boolean** | Confirmation that the SCTL page includes a phone number. | [optional] |
| **seven_eleven_product_pages_are_public** | **Boolean** | Confirmation that product detail pages are publicly viewable. | [optional] |
| **seven_eleven_have_sold_as_regular_price** | **Boolean** | Confirmation that items have been sold at regular (non-discounted) price before. | [optional] |
| **seven_eleven_note** | **String** | Free-text notes for the Seven-Eleven application. | [optional] |
| **seven_eleven_fields** | **String** | Serialized form fields for the Seven-Eleven application. | [optional] |
| **visa_mastercard_credit_card_access_restrictions** | **Boolean** | Confirmation that the site has appropriate access restrictions in place. | [optional] |
| **visa_mastercard_credit_card_mfa_implementation** | **Boolean** | Confirmation that multi-factor authentication is implemented. | [optional] |
| **visa_mastercard_credit_card_account_lock** | **Boolean** | Confirmation that account lockout policies are in place. | [optional] |
| **visa_mastercard_credit_card_public_directories** | **Boolean** | Confirmation that public directory listing is disabled. | [optional] |
| **visa_mastercard_credit_card_file_extension_restrictions** | **Boolean** | Confirmation that file extension restrictions are enforced. | [optional] |
| **visa_mastercard_credit_card_vulnerability_assessments** | **Boolean** | Confirmation that regular vulnerability assessments are conducted. | [optional] |
| **visa_mastercard_credit_card_sql_injection_and_xss** | **Boolean** | Confirmation that the site is protected against SQL injection and XSS attacks. | [optional] |
| **visa_mastercard_credit_card_source_code_review** | **Boolean** | Confirmation that source code security review is performed. | [optional] |
| **visa_mastercard_credit_card_anti_virus_software** | **Boolean** | Confirmation that anti-virus software is installed and maintained. | [optional] |
| **visa_mastercard_credit_card_fields** | **String** | Serialized form fields for the Visa/Mastercard credit card application. | [optional] |
| **jcb_amex_diners_credit_card_access_restrictions** | **Boolean** | Confirmation that the site has appropriate access restrictions in place (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_mfa_implementation** | **Boolean** | Confirmation that multi-factor authentication is implemented (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_account_lock** | **Boolean** | Confirmation that account lockout policies are in place (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_public_directories** | **Boolean** | Confirmation that public directory listing is disabled (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_file_extension_restrictions** | **Boolean** | Confirmation that file extension restrictions are enforced (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_vulnerability_assessments** | **Boolean** | Confirmation that regular vulnerability assessments are conducted (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_sql_injection_and_xss** | **Boolean** | Confirmation that the site is protected against SQL injection and XSS attacks (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_source_code_review** | **Boolean** | Confirmation that source code security review is performed (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_anti_virus_software** | **Boolean** | Confirmation that anti-virus software is installed and maintained (JCB/Amex/Diners). | [optional] |
| **jcb_amex_diners_credit_card_fields** | **String** | Serialized form fields for the JCB/Amex/Diners credit card application. | [optional] |

## Example

```ruby
require 'komoju-sdk'

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

