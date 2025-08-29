# # UpdateField

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**signer_id** | **string** |  | [optional]
**page** | **int** |  | [optional]
**x** | **int** |  | [optional]
**y** | **int** |  | [optional]
**height** | **int** | The height must be 24 or a multiple of 15 greater than 24. If height is not provided, it will be calculated depending on the number of newlines in the mention. | [optional]
**width** | **int** | If not set, the width is automatically calculated with the mention length. | [optional]
**reason** | **string** | Provide extra context to explain why the Document is being signed. Once the Document is signed, the custom reason is stored in the Audit Trail and is included in the signature certificate. The default value is: \&quot;Signed by [Signer first name] [Signer last name]\&quot;. | [optional]
**mention** | **string** | Content of the Mention. You can use dynamic tags when creating the Mention: • %date% will display the current date when the Signer sign the Signature Request (eg. \&quot;24-03-2025\&quot;) • %datetime% will display the current date and time when the Signer signs the Signature Request (eg. \&quot;24-03-2025 10:30 UTC+0\&quot;) | [optional]
**font** | [**\OpenAPI\Client\Model\UpdateFieldFont**](UpdateFieldFont.md) |  | [optional]
**name** | **string** | Radio group&#39;s name | [optional]
**max_length** | **int** |  | [optional]
**question** | **string** | If you don&#39;t want any question, you can give an empty string. | [optional]
**instruction** | **string** |  | [optional]
**optional** | **bool** |  | [optional] [default to false]
**default_value** | **string** | If a default value is provided, the Field will be pre-filled with this value. The Signer can modify it before signing unless the Field is set to &#x60;read-only&#x60;. | [optional]
**read_only** | **bool** | If set to &#x60;true&#x60;, the radio button cannot be modified by the Signer. | [optional] [default to false]
**size** | **int** |  | [optional] [default to 24]
**checked** | **bool** |  | [optional] [default to false]
**radios** | [**\OpenAPI\Client\Model\RadioGroup1RadiosInner[]**](RadioGroup1RadiosInner.md) |  | [optional]
**text** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
