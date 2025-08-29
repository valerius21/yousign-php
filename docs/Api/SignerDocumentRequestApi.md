# OpenAPI\Client\SignerDocumentRequestApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId()**](SignerDocumentRequestApi.md#deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId) | **DELETE** /signature_requests/{signatureRequestId}/document_requests/{documentRequestId} | Delete a Signer Document Request |
| [**deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId()**](SignerDocumentRequestApi.md#deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId) | **DELETE** /signature_requests/{signatureRequestId}/document_requests/{documentRequestId}/signers/{signerId} | Remove a Signer to a given Signer Document Request |
| [**deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments()**](SignerDocumentRequestApi.md#deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments) | **DELETE** /signature_requests/{signatureRequestId}/signers/{signerId}/documents | Delete the Documents uploaded by a Signer |
| [**getSignatureRequestsSignatureRequestIdSignerDocumentRequests()**](SignerDocumentRequestApi.md#getSignatureRequestsSignatureRequestIdSignerDocumentRequests) | **GET** /signature_requests/{signatureRequestId}/document_requests | List Signer Document Requests of the Signature Request |
| [**getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments()**](SignerDocumentRequestApi.md#getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId}/documents | List the Signer Documents of a Signer |
| [**getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId()**](SignerDocumentRequestApi.md#getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId}/documents/{signerDocumentId}/download | Download a Signer Document |
| [**postSignatureRequestsSignatureRequestIdDocumentRequests()**](SignerDocumentRequestApi.md#postSignatureRequestsSignatureRequestIdDocumentRequests) | **POST** /signature_requests/{signatureRequestId}/document_requests | Add Signer Document Request to a Signature Request |
| [**putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId()**](SignerDocumentRequestApi.md#putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId) | **PUT** /signature_requests/{signatureRequestId}/document_requests/{documentRequestId}/signers/{signerId} | Adds a Signer to a given Signer Document Request |


## `deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId()`

```php
deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId($signature_request_id, $document_request_id)
```

Delete a Signer Document Request

Delete a Signer Document Request from signature request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_request_id = 'document_request_id_example'; // string | Signer Document Request Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId($signature_request_id, $document_request_id);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_request_id** | **string**| Signer Document Request Id | |

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

## `deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId()`

```php
deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId($signature_request_id, $document_request_id, $signer_id)
```

Remove a Signer to a given Signer Document Request

Remove a Signer to a given Signer Document Request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_request_id = 'document_request_id_example'; // string | Signer Document Request Id
$signer_id = 'signer_id_example'; // string | Signer Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId($signature_request_id, $document_request_id, $signer_id);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_request_id** | **string**| Signer Document Request Id | |
| **signer_id** | **string**| Signer Id | |

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

## `deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments()`

```php
deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments($signature_request_id, $signer_id)
```

Delete the Documents uploaded by a Signer

Deletes all documents uploaded by a given Signer for a specific Signature Request. Deletion is only possible when Signer status is `signed`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$signer_id = 'signer_id_example'; // string | Signer Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments($signature_request_id, $signer_id);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **signer_id** | **string**| Signer Id | |

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

## `getSignatureRequestsSignatureRequestIdSignerDocumentRequests()`

```php
getSignatureRequestsSignatureRequestIdSignerDocumentRequests($signature_request_id): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdSignerDocumentRequests200Response
```

List Signer Document Requests of the Signature Request

Returns a list of Signer Document Requests for a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdSignerDocumentRequests($signature_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->getSignatureRequestsSignatureRequestIdSignerDocumentRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdSignerDocumentRequests200Response**](../Model/GetSignatureRequestsSignatureRequestIdSignerDocumentRequests200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments()`

```php
getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments($signature_request_id, $signer_id): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdSignersSignerIdDocuments200Response
```

List the Signer Documents of a Signer

Returns a list of Documents uploaded by a given Signer. Only possible when Signer status is `signed`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$signer_id = 'signer_id_example'; // string | Signer Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments($signature_request_id, $signer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **signer_id** | **string**| Signer Id | |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdSignersSignerIdDocuments200Response**](../Model/GetSignatureRequestsSignatureRequestIdSignersSignerIdDocuments200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId()`

```php
getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId($signature_request_id, $signer_id, $signer_document_id): \SplFileObject
```

Download a Signer Document

Downloads a Document uploaded by a given Signer. Only possible when Signer status is `signed`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$signer_id = 'signer_id_example'; // string | Signer Id
$signer_document_id = 'signer_document_id_example'; // string | Signer Document Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId($signature_request_id, $signer_id, $signer_document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **signer_id** | **string**| Signer Id | |
| **signer_document_id** | **string**| Signer Document Id | |

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

## `postSignatureRequestsSignatureRequestIdDocumentRequests()`

```php
postSignatureRequestsSignatureRequestIdDocumentRequests($signature_request_id, $create_signer_document_request): \OpenAPI\Client\Model\SignerDocumentRequest
```

Add Signer Document Request to a Signature Request

Adds a Signer Document Request to a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$create_signer_document_request = new \OpenAPI\Client\Model\CreateSignerDocumentRequest(); // \OpenAPI\Client\Model\CreateSignerDocumentRequest

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdDocumentRequests($signature_request_id, $create_signer_document_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->postSignatureRequestsSignatureRequestIdDocumentRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **create_signer_document_request** | [**\OpenAPI\Client\Model\CreateSignerDocumentRequest**](../Model/CreateSignerDocumentRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignerDocumentRequest**](../Model/SignerDocumentRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId()`

```php
putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId($signature_request_id, $document_request_id, $signer_id): \OpenAPI\Client\Model\SignerDocumentRequest
```

Adds a Signer to a given Signer Document Request

Adds a Signer to a given Signer Document Request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerDocumentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$document_request_id = 'document_request_id_example'; // string | Signer Document Request Id
$signer_id = 'signer_id_example'; // string | Signer Id

try {
    $result = $apiInstance->putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId($signature_request_id, $document_request_id, $signer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerDocumentRequestApi->putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **document_request_id** | **string**| Signer Document Request Id | |
| **signer_id** | **string**| Signer Id | |

### Return type

[**\OpenAPI\Client\Model\SignerDocumentRequest**](../Model/SignerDocumentRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
