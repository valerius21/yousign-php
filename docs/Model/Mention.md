# # Mention

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**signer_id** | **string** |  |
**type** | **string** |  |
**page** | **int** |  |
**x** | **int** |  |
**y** | **int** |  |
**width** | **int** | If not set, the width is automatically calculated with the mention length. | [optional]
**height** | **int** | The height must be calculated using the formula: \&quot;height &#x3D; number_of_lines \\* font_size \\* line_height\&quot;, where the line height is always set to 1.5. | [optional]
**mention** | **string** | Content of the Mention. You can use dynamic tags when creating the Mention: • &#x60;%date%&#x60; will display the current date when the Signer sign the Signature Request (eg. \&quot;24-03-2025\&quot;) • &#x60;%datetime%&#x60; will display the current date and time when the Signer signs the Signature Request (eg. \&quot;24-03-2025 10:30 UTC+0\&quot;) |
**font** | [**\OpenAPI\Client\Model\CreateFieldFont**](CreateFieldFont.md) |  | [optional]
**name** | **string** | Name of the Field. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
