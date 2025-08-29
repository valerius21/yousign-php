# # CreateCustomExperience

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | This property cannot start or end with whitespace, does not allow HTML tags, URL or email. |
**landing_page_disabled** | **bool** |  | [optional] [default to false]
**side_panel_disabled** | **bool** |  | [optional] [default to false]
**background_color** | **string** | Hexadecimal color value | [optional]
**button_color** | **string** | Hexadecimal color value | [optional]
**text_color** | **string** | Hexadecimal color value | [optional]
**text_button_color** | **string** | Hexadecimal color value | [optional]
**disabled_notifications** | [**\OpenAPI\Client\Model\CustomExperienceDisabledNotificationsType[]**](CustomExperienceDisabledNotificationsType.md) |  | [optional]
**email_logo_disabled** | **bool** |  | [optional] [default to false]
**email_header_text_disabled** | **bool** |  | [optional] [default to false]
**email_footer_signature_disabled** | **bool** |  | [optional] [default to false]
**email_expiration_text_disabled** | **bool** |  | [optional] [default to false]
**recipients_activity_disabled** | **bool** |  | [optional] [default to true]
**download_documents_disabled** | **bool** | If false, signers won&#39;t be able to download documents before signing. | [optional] [default to false]
**redirect_urls** | [**\OpenAPI\Client\Model\CreateCustomExperienceRedirectUrls**](CreateCustomExperienceRedirectUrls.md) |  | [optional]
**logo_layout** | [**\OpenAPI\Client\Model\LogoLayout**](LogoLayout.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
