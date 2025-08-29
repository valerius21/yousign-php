# # SignerFieldsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**document_id** | **string** |  |
**signer_id** | **string** |  |
**type** | **string** |  |
**height** | **int** | The height must be calculated using the formula: \&quot;height &#x3D; number_of_lines \\* font_size \\* line_height\&quot;, where the line height is always set to 1.5. |
**width** | **int** |  |
**page** | **int** |  |
**x** | **int** |  |
**y** | **int** |  |
**reason** | **string** |  |
**question** | **string** |  |
**instruction** | **string** |  |
**optional** | **bool** | Does the Signer has to select one of the radio buttons from this group? |
**answer** | **string** |  |
**max_length** | **int** |  |
**font** | [**\OpenAPI\Client\Model\Font**](Font.md) |  |
**name** | **string** |  |
**default_value** | **string** |  | [optional]
**read_only** | **bool** |  | [optional]
**mention** | **string** |  |
**checked** | **bool** | Signer has checked the checkbox |
**size** | **int** | The size determines both the width and height of the checkbox. | [optional]
**radios** | [**\OpenAPI\Client\Model\FieldRadioButtonGroupRadiosInner[]**](FieldRadioButtonGroupRadiosInner.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
