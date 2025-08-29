# # GetIdDocumentVerification200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier for a resource. |
**status** | [**\OpenAPI\Client\Model\LegacyIdDocumentVerificationStatus**](LegacyIdDocumentVerificationStatus.md) |  |
**status_codes** | **int[]** | List of response codes. |
**extracted_from_document** | [**\OpenAPI\Client\Model\GetIdDocumentVerification200ResponseAllOfExtractedFromDocument**](GetIdDocumentVerification200ResponseAllOfExtractedFromDocument.md) |  |
**personal_data_anonymized** | **bool** | Indicates if the personal data extracted from the document has been anonymized. If set to &#x60;true&#x60;, the personal data has been anonymized and the &#x60;extracted_from_document&#x60; fields will be NULL. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
