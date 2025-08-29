# # UpdateSignatureRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional]
**delivery_mode** | **string** | Delivery mode to notify signers. | [optional]
**ordered_signers** | **bool** | Enable an ordered workflow, each signer will be requested to sign in a sequential order | [optional]
**ordered_approvers** | **bool** | When enabled, Approvers are requested to approve sequentially. Each Approver will be invited to approve only once the previous one has completed their approval. | [optional]
**reminder_settings** | [**\OpenAPI\Client\Model\UpdateSignatureRequestReminderSettings**](UpdateSignatureRequestReminderSettings.md) |  | [optional]
**timezone** | **string** | Time zone of the dates and times displayed in emails, the Signature Request expiration date, and the PDF Audit Trail. Format: tz database. Default is set to Europe/Paris. | [optional] [default to 'Europe/Paris']
**email_custom_note** | **string** |  | [optional]
**expiration_date** | **\DateTime** | Due date of the Signature Request (yyyy-mm-dd). The date cannot be in the past and cannot be more than one year after initiation. | [optional]
**external_id** | **string** |  | [optional]
**branding_id** | **string** |  | [optional]
**custom_experience_id** | **string** | Use a specific Custom Experience to customize the signature experience. | [optional]
**signers_allowed_to_decline** | **bool** | Allowing signers to decline to sign. | [optional] [default to false]
**workspace_id** | **string** | Transfer the Signature Request into a given Workspace. | [optional]
**audit_trail_locale** | [**\OpenAPI\Client\Model\AuditTrailLocale**](AuditTrailLocale.md) | Define the locale for the generated audit trail. | [optional]
**email_notification** | [**\OpenAPI\Client\Model\SignatureRequestEmailNotification**](SignatureRequestEmailNotification.md) |  | [optional]
**labels** | **string[]** | List of Labels to associate with the Signature Request. Labels are identified by their ID. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
