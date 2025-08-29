# # SignatureRequestActivated

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**status** | **string** |  |
**name** | **string** |  |
**delivery_mode** | **string** |  |
**created_at** | **\DateTime** |  |
**ordered_signers** | **bool** | Enable an ordered workflow, each Signer will be requested to sign in a sequential order |
**ordered_approvers** | **bool** | Enable an ordered workflow, each Approver will be requested to approve in a sequential order |
**reminder_settings** | [**\OpenAPI\Client\Model\SignatureRequestInListReminderSettings**](SignatureRequestInListReminderSettings.md) |  |
**timezone** | **string** | Time zone of the dates and times displayed in emails, the Signature Request expiration date, and the PDF Audit Trail. Format: tz database. Default is set to Europe/Paris. | [default to 'Europe/Paris']
**email_custom_note** | **string** |  |
**expiration_date** | **\DateTime** |  |
**signers** | [**\OpenAPI\Client\Model\EmbeddedSignerWithSignatureLink[]**](EmbeddedSignerWithSignatureLink.md) |  |
**approvers** | [**\OpenAPI\Client\Model\ApproverToNotify[]**](ApproverToNotify.md) |  | [optional]
**labels** | [**\OpenAPI\Client\Model\SignatureRequestLabel[]**](SignatureRequestLabel.md) | Labels associated to the Signature Request | [optional]
**documents** | [**\OpenAPI\Client\Model\SignatureRequestActivatedDocumentsInner[]**](SignatureRequestActivatedDocumentsInner.md) |  |
**external_id** | **string** |  |
**branding_id** | **string** |  |
**custom_experience_id** | **string** |  |
**audit_trail_locale** | [**\OpenAPI\Client\Model\AuditTrailLocale**](AuditTrailLocale.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
