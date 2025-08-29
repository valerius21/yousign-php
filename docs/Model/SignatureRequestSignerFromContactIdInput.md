# # SignatureRequestSignerFromContactIdInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contact_id** | **string** | Create signer from an existing contact |
**fields** | [**\OpenAPI\Client\Model\FieldsInput[]**](FieldsInput.md) |  | [optional]
**signature_level** | **string** |  | [default to 'electronic_signature']
**signature_authentication_mode** | **string** |  | [optional]
**redirect_urls** | [**\OpenAPI\Client\Model\SignatureRequestSignerFromInfoInputRedirectUrls**](SignatureRequestSignerFromInfoInputRedirectUrls.md) |  | [optional]
**custom_text** | [**\OpenAPI\Client\Model\SignatureRequestSignerFromInfoInputCustomText**](SignatureRequestSignerFromInfoInputCustomText.md) |  | [optional]
**pre_identity_verification_required** | **bool** | Defines the way the Signer&#39;s Identity Documents will be uploaded for Verification. If set to &#x60;true&#x60;, &#x60;signature_level&#x60;should be equal to &#x60;advanced_electronic_signature&#x60; and &#x60;delivery_mode&#x60; set to &#x60;none&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
