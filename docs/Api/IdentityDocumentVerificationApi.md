# OpenAPI\Client\IdentityDocumentVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsIdentityDocuments()**](IdentityDocumentVerificationApi.md#getVerificationsIdentityDocuments) | **GET** /verifications/identity_documents | List Identity Document Verifications |
| [**getVerificationsIdentityDocumentsId()**](IdentityDocumentVerificationApi.md#getVerificationsIdentityDocumentsId) | **GET** /verifications/identity_documents/{identityDocumentVerificationId} | Retrieve an Identity Document Verification |
| [**postVerificationsIdentityDocuments()**](IdentityDocumentVerificationApi.md#postVerificationsIdentityDocuments) | **POST** /verifications/identity_documents | Initiate a new Identity Document Verification |


## `getVerificationsIdentityDocuments()`

```php
getVerificationsIdentityDocuments($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsIdentityDocuments200Response
```

List Identity Document Verifications

Returns the list of all Identity Document Verifications within your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IdentityDocumentVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$status = {"eq":["verified"]}; // object | Filter by `status`. Allowed operators: `eq`. Example: `status[eq]=verified`
$workspace_id = {"eq":["9b6ed2f3-244f-487a-baa1-bbe4f51c8748"]}; // object | Filter by `workspace_id`. Allowed operators: `eq`. Example: `workspace_id[eq]=9b6ed2f3-244f-487a-baa1-bbe4f51c8748`

try {
    $result = $apiInstance->getVerificationsIdentityDocuments($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityDocumentVerificationApi->getVerificationsIdentityDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **status** | [**object**](../Model/.md)| Filter by &#x60;status&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;status[eq]&#x3D;verified&#x60; | [optional] |
| **workspace_id** | [**object**](../Model/.md)| Filter by &#x60;workspace_id&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;workspace_id[eq]&#x3D;9b6ed2f3-244f-487a-baa1-bbe4f51c8748&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetVerificationsIdentityDocuments200Response**](../Model/GetVerificationsIdentityDocuments200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsIdentityDocumentsId()`

```php
getVerificationsIdentityDocumentsId($identity_document_verification_id): \OpenAPI\Client\Model\IdentityDocumentFull
```

Retrieve an Identity Document Verification

Get the detailed results of an Identity Document Verification, including the status of the verification, the reasons in case of rejection and the data extracted from the Identity Document.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IdentityDocumentVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identity_document_verification_id = 'identity_document_verification_id_example'; // string | Identity Document Verification Id

try {
    $result = $apiInstance->getVerificationsIdentityDocumentsId($identity_document_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityDocumentVerificationApi->getVerificationsIdentityDocumentsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identity_document_verification_id** | **string**| Identity Document Verification Id | |

### Return type

[**\OpenAPI\Client\Model\IdentityDocumentFull**](../Model/IdentityDocumentFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsIdentityDocuments()`

```php
postVerificationsIdentityDocuments($first_name, $last_name, $type, $file, $additional_file, $workspace_id): \OpenAPI\Client\Model\IdentityDocumentFull
```

Initiate a new Identity Document Verification

Verify a person's Identity Document by sending the file containing their Identity Document (identity card, passport, residence permit or driving license).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IdentityDocumentVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$first_name = 'first_name_example'; // string | Please provide the holder first name, exactly as it appears on the ID document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don't provide it as part of the name.
$last_name = 'last_name_example'; // string | Please provide the holder last name, exactly as it appears on the ID document birth name. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don't provide it as part of the name.
$type = 'type_example'; // string | The document type to verify
$file = '/path/to/file.txt'; // \SplFileObject | The identity document file to verify. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx.
$additional_file = '/path/to/file.txt'; // \SplFileObject | Additional document file, such as the back side of an identity card. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx.
$workspace_id = 'workspace_id_example'; // string | Scopes the verification to a specific workspace. Defaults to the default workspace if not specified.

try {
    $result = $apiInstance->postVerificationsIdentityDocuments($first_name, $last_name, $type, $file, $additional_file, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityDocumentVerificationApi->postVerificationsIdentityDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **first_name** | **string**| Please provide the holder first name, exactly as it appears on the ID document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don&#39;t provide it as part of the name. | [optional] |
| **last_name** | **string**| Please provide the holder last name, exactly as it appears on the ID document birth name. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don&#39;t provide it as part of the name. | [optional] |
| **type** | **string**| The document type to verify | [optional] |
| **file** | **\SplFileObject****\SplFileObject**| The identity document file to verify. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx. | [optional] |
| **additional_file** | **\SplFileObject****\SplFileObject**| Additional document file, such as the back side of an identity card. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx. | [optional] |
| **workspace_id** | **string**| Scopes the verification to a specific workspace. Defaults to the default workspace if not specified. | [optional] |

### Return type

[**\OpenAPI\Client\Model\IdentityDocumentFull**](../Model/IdentityDocumentFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
