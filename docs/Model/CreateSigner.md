# # CreateSigner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**info** | [**\OpenAPI\Client\Model\NewSignerFromScratchInfo**](NewSignerFromScratchInfo.md) |  |
**fields** | [**\OpenAPI\Client\Model\FieldsInput[]**](FieldsInput.md) |  | [optional]
**insert_after_id** | **string** | Insert just after the position of the specified signer id | [optional]
**signature_level** | **string** |  |
**signature_authentication_mode** | **string** |  | [optional]
**redirect_urls** | [**\OpenAPI\Client\Model\NewSignerFromScratchRedirectUrls**](NewSignerFromScratchRedirectUrls.md) |  | [optional]
**custom_text** | [**\OpenAPI\Client\Model\NewSignerFromScratchCustomText**](NewSignerFromScratchCustomText.md) |  | [optional]
**delivery_mode** | [**\OpenAPI\Client\Model\SignerDeliveryMode**](SignerDeliveryMode.md) |  | [optional]
**identification_attestation_id** | **string** |  | [optional]
**sms_notification** | [**\OpenAPI\Client\Model\SmsNotification1**](SmsNotification1.md) |  | [optional]
**email_notification** | [**\OpenAPI\Client\Model\EmailNotification1**](EmailNotification1.md) |  | [optional]
**pre_identity_verification_required** | **bool** | Defines the way the Signer&#39;s Identity Documents will be uploaded for Verification. If set to &#x60;true&#x60;, &#x60;signature_level&#x60;should be equal to &#x60;advanced_electronic_signature&#x60; and &#x60;delivery_mode&#x60; set to &#x60;none&#x60;. | [optional]
**user_id** | **string** | Create signer from an existing user |
**contact_id** | **string** | Create signer from an existing contact |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
