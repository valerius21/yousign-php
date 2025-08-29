# OpenAPI\Client\LabelApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteLabelsId()**](LabelApi.md#deleteLabelsId) | **DELETE** /labels/{labelId} | Delete a Label |
| [**deleteSignatureRequestsIdLabelsId()**](LabelApi.md#deleteSignatureRequestsIdLabelsId) | **DELETE** /signature_requests/{signatureRequestId}/labels/{labelId} | Remove Label from a Signature Request |
| [**getLabels()**](LabelApi.md#getLabels) | **GET** /labels | List Labels |
| [**getLabelsId()**](LabelApi.md#getLabelsId) | **GET** /labels/{labelId} | Get a Label |
| [**getSignatureRequestsIdLabels()**](LabelApi.md#getSignatureRequestsIdLabels) | **GET** /signature_requests/{signatureRequestId}/labels | List Labels of a Signature Request |
| [**patchLabelId()**](LabelApi.md#patchLabelId) | **PATCH** /labels/{labelId} | Update a Label |
| [**postLabels()**](LabelApi.md#postLabels) | **POST** /labels | Create a new Label |
| [**putSignatureRequestsIdLabelsId()**](LabelApi.md#putSignatureRequestsIdLabelsId) | **PUT** /signature_requests/{signatureRequestId}/labels/{labelId} | Associate a Label with a Signature Request |


## `deleteLabelsId()`

```php
deleteLabelsId($label_id)
```

Delete a Label

Deletes a given Label. This will remove the Label from all Signature Requests it is associated with.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$label_id = 'label_id_example'; // string | Label Id

try {
    $apiInstance->deleteLabelsId($label_id);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->deleteLabelsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **label_id** | **string**| Label Id | |

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

## `deleteSignatureRequestsIdLabelsId()`

```php
deleteSignatureRequestsIdLabelsId($signature_request_id, $label_id)
```

Remove Label from a Signature Request

Removes a Label from a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$label_id = 'label_id_example'; // string | Label Id

try {
    $apiInstance->deleteSignatureRequestsIdLabelsId($signature_request_id, $label_id);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->deleteSignatureRequestsIdLabelsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **label_id** | **string**| Label Id | |

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

## `getLabels()`

```php
getLabels($after, $limit, $name): \OpenAPI\Client\Model\GetLabels200Response
```

List Labels

Returns the list of all the Labels within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$name = {"eq":["Miscellaneous"]}; // object | Filter by `name`. Allowed operators: `eq`, `in`. Example: `name[eq]=Miscellaneous`

try {
    $result = $apiInstance->getLabels($after, $limit, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->getLabels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **name** | [**object**](../Model/.md)| Filter by &#x60;name&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;in&#x60;. Example: &#x60;name[eq]&#x3D;Miscellaneous&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetLabels200Response**](../Model/GetLabels200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLabelsId()`

```php
getLabelsId($label_id): \OpenAPI\Client\Model\Label
```

Get a Label

Retrieves a given Label within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$label_id = 'label_id_example'; // string | Label Id

try {
    $result = $apiInstance->getLabelsId($label_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->getLabelsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **label_id** | **string**| Label Id | |

### Return type

[**\OpenAPI\Client\Model\Label**](../Model/Label.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSignatureRequestsIdLabels()`

```php
getSignatureRequestsIdLabels($signature_request_id): \OpenAPI\Client\Model\GetSignatureRequestsIdLabels200Response
```

List Labels of a Signature Request

Returns the list of Labels associated with a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $result = $apiInstance->getSignatureRequestsIdLabels($signature_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->getSignatureRequestsIdLabels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsIdLabels200Response**](../Model/GetSignatureRequestsIdLabels200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchLabelId()`

```php
patchLabelId($label_id, $update_label): \OpenAPI\Client\Model\Label
```

Update a Label

Updates a given Label. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$label_id = 'label_id_example'; // string | Label Id
$update_label = new \OpenAPI\Client\Model\UpdateLabel(); // \OpenAPI\Client\Model\UpdateLabel

try {
    $result = $apiInstance->patchLabelId($label_id, $update_label);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->patchLabelId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **label_id** | **string**| Label Id | |
| **update_label** | [**\OpenAPI\Client\Model\UpdateLabel**](../Model/UpdateLabel.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Label**](../Model/Label.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postLabels()`

```php
postLabels($create_label): \OpenAPI\Client\Model\Label
```

Create a new Label

Creates a new Label in the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_label = new \OpenAPI\Client\Model\CreateLabel(); // \OpenAPI\Client\Model\CreateLabel

try {
    $result = $apiInstance->postLabels($create_label);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->postLabels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_label** | [**\OpenAPI\Client\Model\CreateLabel**](../Model/CreateLabel.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Label**](../Model/Label.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `putSignatureRequestsIdLabelsId()`

```php
putSignatureRequestsIdLabelsId($signature_request_id, $label_id)
```

Associate a Label with a Signature Request

Associates a Label with a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LabelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$label_id = 'label_id_example'; // string | Label Id

try {
    $apiInstance->putSignatureRequestsIdLabelsId($signature_request_id, $label_id);
} catch (Exception $e) {
    echo 'Exception when calling LabelApi->putSignatureRequestsIdLabelsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **label_id** | **string**| Label Id | |

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
