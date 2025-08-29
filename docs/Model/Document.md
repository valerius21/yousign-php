# # Document

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**filename** | **string** |  |
**nature** | **string** |  |
**content_type** | **string** |  |
**sha256** | **string** | Sha256 checksum |
**is_protected** | **bool** |  |
**is_signed** | **bool** |  |
**created_at** | **\DateTime** |  |
**total_pages** | **int** | Number of pages for signable document |
**is_locked** | **bool** | If protected by password and not yet unlocked |
**initials** | [**\OpenAPI\Client\Model\DocumentInitials**](DocumentInitials.md) |  |
**total_anchors** | **int** | Number of parsed anchors from the document. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
