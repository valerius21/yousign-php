# OpenAPI\Client\ApproverApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSignatureRequestsSignatureRequestIdApproversApproverId()**](ApproverApi.md#deleteSignatureRequestsSignatureRequestIdApproversApproverId) | **DELETE** /signature_requests/{signatureRequestId}/approvers/{approverId} | Delete an Approver |
| [**getSignatureRequestsSignatureRequestIdApproversApproverId()**](ApproverApi.md#getSignatureRequestsSignatureRequestIdApproversApproverId) | **GET** /signature_requests/{signatureRequestId}/approvers/{approverId} | Get an Approver |
| [**patchSignatureRequestsSignatureRequestIdApproversApproverId()**](ApproverApi.md#patchSignatureRequestsSignatureRequestIdApproversApproverId) | **PATCH** /signature_requests/{signatureRequestId}/approvers/{approverId} | Update an Approver |
| [**postSignatureRequestsSignatureRequestIdApprovers()**](ApproverApi.md#postSignatureRequestsSignatureRequestIdApprovers) | **POST** /signature_requests/{signatureRequestId}/approvers | Create a new Approver |
| [**postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder()**](ApproverApi.md#postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder) | **POST** /signature_requests/{signatureRequestId}/approvers/{approverId}/send_reminder | Send manual reminder to an Approver |


## `deleteSignatureRequestsSignatureRequestIdApproversApproverId()`

```php
deleteSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id)
```

Delete an Approver

Deletes a given Approver from a Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApproverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$approver_id = 'approver_id_example'; // string | Approver Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id);
} catch (Exception $e) {
    echo 'Exception when calling ApproverApi->deleteSignatureRequestsSignatureRequestIdApproversApproverId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **approver_id** | **string**| Approver Id | |

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

## `getSignatureRequestsSignatureRequestIdApproversApproverId()`

```php
getSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id): \OpenAPI\Client\Model\Approver
```

Get an Approver

Retrieves a given Approver.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApproverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$approver_id = 'approver_id_example'; // string | Approver Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApproverApi->getSignatureRequestsSignatureRequestIdApproversApproverId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **approver_id** | **string**| Approver Id | |

### Return type

[**\OpenAPI\Client\Model\Approver**](../Model/Approver.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchSignatureRequestsSignatureRequestIdApproversApproverId()`

```php
patchSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id, $update_approver): \OpenAPI\Client\Model\Approver
```

Update an Approver

Updates a given Approver. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApproverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$approver_id = 'approver_id_example'; // string | Approver Id
$update_approver = new \OpenAPI\Client\Model\UpdateApprover(); // \OpenAPI\Client\Model\UpdateApprover

try {
    $result = $apiInstance->patchSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id, $update_approver);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApproverApi->patchSignatureRequestsSignatureRequestIdApproversApproverId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **approver_id** | **string**| Approver Id | |
| **update_approver** | [**\OpenAPI\Client\Model\UpdateApprover**](../Model/UpdateApprover.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Approver**](../Model/Approver.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdApprovers()`

```php
postSignatureRequestsSignatureRequestIdApprovers($signature_request_id, $create_approver): \OpenAPI\Client\Model\Approver
```

Create a new Approver

Adds an Approver to a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApproverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$create_approver = new \OpenAPI\Client\Model\CreateApprover(); // \OpenAPI\Client\Model\CreateApprover | An Approver object to be added to the Signature Request.

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdApprovers($signature_request_id, $create_approver);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApproverApi->postSignatureRequestsSignatureRequestIdApprovers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **create_approver** | [**\OpenAPI\Client\Model\CreateApprover**](../Model/CreateApprover.md)| An Approver object to be added to the Signature Request. | [optional] |

### Return type

[**\OpenAPI\Client\Model\Approver**](../Model/Approver.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder()`

```php
postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder($signature_request_id, $approver_id)
```

Send manual reminder to an Approver

Sends a reminder to a given Approver to review their Signature Request. Only possible when the Signature Request status is `approval` and the Approver status is `notified`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApproverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$approver_id = 'approver_id_example'; // string | Approver Id

try {
    $apiInstance->postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder($signature_request_id, $approver_id);
} catch (Exception $e) {
    echo 'Exception when calling ApproverApi->postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **approver_id** | **string**| Approver Id | |

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
