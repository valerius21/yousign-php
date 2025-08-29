# OpenAPI\Client\ArchiveApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getArchivesArchivedFileIdDownload()**](ArchiveApi.md#getArchivesArchivedFileIdDownload) | **GET** /archives/{archivedFileId}/download | Download archived file |
| [**postArchives()**](ArchiveApi.md#postArchives) | **POST** /archives | Direct upload an archived file |


## `getArchivesArchivedFileIdDownload()`

```php
getArchivesArchivedFileIdDownload($archived_file_id): \SplFileObject
```

Download archived file

Download the archived file using the ArchivedFileId.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ArchiveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$archived_file_id = 'archived_file_id_example'; // string | ArchivedFileId

try {
    $result = $apiInstance->getArchivesArchivedFileIdDownload($archived_file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArchiveApi->getArchivesArchivedFileIdDownload: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **archived_file_id** | **string**| ArchivedFileId | |

### Return type

**\SplFileObject**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/octet-stream`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postArchives()`

```php
postArchives($file, $workspace_id, $archive_y, $tags, $expired_at): \OpenAPI\Client\Model\ArchivedFile
```

Direct upload an archived file

Archive a file in a secure digital safe for 10 years

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ArchiveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | File to be uploaded
$workspace_id = 'workspace_id_example'; // string
$archive_y = 'archive_y_example'; // string
$tags = array('tags_example'); // string[] | Tags for the file
$expired_at = 'expired_at_example'; // string | Expiration date of the file

try {
    $result = $apiInstance->postArchives($file, $workspace_id, $archive_y, $tags, $expired_at);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArchiveApi->postArchives: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| File to be uploaded | |
| **workspace_id** | **string**|  | [optional] |
| **archive_y** | **string**|  | [optional] |
| **tags** | [**string[]**](../Model/string.md)| Tags for the file | [optional] |
| **expired_at** | **string**| Expiration date of the file | [optional] |

### Return type

[**\OpenAPI\Client\Model\ArchivedFile**](../Model/ArchivedFile.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
