# # CreateField

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**signer_id** | **string** |  |
**type** | **string** |  |
**page** | **int** |  |
**x** | **int** |  |
**y** | **int** |  |
**height** | **int** | The height must be calculated using the formula: \&quot;height &#x3D; number_of_lines \\* font_size \\* line_height\&quot;, where the line height is always set to 1.5. | [optional]
**width** | **int** | If not set, the width is automatically calculated with the read only text length. | [optional]
**reason** | **string** | Provide extra context to explain why the Document is being signed. Once the Document is signed, the custom reason is stored in the Audit Trail and is included in the signature certificate. The default value is: \&quot;Signed by [Signer first name] [Signer last name]\&quot;. | [optional]
**mention** | **string** | Content of the Mention. You can use dynamic tags when creating the Mention: • &#x60;%date%&#x60; will display the current date when the Signer sign the Signature Request (eg. \&quot;24-03-2025\&quot;) • &#x60;%datetime%&#x60; will display the current date and time when the Signer signs the Signature Request (eg. \&quot;24-03-2025 10:30 UTC+0\&quot;) |
**font** | [**\OpenAPI\Client\Model\CreateFieldFont**](CreateFieldFont.md) |  | [optional]
**name** | **string** | Radio group&#39;s name | [optional]
**max_length** | **int** |  |
**question** | **string** | If you don&#39;t want any question, you can give an empty string. |
**instruction** | **string** |  | [optional]
**optional** | **bool** |  | [optional] [default to false]
**default_value** | **string** | If a default value is provided, the Field will be pre-filled with this value. The Signer can modify it before signing unless the Field is set to &#x60;read-only&#x60;. | [optional]
**read_only** | **bool** | If set to &#x60;true&#x60;, the radio button cannot be modified by the Signer. | [optional] [default to false]
**size** | **int** |  | [optional] [default to 24]
**checked** | **bool** |  | [optional] [default to false]
**radios** | [**\OpenAPI\Client\Model\RadioGroupRadiosInner[]**](RadioGroupRadiosInner.md) |  |
**text** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
