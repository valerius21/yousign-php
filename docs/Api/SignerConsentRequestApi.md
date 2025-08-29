# OpenAPI\Client\SignerConsentRequestApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId()**](SignerConsentRequestApi.md#deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId) | **DELETE** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId} | Delete a Signer Consent Request |
| [**deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId()**](SignerConsentRequestApi.md#deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId) | **DELETE** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId}/signers/{signerId} | Remove a Signer from a given Signer Consent Request |
| [**getSignatureRequestsSignatureRequestIdSignerConsentRequests()**](SignerConsentRequestApi.md#getSignatureRequestsSignatureRequestIdSignerConsentRequests) | **GET** /signature_requests/{signatureRequestId}/consent_requests | List Signer Consent Requests of the Signature Request |
| [**patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId()**](SignerConsentRequestApi.md#patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId) | **PATCH** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId} | Update a Signer Consent Request |
| [**postSignatureRequestsSignatureRequestIdConsentRequests()**](SignerConsentRequestApi.md#postSignatureRequestsSignatureRequestIdConsentRequests) | **POST** /signature_requests/{signatureRequestId}/consent_requests | Add Signer Consent Request to a Signature Request |
| [**putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId()**](SignerConsentRequestApi.md#putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId) | **PUT** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId}/signers/{signerId} | Adds a Signer to a given Signer Consent Request |


## `deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId()`

```php
deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId($signature_request_id, $consent_request_id)
```

Delete a Signer Consent Request

Delete a Signer Consent Request from signature request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerConsentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$consent_request_id = 'consent_request_id_example'; // string | Signer Consent Request Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId($signature_request_id, $consent_request_id);
} catch (Exception $e) {
    echo 'Exception when calling SignerConsentRequestApi->deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **consent_request_id** | **string**| Signer Consent Request Id | |

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

## `deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId()`

```php
deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId($signature_request_id, $consent_request_id, $signer_id)
```

Remove a Signer from a given Signer Consent Request

Remove a Signer from a given Signer Consent Request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerConsentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$consent_request_id = 'consent_request_id_example'; // string | Signer Consent Request Id
$signer_id = 'signer_id_example'; // string | Signer Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId($signature_request_id, $consent_request_id, $signer_id);
} catch (Exception $e) {
    echo 'Exception when calling SignerConsentRequestApi->deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **consent_request_id** | **string**| Signer Consent Request Id | |
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

## `getSignatureRequestsSignatureRequestIdSignerConsentRequests()`

```php
getSignatureRequestsSignatureRequestIdSignerConsentRequests($signature_request_id): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdSignerConsentRequests200Response
```

List Signer Consent Requests of the Signature Request

Returns a list of Signer Consent Requests for a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerConsentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdSignerConsentRequests($signature_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerConsentRequestApi->getSignatureRequestsSignatureRequestIdSignerConsentRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdSignerConsentRequests200Response**](../Model/GetSignatureRequestsSignatureRequestIdSignerConsentRequests200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId()`

```php
patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId($signature_request_id, $consent_request_id, $update_signer_consent_request): \OpenAPI\Client\Model\SignerConsentRequest
```

Update a Signer Consent Request

Updates a given Signer Consent Request. Any parameters not provided are left unchanged. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerConsentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$consent_request_id = 'consent_request_id_example'; // string | Signer Consent Request Id
$update_signer_consent_request = new \OpenAPI\Client\Model\UpdateSignerConsentRequest(); // \OpenAPI\Client\Model\UpdateSignerConsentRequest

try {
    $result = $apiInstance->patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId($signature_request_id, $consent_request_id, $update_signer_consent_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerConsentRequestApi->patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **consent_request_id** | **string**| Signer Consent Request Id | |
| **update_signer_consent_request** | [**\OpenAPI\Client\Model\UpdateSignerConsentRequest**](../Model/UpdateSignerConsentRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignerConsentRequest**](../Model/SignerConsentRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdConsentRequests()`

```php
postSignatureRequestsSignatureRequestIdConsentRequests($signature_request_id, $create_signer_consent_request): \OpenAPI\Client\Model\SignerConsentRequest
```

Add Signer Consent Request to a Signature Request

Adds a Signer Consent Request to a given Signature Request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerConsentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$create_signer_consent_request = new \OpenAPI\Client\Model\CreateSignerConsentRequest(); // \OpenAPI\Client\Model\CreateSignerConsentRequest

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdConsentRequests($signature_request_id, $create_signer_consent_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignerConsentRequestApi->postSignatureRequestsSignatureRequestIdConsentRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **create_signer_consent_request** | [**\OpenAPI\Client\Model\CreateSignerConsentRequest**](../Model/CreateSignerConsentRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignerConsentRequest**](../Model/SignerConsentRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId()`

```php
putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId($signature_request_id, $consent_request_id, $signer_id)
```

Adds a Signer to a given Signer Consent Request

Adds a Signer to a given Signer Consent Request. This action is only permitted when the Signature Request is a draft.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignerConsentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$consent_request_id = 'consent_request_id_example'; // string | Signer Consent Request Id
$signer_id = 'signer_id_example'; // string | Signer Id

try {
    $apiInstance->putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId($signature_request_id, $consent_request_id, $signer_id);
} catch (Exception $e) {
    echo 'Exception when calling SignerConsentRequestApi->putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **consent_request_id** | **string**| Signer Consent Request Id | |
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
