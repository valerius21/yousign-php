# # InitiateIdentityVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first_name** | **string** | The first name provided must match exactly as it appears on the ID document, as a consistency check will be performed. If multiple given names are listed on the document, you must provide only one of them. |
**last_name** | **string** | The last name provided must match exactly as it appears on the ID document, as a consistency check will be performed. If both a birth name and a usage name are listed on the document, you must provide one of them, but not both. |
**redirection_url** | **string** | The URL to redirect the person back to your application or website after the identity verification flow is complete. |
**face_recognition** | **bool** | Enable face recognition step in the identity verification flow. | [optional] [default to false]
**workspace_id** | **string** | Scopes the verification to a specific workspace. Defaults to the default workspace if not specified. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
