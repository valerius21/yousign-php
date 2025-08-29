# OpenAPI\Client\CustomExperienceApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteCustomExperience()**](CustomExperienceApi.md#deleteCustomExperience) | **DELETE** /custom_experiences/{customExperienceId} | Delete a Custom Experience |
| [**deleteCustomExperienceLogo()**](CustomExperienceApi.md#deleteCustomExperienceLogo) | **DELETE** /custom_experiences/{customExperienceId}/logo | Delete a Custom Experience logo |
| [**getCustomExperiences()**](CustomExperienceApi.md#getCustomExperiences) | **GET** /custom_experiences | List Custom Experiences |
| [**getCustomExperiencesCustomExperienceId()**](CustomExperienceApi.md#getCustomExperiencesCustomExperienceId) | **GET** /custom_experiences/{customExperienceId} | Get a Custom Experience |
| [**patchCustomExperienceLogo()**](CustomExperienceApi.md#patchCustomExperienceLogo) | **POST** /custom_experiences/{customExperienceId}/logo | Update a Custom Experience logo |
| [**patchCustomExperiencesCustomExperienceId()**](CustomExperienceApi.md#patchCustomExperiencesCustomExperienceId) | **PATCH** /custom_experiences/{customExperienceId} | Update a Custom Experience |
| [**postCustomExperience()**](CustomExperienceApi.md#postCustomExperience) | **POST** /custom_experiences | Create a Custom Experience |


## `deleteCustomExperience()`

```php
deleteCustomExperience($custom_experience_id)
```

Delete a Custom Experience

Deletes a given Custom Experience.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$custom_experience_id = 'custom_experience_id_example'; // string | Custom Experience Id

try {
    $apiInstance->deleteCustomExperience($custom_experience_id);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->deleteCustomExperience: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **custom_experience_id** | **string**| Custom Experience Id | |

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

## `deleteCustomExperienceLogo()`

```php
deleteCustomExperienceLogo($custom_experience_id)
```

Delete a Custom Experience logo

Deletes the logo of a Custom Experience.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$custom_experience_id = 'custom_experience_id_example'; // string | Custom Experience Id

try {
    $apiInstance->deleteCustomExperienceLogo($custom_experience_id);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->deleteCustomExperienceLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **custom_experience_id** | **string**| Custom Experience Id | |

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

## `getCustomExperiences()`

```php
getCustomExperiences($after, $limit): \OpenAPI\Client\Model\GetCustomExperiences200Response
```

List Custom Experiences

Returns the list of all Custom Experiences in your Organization. You can limit the number of items returned by using pagination.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.

try {
    $result = $apiInstance->getCustomExperiences($after, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->getCustomExperiences: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |

### Return type

[**\OpenAPI\Client\Model\GetCustomExperiences200Response**](../Model/GetCustomExperiences200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCustomExperiencesCustomExperienceId()`

```php
getCustomExperiencesCustomExperienceId($custom_experience_id): \OpenAPI\Client\Model\CustomExperience
```

Get a Custom Experience

Retrieves a given Custom Experience.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$custom_experience_id = 'custom_experience_id_example'; // string | Custom Experience Id

try {
    $result = $apiInstance->getCustomExperiencesCustomExperienceId($custom_experience_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->getCustomExperiencesCustomExperienceId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **custom_experience_id** | **string**| Custom Experience Id | |

### Return type

[**\OpenAPI\Client\Model\CustomExperience**](../Model/CustomExperience.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchCustomExperienceLogo()`

```php
patchCustomExperienceLogo($custom_experience_id, $file): \OpenAPI\Client\Model\CustomExperience
```

Update a Custom Experience logo

Updates the logo of a given Custom Experience by uploading the image of your choice.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$custom_experience_id = 'custom_experience_id_example'; // string | Custom Experience Id
$file = '/path/to/file.txt'; // \SplFileObject

try {
    $result = $apiInstance->patchCustomExperienceLogo($custom_experience_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->patchCustomExperienceLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **custom_experience_id** | **string**| Custom Experience Id | |
| **file** | **\SplFileObject****\SplFileObject**|  | |

### Return type

[**\OpenAPI\Client\Model\CustomExperience**](../Model/CustomExperience.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchCustomExperiencesCustomExperienceId()`

```php
patchCustomExperiencesCustomExperienceId($custom_experience_id, $update_custom_experience): \OpenAPI\Client\Model\CustomExperience
```

Update a Custom Experience

Updates a given Custom Experience. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$custom_experience_id = 'custom_experience_id_example'; // string | Custom Experience Id
$update_custom_experience = new \OpenAPI\Client\Model\UpdateCustomExperience(); // \OpenAPI\Client\Model\UpdateCustomExperience

try {
    $result = $apiInstance->patchCustomExperiencesCustomExperienceId($custom_experience_id, $update_custom_experience);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->patchCustomExperiencesCustomExperienceId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **custom_experience_id** | **string**| Custom Experience Id | |
| **update_custom_experience** | [**\OpenAPI\Client\Model\UpdateCustomExperience**](../Model/UpdateCustomExperience.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomExperience**](../Model/CustomExperience.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postCustomExperience()`

```php
postCustomExperience($create_custom_experience): \OpenAPI\Client\Model\CustomExperience
```

Create a Custom Experience

Creates a new Custom Experience.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomExperienceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_custom_experience = new \OpenAPI\Client\Model\CreateCustomExperience(); // \OpenAPI\Client\Model\CreateCustomExperience

try {
    $result = $apiInstance->postCustomExperience($create_custom_experience);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomExperienceApi->postCustomExperience: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_custom_experience** | [**\OpenAPI\Client\Model\CreateCustomExperience**](../Model/CreateCustomExperience.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomExperience**](../Model/CustomExperience.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
