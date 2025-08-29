# OpenAPI\Client\CompanyVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsCompanies()**](CompanyVerificationApi.md#getVerificationsCompanies) | **GET** /verifications/companies | List Company Verifications |
| [**getVerificationsCompaniesId()**](CompanyVerificationApi.md#getVerificationsCompaniesId) | **GET** /verifications/companies/{companyVerificationId} | Retrieve a Company Verification |
| [**postVerificationsCompanies()**](CompanyVerificationApi.md#postVerificationsCompanies) | **POST** /verifications/companies | Initiate a new Company Verification |


## `getVerificationsCompanies()`

```php
getVerificationsCompanies($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsCompanies200Response
```

List Company Verifications

Returns the list of all Company Verifications within your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CompanyVerificationApi(
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
    $result = $apiInstance->getVerificationsCompanies($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompanyVerificationApi->getVerificationsCompanies: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GetVerificationsCompanies200Response**](../Model/GetVerificationsCompanies200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsCompaniesId()`

```php
getVerificationsCompaniesId($company_verification_id): \OpenAPI\Client\Model\CompanyFull
```

Retrieve a Company Verification

Get the detailed results of a Company Verification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CompanyVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$company_verification_id = 'company_verification_id_example'; // string | Company Verification Id

try {
    $result = $apiInstance->getVerificationsCompaniesId($company_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompanyVerificationApi->getVerificationsCompaniesId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **company_verification_id** | **string**| Company Verification Id | |

### Return type

[**\OpenAPI\Client\Model\CompanyFull**](../Model/CompanyFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsCompanies()`

```php
postVerificationsCompanies($initiate_company_from_json): \OpenAPI\Client\Model\CompanyFull
```

Initiate a new Company Verification

Initiate a new Company Verification

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CompanyVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$initiate_company_from_json = {"company_number":"794513986","country_code":"FR","workspace_id":"9a93d3b5-fb3b-4abf-9e70-26315b33506c"}; // \OpenAPI\Client\Model\InitiateCompanyFromJson

try {
    $result = $apiInstance->postVerificationsCompanies($initiate_company_from_json);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompanyVerificationApi->postVerificationsCompanies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **initiate_company_from_json** | [**\OpenAPI\Client\Model\InitiateCompanyFromJson**](../Model/InitiateCompanyFromJson.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CompanyFull**](../Model/CompanyFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
