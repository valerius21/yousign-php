# # CreateApprover

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**custom_text** | [**\OpenAPI\Client\Model\CustomText**](CustomText.md) |  | [optional]
**insert_after_id** | **string** | ID of the Approver that this Approver follows in the approval sequence. They will only be asked to approve once that previous Approver has approved. Only applicable when &#x60;ordered_approvers&#x60; is enabled for the Signature Request. | [optional]
**info** | [**\OpenAPI\Client\Model\NewApproverFromScratchInfo**](NewApproverFromScratchInfo.md) |  |
**user_id** | **string** |  |
**contact_id** | **string** |  |
**signer_id** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
