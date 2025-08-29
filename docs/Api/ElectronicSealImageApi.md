# OpenAPI\Client\ElectronicSealImageApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteElectronicSealImage()**](ElectronicSealImageApi.md#deleteElectronicSealImage) | **DELETE** /electronic_seal_images/{electronicSealImageId} | Delete an Electronic Seal Image |
| [**downloadElectronicSealImage()**](ElectronicSealImageApi.md#downloadElectronicSealImage) | **GET** /electronic_seal_images/{electronicSealImageId}/download | Download an Electronic Seal Image |
| [**uploadElectronicSealImage()**](ElectronicSealImageApi.md#uploadElectronicSealImage) | **POST** /electronic_seal_images | Upload an Electronic Seal Image |


## `deleteElectronicSealImage()`

```php
deleteElectronicSealImage($electronic_seal_image_id)
```

Delete an Electronic Seal Image

Deletes a given Electronic Seal Image.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$electronic_seal_image_id = 'electronic_seal_image_id_example'; // string | Electronic Seal Image Id

try {
    $apiInstance->deleteElectronicSealImage($electronic_seal_image_id);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealImageApi->deleteElectronicSealImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **electronic_seal_image_id** | **string**| Electronic Seal Image Id | |

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

## `downloadElectronicSealImage()`

```php
downloadElectronicSealImage($electronic_seal_image_id): \SplFileObject
```

Download an Electronic Seal Image

Download a given Electronic Seal Image.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$electronic_seal_image_id = 'electronic_seal_image_id_example'; // string | Electronic Seal Image Id

try {
    $result = $apiInstance->downloadElectronicSealImage($electronic_seal_image_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealImageApi->downloadElectronicSealImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **electronic_seal_image_id** | **string**| Electronic Seal Image Id | |

### Return type

**\SplFileObject**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `image/png`, `image/jpg`, `image/gif`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadElectronicSealImage()`

```php
uploadElectronicSealImage($file, $name): \OpenAPI\Client\Model\ElectronicSealImage
```

Upload an Electronic Seal Image

Upload an Electronic Seal Image to use for creating an Electronic Seal (can be used for several Electronic Seals).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ElectronicSealImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | Seal Image to be displayed on a sealed Document. Accepted formats: PNG/JPG/GIF, max 500 Ko.
$name = 'name_example'; // string | Name of the Seal Image.

try {
    $result = $apiInstance->uploadElectronicSealImage($file, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ElectronicSealImageApi->uploadElectronicSealImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| Seal Image to be displayed on a sealed Document. Accepted formats: PNG/JPG/GIF, max 500 Ko. | |
| **name** | **string**| Name of the Seal Image. | |

### Return type

[**\OpenAPI\Client\Model\ElectronicSealImage**](../Model/ElectronicSealImage.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
