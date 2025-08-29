# # CreateUser

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | The email address must not match any existing User&#39;s email. |
**role** | **string** | Role assigned to the User in the Organization. |
**locale** | [**\OpenAPI\Client\Model\Locale**](Locale.md) |  |
**workspaces** | **string[]** | The new User must be associated with at least one Workspace in the Organization. |
**first_name** | **string** | User&#39;s first name | [optional]
**last_name** | **string** | User&#39;s last name | [optional]
**phone_number** | **string** | E.164 format | [optional]
**job_title** | **string** | This property cannot start or end with whitespace, does not allow HTML tags, URL or email. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
