# # FieldsInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **string** |  |
**type** | **string** |  |
**page** | **int** |  |
**x** | **int** |  |
**y** | **int** |  |
**height** | **int** | The height must be 24 or a multiple of 15 greater than 24. | [optional]
**width** | **int** | If not set, the width is automatically calculated with the max_length value | [optional]
**reason** | **string** | Provide extra context to explain why the Document is being signed. Once the Document is signed, the custom reason is stored in the Audit Trail and is included in the signature certificate. The default value is: \&quot;Signed by [Signer first name] [Signer last name]\&quot;. | [optional]
**mention** | **string** |  |
**name** | **string** | Radio group&#39;s name | [optional]
**max_length** | **int** |  |
**question** | **string** |  |
**instruction** | **string** |  | [optional]
**optional** | **bool** |  |
**default_value** | **string** | If a default value is provided, the Field will be pre-filled with this value. The Signer can modify it before signing unless the Field is set to &#x60;read-only&#x60;. | [optional]
**read_only** | **bool** | If set to &#x60;true&#x60;, the radio button cannot be modified by the Signer. | [optional] [default to false]
**size** | **int** | The omission of size parameter is considered as deprecated. The size determines both the width and height of the checkbox. | [optional]
**checked** | **bool** |  |
**default_checked** | **bool** |  | [optional]
**radios** | [**\OpenAPI\Client\Model\RadioGroup2RadiosInner[]**](RadioGroup2RadiosInner.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
