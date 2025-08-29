# # Mention1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**signer_id** | **string** |  | [optional]
**page** | **int** |  | [optional]
**x** | **int** |  | [optional]
**y** | **int** |  | [optional]
**width** | **int** | If not set, the width is automatically calculated with the read only text length. | [optional]
**height** | **int** | The height must be 24 or a multiple of 15 greater than 24. If height is not provided, it will be calculated depending on the number of newlines in the read only text. | [optional]
**mention** | **string** | Content of the Mention. You can use dynamic tags when creating the Mention: • %date% will display the current date when the Signer sign the Signature Request (eg. \&quot;24-03-2025\&quot;) • %datetime% will display the current date and time when the Signer signs the Signature Request (eg. \&quot;24-03-2025 10:30 UTC+0\&quot;) | [optional]
**font** | [**\OpenAPI\Client\Model\UpdateFieldFont**](UpdateFieldFont.md) |  | [optional]
**name** | **string** | Name of the Field. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
