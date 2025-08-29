# OpenAPI\Client\ElectronicSealDocumentApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**downloadElectronicSealDocument()**](ElectronicSealDocumentApi.md#downloadElectronicSealDocument) | **GET** /electronic_seal_documents/{electronicSealDocumentId}/download | Download an Electronic Seal Document |
| [**uploadElectronicSealDocument()**](ElectronicSealDocumentApi.md#uploadElectronicSealDocument) | **POST** /electronic_seal_documents | Create an Electronic Seal Document |


## `downloadElectronicSealDocument()`

```php
downloadElectronicSealDocument($electronic_seal_document_id): \SplFileObject
```

Download an Electronic Seal Document

Download a given Electronic Seal Document.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealDocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$electronic_seal_document_id = 'electronic_seal_document_id_example'; // string | Electronic Seal Id

try {
    $result = $apiInstance->downloadElectronicSealDocument($electronic_seal_document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealDocumentApi->downloadElectronicSealDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **electronic_seal_document_id** | **string**| Electronic Seal Id | |

### Return type

**\SplFileObject**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadElectronicSealDocument()`

```php
uploadElectronicSealDocument($file, $password): \OpenAPI\Client\Model\ElectronicSealDocument
```

Create an Electronic Seal Document

Create an Electronic Seal Document from an other one.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealDocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | Binary file. Accepted formats: PDF.
$password = 'password_example'; // string | The password required to unlock the document if it is protected.

try {
    $result = $apiInstance->uploadElectronicSealDocument($file, $password);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealDocumentApi->uploadElectronicSealDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| Binary file. Accepted formats: PDF. | |
| **password** | **string**| The password required to unlock the document if it is protected. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ElectronicSealDocument**](../Model/ElectronicSealDocument.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`, `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
