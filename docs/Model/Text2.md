# # Text2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_id** | **string** |  |
**type** | **string** |  |
**page** | **int** |  |
**x** | **int** |  |
**y** | **int** |  |
**width** | **int** | If not set, the width is automatically calculated with the max_length value | [optional]
**height** | **int** | The height must be 24 or a multiple of 15 greater than 24. | [optional]
**max_length** | **int** |  |
**question** | **string** |  |
**instruction** | **string** |  | [optional]
**optional** | **bool** |  |
**name** | **string** | Name of the Field. | [optional]
**default_value** | **string** | If a default value is provided, the Field will be pre-filled with this value. The Signer can modify it before signing unless the Field is set to &#x60;read-only&#x60;. | [optional]
**read_only** | **bool** | If set to &#x60;true&#x60;, the Signer cannot modify the Field and the default value (if provided) will remain unchanged. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
