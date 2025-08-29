# OpenAPI\Client\SignatureRequestApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSignatureRequestsSignatureRequestId()**](SignatureRequestApi.md#deleteSignatureRequestsSignatureRequestId) | **DELETE** /signature_requests/{signatureRequestId} | Delete a Signature Request |
| [**getSignatureRequests()**](SignatureRequestApi.md#getSignatureRequests) | **GET** /signature_requests | List Signature Requests |
| [**getSignatureRequestsSignatureRequestId()**](SignatureRequestApi.md#getSignatureRequestsSignatureRequestId) | **GET** /signature_requests/{signatureRequestId} | Fetch a Signature Request |
| [**patchSignatureRequestsSignatureRequestId()**](SignatureRequestApi.md#patchSignatureRequestsSignatureRequestId) | **PATCH** /signature_requests/{signatureRequestId} | Update a Signature Request |
| [**postSignatureRequests()**](SignatureRequestApi.md#postSignatureRequests) | **POST** /signature_requests | Initiate a new Signature Request |
| [**postSignatureRequestsSignatureRequestIdActivate()**](SignatureRequestApi.md#postSignatureRequestsSignatureRequestIdActivate) | **POST** /signature_requests/{signatureRequestId}/activate | Activate a Signature Request |
| [**postSignatureRequestsSignatureRequestIdCancel()**](SignatureRequestApi.md#postSignatureRequestsSignatureRequestIdCancel) | **POST** /signature_requests/{signatureRequestId}/cancel | Cancel a Signature Request |
| [**postSignatureRequestsSignatureRequestIdReactivate()**](SignatureRequestApi.md#postSignatureRequestsSignatureRequestIdReactivate) | **POST** /signature_requests/{signatureRequestId}/reactivate | Reactivate an expired Signature Request |


## `deleteSignatureRequestsSignatureRequestId()`

```php
deleteSignatureRequestsSignatureRequestId($signature_request_id, $permanent_delete)
```

Delete a Signature Request

Deletes a given Signature Request, not possible if the Signature Request is in `approval` and `ongoing` status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$permanent_delete = false; // bool | If true it will permanently delete the Signature Request. It will no longer be retrievable.

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestId($signature_request_id, $permanent_delete);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->deleteSignatureRequestsSignatureRequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **permanent_delete** | **bool**| If true it will permanently delete the Signature Request. It will no longer be retrievable. | [optional] [default to false] |

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

## `getSignatureRequests()`

```php
getSignatureRequests($after, $limit, $status, $created_at, $workspace_id, $external_id, $source, $q, $label_name): \OpenAPI\Client\Model\GetSignatureRequests200Response
```

List Signature Requests

Returns the list of all Signatures Requests in your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$status = {"eq":["draft"],"in":["draft","done"]}; // object | Filter by `status`. Allowed operators: `eq`, `in`. Example: `status[in]=draft,done`
$created_at = {"between":["2025-03-02","2025-03-04"],"before":["2025-03-02"]}; // object | Filter by `created_at`. Allowed operators: `eq`, `between`, `before`, `after`. Format: the date format required is `yyyy-mm-dd` Example: `created_at[between]=2025-03-02,2025-03-04`
$workspace_id = {"eq":["9b6ed2f3-244f-487a-baa1-bbe4f51c8748"]}; // object | Filter by `workspace_id`. Allowed operators: `eq`. Example: `workspace_id[eq]=9b6ed2f3-244f-487a-baa1-bbe4f51c8748`
$external_id = {"eq":["an-external-id"]}; // object | Filter by `external_id`. Allowed operators: `eq`. Example: `external_id[eq]=an-external-id`
$source = {"eq":["public_api"],"in":["public_api","app"]}; // object | Filter by `source`. Allowed operators: `eq`, `in`. Example: `source[in]=public_api,app`
$q = 'q_example'; // string | Search on name
$label_name = {"eq":["To Sign"],"in":["To Sign","Miscellaneous"]}; // object | Filter by Label's `name`. Allowed operators: `eq`, `in`. Example: `label.name[in]=To Sign,Miscellaneous`

try {
    $result = $apiInstance->getSignatureRequests($after, $limit, $status, $created_at, $workspace_id, $external_id, $source, $q, $label_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->getSignatureRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **status** | [**object**](../Model/.md)| Filter by &#x60;status&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;in&#x60;. Example: &#x60;status[in]&#x3D;draft,done&#x60; | [optional] |
| **created_at** | [**object**](../Model/.md)| Filter by &#x60;created_at&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;between&#x60;, &#x60;before&#x60;, &#x60;after&#x60;. Format: the date format required is &#x60;yyyy-mm-dd&#x60; Example: &#x60;created_at[between]&#x3D;2025-03-02,2025-03-04&#x60; | [optional] |
| **workspace_id** | [**object**](../Model/.md)| Filter by &#x60;workspace_id&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;workspace_id[eq]&#x3D;9b6ed2f3-244f-487a-baa1-bbe4f51c8748&#x60; | [optional] |
| **external_id** | [**object**](../Model/.md)| Filter by &#x60;external_id&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;external_id[eq]&#x3D;an-external-id&#x60; | [optional] |
| **source** | [**object**](../Model/.md)| Filter by &#x60;source&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;in&#x60;. Example: &#x60;source[in]&#x3D;public_api,app&#x60; | [optional] |
| **q** | **string**| Search on name | [optional] |
| **label_name** | [**object**](../Model/.md)| Filter by Label&#39;s &#x60;name&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;in&#x60;. Example: &#x60;label.name[in]&#x3D;To Sign,Miscellaneous&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequests200Response**](../Model/GetSignatureRequests200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSignatureRequestsSignatureRequestId()`

```php
getSignatureRequestsSignatureRequestId($signature_request_id): \OpenAPI\Client\Model\SignatureRequest
```

Fetch a Signature Request

Retrieves a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestId($signature_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->getSignatureRequestsSignatureRequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

### Return type

[**\OpenAPI\Client\Model\SignatureRequest**](../Model/SignatureRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchSignatureRequestsSignatureRequestId()`

```php
patchSignatureRequestsSignatureRequestId($signature_request_id, $update_signature_request): \OpenAPI\Client\Model\SignatureRequest
```

Update a Signature Request

Updates a given Signature Request. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$update_signature_request = new \OpenAPI\Client\Model\UpdateSignatureRequest(); // \OpenAPI\Client\Model\UpdateSignatureRequest

try {
    $result = $apiInstance->patchSignatureRequestsSignatureRequestId($signature_request_id, $update_signature_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->patchSignatureRequestsSignatureRequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **update_signature_request** | [**\OpenAPI\Client\Model\UpdateSignatureRequest**](../Model/UpdateSignatureRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignatureRequest**](../Model/SignatureRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequests()`

```php
postSignatureRequests($create_signature_request): \OpenAPI\Client\Model\SignatureRequest
```

Initiate a new Signature Request

Creates a new Signature Request resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_signature_request = new \OpenAPI\Client\Model\CreateSignatureRequest(); // \OpenAPI\Client\Model\CreateSignatureRequest

try {
    $result = $apiInstance->postSignatureRequests($create_signature_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->postSignatureRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_signature_request** | [**\OpenAPI\Client\Model\CreateSignatureRequest**](../Model/CreateSignatureRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignatureRequest**](../Model/SignatureRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdActivate()`

```php
postSignatureRequestsSignatureRequestIdActivate($signature_request_id, $activate_signature_request): \OpenAPI\Client\Model\SignatureRequestActivated
```

Activate a Signature Request

Activates a Signature request, so it is not in `draft` status anymore. If the `delivery_mode` is not `null`, activating the Signature Request will trigger the notifications to Approvers/Followers/Signers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$activate_signature_request = new \OpenAPI\Client\Model\ActivateSignatureRequest(); // \OpenAPI\Client\Model\ActivateSignatureRequest

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdActivate($signature_request_id, $activate_signature_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->postSignatureRequestsSignatureRequestIdActivate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **activate_signature_request** | [**\OpenAPI\Client\Model\ActivateSignatureRequest**](../Model/ActivateSignatureRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignatureRequestActivated**](../Model/SignatureRequestActivated.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdCancel()`

```php
postSignatureRequestsSignatureRequestIdCancel($signature_request_id, $post_signature_requests_signature_request_id_cancel_request): \OpenAPI\Client\Model\SignatureRequest
```

Cancel a Signature Request

Cancels a Signature Request when it is in `approval` or `ongoing` status. A canceled Signature Request cannot be reactivated.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$post_signature_requests_signature_request_id_cancel_request = new \OpenAPI\Client\Model\PostSignatureRequestsSignatureRequestIdCancelRequest(); // \OpenAPI\Client\Model\PostSignatureRequestsSignatureRequestIdCancelRequest

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdCancel($signature_request_id, $post_signature_requests_signature_request_id_cancel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->postSignatureRequestsSignatureRequestIdCancel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **post_signature_requests_signature_request_id_cancel_request** | [**\OpenAPI\Client\Model\PostSignatureRequestsSignatureRequestIdCancelRequest**](../Model/PostSignatureRequestsSignatureRequestIdCancelRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignatureRequest**](../Model/SignatureRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdReactivate()`

```php
postSignatureRequestsSignatureRequestIdReactivate($signature_request_id, $post_signature_requests_signature_request_id_reactivate_request): \OpenAPI\Client\Model\SignatureRequest
```

Reactivate an expired Signature Request

Reactivates a Signature Request when it is in `expired` status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SignatureRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$post_signature_requests_signature_request_id_reactivate_request = new \OpenAPI\Client\Model\PostSignatureRequestsSignatureRequestIdReactivateRequest(); // \OpenAPI\Client\Model\PostSignatureRequestsSignatureRequestIdReactivateRequest

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdReactivate($signature_request_id, $post_signature_requests_signature_request_id_reactivate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SignatureRequestApi->postSignatureRequestsSignatureRequestIdReactivate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **post_signature_requests_signature_request_id_reactivate_request** | [**\OpenAPI\Client\Model\PostSignatureRequestsSignatureRequestIdReactivateRequest**](../Model/PostSignatureRequestsSignatureRequestIdReactivateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SignatureRequest**](../Model/SignatureRequest.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
