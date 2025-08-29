# OpenAPI\Client\ElectronicSealAuditTrailApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**downloadElectronicSealAuditTrail()**](ElectronicSealAuditTrailApi.md#downloadElectronicSealAuditTrail) | **GET** /electronic_seals/{electronicSealId}/audit_trails/download | Download an Electronic Seal Audit Trail |
| [**getElectronicSealAuditTrail()**](ElectronicSealAuditTrailApi.md#getElectronicSealAuditTrail) | **GET** /electronic_seals/{electronicSealId}/audit_trails | Get an Electronic Seal Audit Trail |


## `downloadElectronicSealAuditTrail()`

```php
downloadElectronicSealAuditTrail($electronic_seal_id): \SplFileObject
```

Download an Electronic Seal Audit Trail

Electronic Seal Audit Trail is only available when the Electronic Seal is \"done\".

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealAuditTrailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$electronic_seal_id = 'electronic_seal_id_example'; // string | Electronic Seal Id

try {
    $result = $apiInstance->downloadElectronicSealAuditTrail($electronic_seal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealAuditTrailApi->downloadElectronicSealAuditTrail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **electronic_seal_id** | **string**| Electronic Seal Id | |

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

## `getElectronicSealAuditTrail()`

```php
getElectronicSealAuditTrail($electronic_seal_id): \OpenAPI\Client\Model\ElectronicSealAuditTrail
```

Get an Electronic Seal Audit Trail

Electronic Seal Audit Trail is only available when the Electronic Seal is \"done\".

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealAuditTrailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$electronic_seal_id = 'electronic_seal_id_example'; // string | Electronic Seal Id

try {
    $result = $apiInstance->getElectronicSealAuditTrail($electronic_seal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealAuditTrailApi->getElectronicSealAuditTrail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **electronic_seal_id** | **string**| Electronic Seal Id | |

### Return type

[**\OpenAPI\Client\Model\ElectronicSealAuditTrail**](../Model/ElectronicSealAuditTrail.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
