# # IdentityDocumentFullAllOfDataExtractedFromDocument

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first_name** | **string** | The document holder&#39;s first name as it appears on the identity document |
**birth_name** | **string** | The document holder&#39;s birth name (family name at birth) |
**last_name** | **string** | The document holder&#39;s current last name (may differ from birth name) |
**born_on** | **\DateTime** | The document holder&#39;s date of birth as it appears on the document |
**birth_location** | **string** | The holder&#39;s place of birth as it appears on the document |
**gender** | **string** | The holder&#39;s gender as it appears on the document. \&quot;m\&quot; for Male, \&quot;f\&quot; for Female, \&quot;x\&quot; for Non-binary or unspecified. |
**full_address** | **string** | The holder&#39;s complete postal address as it appears on the document |
**type** | **string** | The type of identity document that was verified |
**issuing_country_code** | **string** | The country that issued the document (ISO 3166-1 alpha-2 code) |
**issued_on** | **\DateTime** | The date when the document was issued |
**expired_on** | **\DateTime** | The date when the document legally expires |
**document_number** | **string** | Document identifier number (may contain letters) |
**mrz** | [**\OpenAPI\Client\Model\GetIdDocumentVerification200ResponseAllOfExtractedFromDocumentMrz**](GetIdDocumentVerification200ResponseAllOfExtractedFromDocumentMrz.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
