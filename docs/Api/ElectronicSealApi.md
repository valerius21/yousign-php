# OpenAPI\Client\ElectronicSealApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getElectronicSeal()**](ElectronicSealApi.md#getElectronicSeal) | **GET** /electronic_seals/{electronicSealId} | Get an Electronic Seal |
| [**listElectronicSealImages()**](ElectronicSealApi.md#listElectronicSealImages) | **GET** /electronic_seal_images | List Electronic Seal Images |
| [**postElectronicSeals()**](ElectronicSealApi.md#postElectronicSeals) | **POST** /electronic_seals | Create an Electronic Seal |


## `getElectronicSeal()`

```php
getElectronicSeal($electronic_seal_id): \OpenAPI\Client\Model\ElectronicSeal
```

Get an Electronic Seal

Retrieves a given Electronic Seal.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$electronic_seal_id = 'electronic_seal_id_example'; // string | Electronic Seal Id

try {
    $result = $apiInstance->getElectronicSeal($electronic_seal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealApi->getElectronicSeal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **electronic_seal_id** | **string**| Electronic Seal Id | |

### Return type

[**\OpenAPI\Client\Model\ElectronicSeal**](../Model/ElectronicSeal.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listElectronicSealImages()`

```php
listElectronicSealImages($after, $limit): \OpenAPI\Client\Model\ListElectronicSealImages200Response
```

List Electronic Seal Images

Lists Electronic Seal Images. The list is paginated and can be filtered by the `after` cursor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.

try {
    $result = $apiInstance->listElectronicSealImages($after, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealApi->listElectronicSealImages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |

### Return type

[**\OpenAPI\Client\Model\ListElectronicSealImages200Response**](../Model/ListElectronicSealImages200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postElectronicSeals()`

```php
postElectronicSeals($create_electronic_seal_payload): \OpenAPI\Client\Model\ElectronicSeal
```

Create an Electronic Seal

Create a new Electronic Seal

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_electronic_seal_payload = new \OpenAPI\Client\Model\CreateElectronicSealPayload(); // \OpenAPI\Client\Model\CreateElectronicSealPayload

try {
    $result = $apiInstance->postElectronicSeals($create_electronic_seal_payload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealApi->postElectronicSeals: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_electronic_seal_payload** | [**\OpenAPI\Client\Model\CreateElectronicSealPayload**](../Model/CreateElectronicSealPayload.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ElectronicSeal**](../Model/ElectronicSeal.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
