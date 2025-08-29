# OpenAPI\Client\MetadataApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSignatureRequestsSignatureRequestIdMetadata()**](MetadataApi.md#deleteSignatureRequestsSignatureRequestIdMetadata) | **DELETE** /signature_requests/{signatureRequestId}/metadata | Delete the Signature Request Metadata |
| [**getSignatureRequestsSignatureRequestIdMetadata()**](MetadataApi.md#getSignatureRequestsSignatureRequestIdMetadata) | **GET** /signature_requests/{signatureRequestId}/metadata | Get the Signature Request Metadata |
| [**postSignatureRequestsSignatureRequestIdMetadata()**](MetadataApi.md#postSignatureRequestsSignatureRequestIdMetadata) | **POST** /signature_requests/{signatureRequestId}/metadata | Attach Metadata to a Signature Request |
| [**putSignatureRequestsSignatureRequestIdMetadata()**](MetadataApi.md#putSignatureRequestsSignatureRequestIdMetadata) | **PUT** /signature_requests/{signatureRequestId}/metadata | Update Metadata of a Signature Request |


## `deleteSignatureRequestsSignatureRequestIdMetadata()`

```php
deleteSignatureRequestsSignatureRequestIdMetadata($signature_request_id)
```

Delete the Signature Request Metadata

Deletes the Metadata of a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdMetadata($signature_request_id);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->deleteSignatureRequestsSignatureRequestIdMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

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

## `getSignatureRequestsSignatureRequestIdMetadata()`

```php
getSignatureRequestsSignatureRequestIdMetadata($signature_request_id): \OpenAPI\Client\Model\Metadata
```

Get the Signature Request Metadata

Retrieves the Metadata of a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdMetadata($signature_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->getSignatureRequestsSignatureRequestIdMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

### Return type

[**\OpenAPI\Client\Model\Metadata**](../Model/Metadata.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdMetadata()`

```php
postSignatureRequestsSignatureRequestIdMetadata($signature_request_id, $metadata): \OpenAPI\Client\Model\Metadata
```

Attach Metadata to a Signature Request

Add Metadata to a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$metadata = new \OpenAPI\Client\Model\Metadata(); // \OpenAPI\Client\Model\Metadata

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdMetadata($signature_request_id, $metadata);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->postSignatureRequestsSignatureRequestIdMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **metadata** | [**\OpenAPI\Client\Model\Metadata**](../Model/Metadata.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Metadata**](../Model/Metadata.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `putSignatureRequestsSignatureRequestIdMetadata()`

```php
putSignatureRequestsSignatureRequestIdMetadata($signature_request_id, $metadata): \OpenAPI\Client\Model\Metadata
```

Update Metadata of a Signature Request

Updates the Metadata of a given Signature Request. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$metadata = new \OpenAPI\Client\Model\Metadata(); // \OpenAPI\Client\Model\Metadata

try {
    $result = $apiInstance->putSignatureRequestsSignatureRequestIdMetadata($signature_request_id, $metadata);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->putSignatureRequestsSignatureRequestIdMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **metadata** | [**\OpenAPI\Client\Model\Metadata**](../Model/Metadata.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Metadata**](../Model/Metadata.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
