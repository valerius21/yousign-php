# OpenAPI\Client\BankAccountVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsBankAccounts()**](BankAccountVerificationApi.md#getVerificationsBankAccounts) | **GET** /verifications/bank_accounts | List Bank Account Verifications |
| [**getVerificationsBankAccountsId()**](BankAccountVerificationApi.md#getVerificationsBankAccountsId) | **GET** /verifications/bank_accounts/{bankAccountVerificationId} | Retrieve a Bank Account Verification |
| [**postVerificationsBankAccounts()**](BankAccountVerificationApi.md#postVerificationsBankAccounts) | **POST** /verifications/bank_accounts | Initiate a new Bank Account Verification |


## `getVerificationsBankAccounts()`

```php
getVerificationsBankAccounts($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsBankAccounts200Response
```

List Bank Account Verifications

Returns the list of all Bank Account Verifications within your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountVerificationApi(
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
    $result = $apiInstance->getVerificationsBankAccounts($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountVerificationApi->getVerificationsBankAccounts: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GetVerificationsBankAccounts200Response**](../Model/GetVerificationsBankAccounts200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsBankAccountsId()`

```php
getVerificationsBankAccountsId($bank_account_verification_id): \OpenAPI\Client\Model\BankAccountFull
```

Retrieve a Bank Account Verification

Get the detailed results of a Bank Account Verification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bank_account_verification_id = 'bank_account_verification_id_example'; // string | Bank Account Verification Id

try {
    $result = $apiInstance->getVerificationsBankAccountsId($bank_account_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountVerificationApi->getVerificationsBankAccountsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bank_account_verification_id** | **string**| Bank Account Verification Id | |

### Return type

[**\OpenAPI\Client\Model\BankAccountFull**](../Model/BankAccountFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsBankAccounts()`

```php
postVerificationsBankAccounts($file, $iban, $bic, $workspace_id, $legal_person, $natural_person): \OpenAPI\Client\Model\BankAccountFull
```

Initiate a new Bank Account Verification

Ask for a Bank Account Verification by sending the file containing the bank account details, such as IBAN and BIC.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankAccountVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | The file containing the bank account details. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx.
$iban = 'iban_example'; // string | International Bank Account Number (IBAN)
$bic = 'bic_example'; // string | Business Identifier Codes (BIC)
$workspace_id = 'workspace_id_example'; // string | Scopes the verification to a specific workspace. Defaults to the default workspace if not specified.
$legal_person = new \OpenAPI\Client\Model\InitiateBankAccountWithLegalPersonLegalPerson(); // \OpenAPI\Client\Model\InitiateBankAccountWithLegalPersonLegalPerson
$natural_person = new \OpenAPI\Client\Model\InitiateBankAccountWithNaturalPersonNaturalPerson(); // \OpenAPI\Client\Model\InitiateBankAccountWithNaturalPersonNaturalPerson

try {
    $result = $apiInstance->postVerificationsBankAccounts($file, $iban, $bic, $workspace_id, $legal_person, $natural_person);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountVerificationApi->postVerificationsBankAccounts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| The file containing the bank account details. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx. | [optional] |
| **iban** | **string**| International Bank Account Number (IBAN) | [optional] |
| **bic** | **string**| Business Identifier Codes (BIC) | [optional] |
| **workspace_id** | **string**| Scopes the verification to a specific workspace. Defaults to the default workspace if not specified. | [optional] |
| **legal_person** | [**\OpenAPI\Client\Model\InitiateBankAccountWithLegalPersonLegalPerson**](../Model/InitiateBankAccountWithLegalPersonLegalPerson.md)|  | [optional] |
| **natural_person** | [**\OpenAPI\Client\Model\InitiateBankAccountWithNaturalPersonNaturalPerson**](../Model/InitiateBankAccountWithNaturalPersonNaturalPerson.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BankAccountFull**](../Model/BankAccountFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
