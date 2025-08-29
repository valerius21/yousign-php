# # FieldText

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**document_id** | **string** |  |
**signer_id** | **string** |  |
**type** | **string** |  |
**width** | **int** | If not set, the width is automatically calculated with the max_length value |
**height** | **int** | The height must be calculated using the formula: \&quot;height &#x3D; number_of_lines \\* font_size \\* line_height\&quot;, where the line height is always set to 1.5. |
**page** | **int** |  |
**x** | **int** |  |
**y** | **int** |  |
**question** | **string** |  |
**instruction** | **string** |  |
**optional** | **bool** |  |
**answer** | **string** |  |
**max_length** | **int** |  |
**font** | [**\OpenAPI\Client\Model\Font**](Font.md) |  |
**name** | **string** |  | [optional]
**default_value** | **string** |  | [optional]
**read_only** | **bool** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
