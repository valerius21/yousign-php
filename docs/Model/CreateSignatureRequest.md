# # CreateSignatureRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the signature request |
**delivery_mode** | **string** | Delivery mode to notify signers. |
**ordered_signers** | **bool** | Enable an ordered workflow, each signer will be requested to sign in a sequential order | [optional]
**ordered_approvers** | **bool** | When enabled, Approvers are requested to approve sequentially. Each Approver will be invited to approve only once the previous one has completed their approval. | [optional]
**reminder_settings** | [**\OpenAPI\Client\Model\CreateSignatureRequestReminderSettings**](CreateSignatureRequestReminderSettings.md) |  | [optional]
**timezone** | **string** | Time zone of the dates and times displayed in emails, the Signature Request expiration date, and the PDF Audit Trail. Format: tz database. Default is set to Europe/Paris. | [optional] [default to 'Europe/Paris']
**email_custom_note** | **string** | A custom note added to emails sent to signers. | [optional]
**expiration_date** | **\DateTime** | Due date of the Signature Request (yyyy-mm-dd). Defaults to 6 months after initiation. The date cannot be in the past and cannot be more than one year after initiation. | [optional]
**template_id** | **string** | Create a signature request from an existing template. | [optional]
**external_id** | **string** | Store a custom id that will be added to webhooks &amp; appended to redirect urls. | [optional]
**branding_id** | **string** | Use a specific branding to customize the signature experience. | [optional]
**custom_experience_id** | **string** | Use a specific Custom Experience to customize the signature experience. | [optional]
**documents** | **string[]** | You can directly attach orphan documents to the signature request. | [optional]
**signers** | [**\OpenAPI\Client\Model\CreateSignatureRequestSignersInner[]**](CreateSignatureRequestSignersInner.md) | Can only be used if you add documents at the same time. | [optional]
**workspace_id** | **string** | Scope the signature request to a specific workspace. If template_id is filled and Template is already linked to a Workspace, keep this field to null ; the created Signature Request will be scoped to Template&#39;s Workspace. | [optional]
**audit_trail_locale** | [**\OpenAPI\Client\Model\AuditTrailLocale**](AuditTrailLocale.md) | Define the locale for the generated audit trail. | [optional]
**signers_allowed_to_decline** | **bool** | Allowing signers to decline to sign. | [optional] [default to false]
**email_notification** | [**\OpenAPI\Client\Model\SignatureRequestEmailNotification**](SignatureRequestEmailNotification.md) |  | [optional]
**template_placeholders** | [**\OpenAPI\Client\Model\CreateSignatureRequestTemplatePlaceholders**](CreateSignatureRequestTemplatePlaceholders.md) |  | [optional]
**archiving** | [**\OpenAPI\Client\Model\Archiving**](Archiving.md) |  | [optional]
**labels** | **string[]** | List of Labels to associate with the Signature Request. Labels are identified by their ID. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
