# OpenAPI\Client\BankAccountConnectionVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsBankAccountConnections()**](BankAccountConnectionVerificationApi.md#getVerificationsBankAccountConnections) | **GET** /verifications/bank_account_connections | List Bank Account Connection Verifications |
| [**getVerificationsBankAccountConnectionsId()**](BankAccountConnectionVerificationApi.md#getVerificationsBankAccountConnectionsId) | **GET** /verifications/bank_account_connections/{verificationId} | Retrieve a Bank Account Connection Verification |
| [**postVerificationsBankAccountConnections()**](BankAccountConnectionVerificationApi.md#postVerificationsBankAccountConnections) | **POST** /verifications/bank_account_connections | Initiate a new Bank Account Connection |


## `getVerificationsBankAccountConnections()`

```php
getVerificationsBankAccountConnections($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsBankAccountConnections200Response
```

List Bank Account Connection Verifications

Returns the list of all Bank Account Connection Verifications within your organization. You can limit the number of items returned by using filters and pagination.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountConnectionVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$status = {"eq":"verified"}; // object | Filter by `status`. Allowed operators: `eq`, `in`. Example: `status[eq]=verified` or `status[in]=verified,failed`
$workspace_id = {"eq":"9b6ed2f3-244f-487a-baa1-bbe4f51c8748"}; // object | Filter by `workspace_id`. Allowed operators: `eq`. Example: `workspace_id[eq]=9b6ed2f3-244f-487a-baa1-bbe4f51c8748`

try {
    $result = $apiInstance->getVerificationsBankAccountConnections($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountConnectionVerificationApi->getVerificationsBankAccountConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **status** | [**object**](../Model/.md)| Filter by &#x60;status&#x60;. Allowed operators: &#x60;eq&#x60;, &#x60;in&#x60;. Example: &#x60;status[eq]&#x3D;verified&#x60; or &#x60;status[in]&#x3D;verified,failed&#x60; | [optional] |
| **workspace_id** | [**object**](../Model/.md)| Filter by &#x60;workspace_id&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;workspace_id[eq]&#x3D;9b6ed2f3-244f-487a-baa1-bbe4f51c8748&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetVerificationsBankAccountConnections200Response**](../Model/GetVerificationsBankAccountConnections200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsBankAccountConnectionsId()`

```php
getVerificationsBankAccountConnectionsId($verification_id): \OpenAPI\Client\Model\BankAccountConnectionFull
```

Retrieve a Bank Account Connection Verification

Get the detailed results of a Bank Account Connection Verification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountConnectionVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$verification_id = 'verification_id_example'; // string | Bank Account Connection Verification Id

try {
    $result = $apiInstance->getVerificationsBankAccountConnectionsId($verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountConnectionVerificationApi->getVerificationsBankAccountConnectionsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **verification_id** | **string**| Bank Account Connection Verification Id | |

### Return type

[**\OpenAPI\Client\Model\BankAccountConnectionFull**](../Model/BankAccountConnectionFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsBankAccountConnections()`

```php
postVerificationsBankAccountConnections($post_verifications_bank_account_connections_request): \OpenAPI\Client\Model\BankAccountConnectionFull
```

Initiate a new Bank Account Connection

Initiate a new Bank Account Connection resource

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountConnectionVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_verifications_bank_account_connections_request = new \OpenAPI\Client\Model\PostVerificationsBankAccountConnectionsRequest(); // \OpenAPI\Client\Model\PostVerificationsBankAccountConnectionsRequest

try {
    $result = $apiInstance->postVerificationsBankAccountConnections($post_verifications_bank_account_connections_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountConnectionVerificationApi->postVerificationsBankAccountConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_verifications_bank_account_connections_request** | [**\OpenAPI\Client\Model\PostVerificationsBankAccountConnectionsRequest**](../Model/PostVerificationsBankAccountConnectionsRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BankAccountConnectionFull**](../Model/BankAccountConnectionFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
