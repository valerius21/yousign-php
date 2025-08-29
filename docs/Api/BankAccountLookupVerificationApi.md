# OpenAPI\Client\BankAccountLookupVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsBankAccountLookups()**](BankAccountLookupVerificationApi.md#getVerificationsBankAccountLookups) | **GET** /verifications/bank_account_lookups | List Bank Account Lookup Verifications |
| [**getVerificationsBankAccountLookupsId()**](BankAccountLookupVerificationApi.md#getVerificationsBankAccountLookupsId) | **GET** /verifications/bank_account_lookups/{bankAccountLookupVerificationId} | Retrieve a Bank Account Lookup Verification |
| [**postVerificationsBankAccountLookups()**](BankAccountLookupVerificationApi.md#postVerificationsBankAccountLookups) | **POST** /verifications/bank_account_lookups | Initiate a new Bank Account Lookup Verification |


## `getVerificationsBankAccountLookups()`

```php
getVerificationsBankAccountLookups($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsBankAccountLookups200Response
```

List Bank Account Lookup Verifications

Returns the list of all Bank Account Lookup Verifications within your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountLookupVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$status = {"eq":["verified"]}; // object | Filter by `status`. Allowed operators: `eq`. Example: `status[eq]=verified`
$workspace_id = {"eq":["9b6ed2f3-244f-487a-baa1-bbe4f51c8748"]}; // object | Filter by `workspace_id`. Allowed operators: `eq`. Example: `workspace_id[eq]=9b6ed2f3-244f-487a-baa1-bbe4f51c8748`

try {
    $result = $apiInstance->getVerificationsBankAccountLookups($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountLookupVerificationApi->getVerificationsBankAccountLookups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **status** | [**object**](../Model/.md)| Filter by &#x60;status&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;status[eq]&#x3D;verified&#x60; | [optional] |
| **workspace_id** | [**object**](../Model/.md)| Filter by &#x60;workspace_id&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;workspace_id[eq]&#x3D;9b6ed2f3-244f-487a-baa1-bbe4f51c8748&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetVerificationsBankAccountLookups200Response**](../Model/GetVerificationsBankAccountLookups200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsBankAccountLookupsId()`

```php
getVerificationsBankAccountLookupsId($bank_account_lookup_verification_id): \OpenAPI\Client\Model\BankAccountLookupMeta
```

Retrieve a Bank Account Lookup Verification

Retrieve a specific Bank Account Lookup Verification by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountLookupVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bank_account_lookup_verification_id = 'bank_account_lookup_verification_id_example'; // string | Bank Account Lookup Verification Id

try {
    $result = $apiInstance->getVerificationsBankAccountLookupsId($bank_account_lookup_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountLookupVerificationApi->getVerificationsBankAccountLookupsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bank_account_lookup_verification_id** | **string**| Bank Account Lookup Verification Id | |

### Return type

[**\OpenAPI\Client\Model\BankAccountLookupMeta**](../Model/BankAccountLookupMeta.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsBankAccountLookups()`

```php
postVerificationsBankAccountLookups($post_verifications_bank_account_lookups_request): \OpenAPI\Client\Model\BankAccountLookupMeta
```

Initiate a new Bank Account Lookup Verification

Initiate a new Bank Account Lookup Verification to check if a bank account exists and belongs to the specified person or company.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountLookupVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_verifications_bank_account_lookups_request = new \OpenAPI\Client\Model\PostVerificationsBankAccountLookupsRequest(); // \OpenAPI\Client\Model\PostVerificationsBankAccountLookupsRequest

try {
    $result = $apiInstance->postVerificationsBankAccountLookups($post_verifications_bank_account_lookups_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountLookupVerificationApi->postVerificationsBankAccountLookups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_verifications_bank_account_lookups_request** | [**\OpenAPI\Client\Model\PostVerificationsBankAccountLookupsRequest**](../Model/PostVerificationsBankAccountLookupsRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BankAccountLookupMeta**](../Model/BankAccountLookupMeta.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
