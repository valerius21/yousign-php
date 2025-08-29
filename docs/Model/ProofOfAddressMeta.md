# # ProofOfAddressMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier for a resource. |
**workspace_id** | **string** | The Workspace ID in which the Proof of Address Verification has been created. |
**created_at** | **\DateTime** | Creation date of the Proof of Address Verification. |
**updated_at** | **\DateTime** | Update date of the Proof of Address Verification. |
**status** | **string** | Status of the verification |
**status_codes** | **string[]** | List of status codes. Indicates the cause when the status is &#x60;failed&#x60; or &#x60;inconclusive&#x60;. |
**data_anonymized** | **bool** | Indicates if the data related to the ProofOfAddress Verification has been anonymized. If set to &#x60;true&#x60;, the data are removed and most fields will be NULL. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
