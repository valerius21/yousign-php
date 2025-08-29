# # CreateElectronicSealPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **string** | Specify which Electronic Seal Document to use for creating an Electronic Seal. |
**image_id** | **string** | Specify which Electronic Seal Image to use for creating an Electronic Seal. | [optional]
**external_id** | **string** | Store a custom id that will be added to webhooks | [optional]
**fields** | [**\OpenAPI\Client\Model\CreateElectronicSealPayloadFieldsInner[]**](CreateElectronicSealPayloadFieldsInner.md) | Fields you want to add to your Document. At least one Seal Field is mandatory. |
**signature_level** | **string** | Level of Electronic Seal for your Document | [optional]
**certificate_id** | **string** | Specify which certificate to use for creating an Electronic Seal (only available for advanced_electronic_signature level). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
