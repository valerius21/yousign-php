# OpenAPI\Client\FieldApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId()**](FieldApi.md#deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId) | **DELETE** /signature_requests/{signatureRequestId}/documents/{documentId}/fields/{fieldId} | Delete a Field |
| [**getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields()**](FieldApi.md#getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields) | **GET** /signature_requests/{signatureRequestId}/documents/{documentId}/fields | Lists the Fields of a Signature Request Document. |
| [**postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields()**](FieldApi.md#postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields) | **POST** /signature_requests/{signatureRequestId}/documents/{documentId}/fields | Create a new Field on a Document |
| [**signatureRequestsIdDocumentsIdFieldsIdAnswer()**](FieldApi.md#signatureRequestsIdDocumentsIdFieldsIdAnswer) | **POST** /signature_requests/{signatureRequestId}/documents/{documentId}/fields/{fieldId}/answer | Answer a Field |
| [**updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId()**](FieldApi.md#updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId) | **PATCH** /signature_requests/{signatureRequestId}/documents/{documentId}/fields/{fieldId} | Update a Field |


## `deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId()`

```php
deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId($signature_request_id, $document_id, $field_id)
```

Delete a Field

Deletes a given Field from a Document.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_id = 'document_id_example'; // string | Document Id
$field_id = 'field_id_example'; // string | Field Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId($signature_request_id, $document_id, $field_id);
} catch (Exception $e) {
    echo 'Exception when calling FieldApi->deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_id** | **string**| Document Id | |
| **field_id** | **string**| Field Id | |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields()`

```php
getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields($signature_request_id, $document_id, $after, $limit, $type, $signer_id, $name): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200Response
```

Lists the Fields of a Signature Request Document.

Returns a list of Fields for a given Document. You can limit the number of items returned by using filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_id = 'document_id_example'; // string | Document ID
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$type = {"eq":["text"],"in":["text","checkbox"]}; // object | Filter by `type`. Allowed operators: `eq`, `in`. Example: `type[in]=text,checkbox`
$signer_id = {"eq":["500800fc-3f91-4e86-a9c9-866809a1e3c9"]}; // object | Filter by `signer_id`. Allowed operators: `eq`. Example: `signer_id[eq]=500800fc-3f91-4e86-a9c9-866809a1e3c9`
$name = {"eq":["text 1"]}; // object | Filter by `name`. Allowed operators: `eq`. Example: `name[eq]=text 1`

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields($signature_request_id, $document_id, $after, $limit, $type, $signer_id, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FieldApi->getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_id** | **string**| Document ID | |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **type** | [**object**](../Model/.md)| Filter by &#x60;type&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;in&#x60;. Example: &#x60;type[in]&#x3D;text,checkbox&#x60; | [optional] |
| **signer_id** | [**object**](../Model/.md)| Filter by &#x60;signer_id&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;signer_id[eq]&#x3D;500800fc-3f91-4e86-a9c9-866809a1e3c9&#x60; | [optional] |
| **name** | [**object**](../Model/.md)| Filter by &#x60;name&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;name[eq]&#x3D;text 1&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200Response**](../Model/GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields()`

```php
postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields($signature_request_id, $document_id, $create_field): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner
```

Create a new Field on a Document

Adds a Field to a given Document.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_id = 'document_id_example'; // string | Document ID
$create_field = new \OpenAPI\Client\Model\CreateField(); // \OpenAPI\Client\Model\CreateField

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields($signature_request_id, $document_id, $create_field);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FieldApi->postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_id** | **string**| Document ID | |
| **create_field** | [**\OpenAPI\Client\Model\CreateField**](../Model/CreateField.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner**](../Model/GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `signatureRequestsIdDocumentsIdFieldsIdAnswer()`

```php
signatureRequestsIdDocumentsIdFieldsIdAnswer($signature_request_id, $document_id, $field_id, $field_answer)
```

Answer a Field

This endpoint can be used on ongoing Signature Requests only. It aims to fill a Field value with a Signer input collected in your custom signing interface. The Fields compatible are Text Fields, Checkboxes and Radio Groups.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_id = 'document_id_example'; // string | Document Id
$field_id = 'field_id_example'; // string | Field Id
$field_answer = new \OpenAPI\Client\Model\FieldAnswer(); // \OpenAPI\Client\Model\FieldAnswer

try {
    $apiInstance->signatureRequestsIdDocumentsIdFieldsIdAnswer($signature_request_id, $document_id, $field_id, $field_answer);
} catch (Exception $e) {
    echo 'Exception when calling FieldApi->signatureRequestsIdDocumentsIdFieldsIdAnswer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_id** | **string**| Document Id | |
| **field_id** | **string**| Field Id | |
| **field_answer** | [**\OpenAPI\Client\Model\FieldAnswer**](../Model/FieldAnswer.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId()`

```php
updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId($signature_request_id, $document_id, $field_id, $update_field): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner
```

Update a Field

Updates a given Field. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_id = 'document_id_example'; // string | Document Id
$field_id = 'field_id_example'; // string | Field Id
$update_field = new \OpenAPI\Client\Model\UpdateField(); // \OpenAPI\Client\Model\UpdateField

try {
    $result = $apiInstance->updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId($signature_request_id, $document_id, $field_id, $update_field);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FieldApi->updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_id** | **string**| Document Id | |
| **field_id** | **string**| Field Id | |
| **update_field** | [**\OpenAPI\Client\Model\UpdateField**](../Model/UpdateField.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner**](../Model/GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
