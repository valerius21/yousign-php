# # BankAccountMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier for a resource. |
**workspace_id** | **string** | The Workspace ID in which the verification has been created. | [optional]
**created_at** | **\DateTime** | Creation date of the Bank Account Verification. |
**updated_at** | **\DateTime** | Update date of the Bank Account Verification. |
**status** | [**\OpenAPI\Client\Model\BankAccountStatus**](BankAccountStatus.md) |  |
**status_codes** | **string[]** | List of status codes. Indicates the cause when the status is &#x60;failed&#x60; or &#x60;inconclusive&#x60;. |
**data_anonymized** | **bool** | Indicates if the personal data extracted from the document has been anonymized. If set to &#x60;true&#x60;, the personal data has been anonymized and most fields will be NULL. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
