# # SignatureRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**status** | [**\OpenAPI\Client\Model\SignatureRequestStatus**](SignatureRequestStatus.md) |  |
**name** | **string** |  |
**delivery_mode** | **string** |  |
**created_at** | **\DateTime** |  |
**ordered_signers** | **bool** | Enable an ordered workflow, each Signer will be requested to sign in a sequential order |
**ordered_approvers** | **bool** | Enable an ordered workflow, each Approver will be requested to approve in a sequential order |
**reminder_settings** | [**\OpenAPI\Client\Model\SignatureRequestInListReminderSettings**](SignatureRequestInListReminderSettings.md) |  |
**timezone** | **string** | Time zone of the dates and times displayed in emails, the Signature Request expiration date, and the PDF Audit Trail. Format: tz database. Default is set to Europe/Paris. | [default to 'Europe/Paris']
**email_custom_note** | **string** |  |
**expiration_date** | **\DateTime** |  |
**source** | **string** |  |
**signers** | [**\OpenAPI\Client\Model\SignatureRequestInListSignersInner[]**](SignatureRequestInListSignersInner.md) |  |
**approvers** | [**\OpenAPI\Client\Model\SignatureRequestInListApproversInner[]**](SignatureRequestInListApproversInner.md) |  | [optional]
**labels** | [**\OpenAPI\Client\Model\SignatureRequestLabel[]**](SignatureRequestLabel.md) | Labels associated to the Signature Request | [optional]
**documents** | [**\OpenAPI\Client\Model\SignatureRequestInListDocumentsInner[]**](SignatureRequestInListDocumentsInner.md) |  |
**sender** | [**\OpenAPI\Client\Model\SignatureRequestInListSender**](SignatureRequestInListSender.md) |  |
**external_id** | **string** |  |
**branding_id** | **string** |  |
**custom_experience_id** | **string** |  |
**signers_allowed_to_decline** | **bool** |  |
**workspace_id** | **string** |  | [optional]
**audit_trail_locale** | [**\OpenAPI\Client\Model\AuditTrailLocale**](AuditTrailLocale.md) |  |
**email_notification** | [**\OpenAPI\Client\Model\SignatureRequestEmailNotification**](SignatureRequestEmailNotification.md) |  |
**bulk_send_batch_id** | **string** |  |
**decline_information** | [**\OpenAPI\Client\Model\SignatureRequestDeclineInformation**](SignatureRequestDeclineInformation.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
