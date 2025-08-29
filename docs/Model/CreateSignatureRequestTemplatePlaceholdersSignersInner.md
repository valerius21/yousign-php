# # CreateSignatureRequestTemplatePlaceholdersSignersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **string** |  |
**info** | [**\OpenAPI\Client\Model\SignatureRequestPlaceholderSignerSubstituteFromInfoInputInfo**](SignatureRequestPlaceholderSignerSubstituteFromInfoInputInfo.md) |  |
**signature_level** | **string** |  | [optional] [default to 'electronic_signature']
**signature_authentication_mode** | **string** |  | [optional]
**redirect_urls** | [**\OpenAPI\Client\Model\NewSignerFromScratchRedirectUrls**](NewSignerFromScratchRedirectUrls.md) |  | [optional]
**custom_text** | [**\OpenAPI\Client\Model\SignatureRequestSignerFromInfoInputCustomText**](SignatureRequestSignerFromInfoInputCustomText.md) |  | [optional]
**delivery_mode** | [**\OpenAPI\Client\Model\SignerDeliveryMode**](SignerDeliveryMode.md) |  | [optional]
**user_id** | **string** | Create signer from an existing user |
**contact_id** | **string** | Create signer from an existing contact |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
