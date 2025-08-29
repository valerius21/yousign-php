# OpenAPI\Client\ProofOfAddressVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsProofsOfAddress()**](ProofOfAddressVerificationApi.md#getVerificationsProofsOfAddress) | **GET** /verifications/proofs_of_address | List Proof of Address Verifications |
| [**getVerificationsProofsOfAddressId()**](ProofOfAddressVerificationApi.md#getVerificationsProofsOfAddressId) | **GET** /verifications/proofs_of_address/{proofOfAddressVerificationId} | Retrieve a Proof of Address Verification |
| [**postVerificationsProofsOfAddress()**](ProofOfAddressVerificationApi.md#postVerificationsProofsOfAddress) | **POST** /verifications/proofs_of_address | Initiate a new Proof of Address Verification |


## `getVerificationsProofsOfAddress()`

```php
getVerificationsProofsOfAddress($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsProofsOfAddress200Response
```

List Proof of Address Verifications

Returns the list of all Proof of Address Verifications within your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProofOfAddressVerificationApi(
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
    $result = $apiInstance->getVerificationsProofsOfAddress($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProofOfAddressVerificationApi->getVerificationsProofsOfAddress: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GetVerificationsProofsOfAddress200Response**](../Model/GetVerificationsProofsOfAddress200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsProofsOfAddressId()`

```php
getVerificationsProofsOfAddressId($proof_of_address_verification_id): \OpenAPI\Client\Model\ProofOfAddressFull
```

Retrieve a Proof of Address Verification

Get the detailed results of a Proof of Address Verification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProofOfAddressVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$proof_of_address_verification_id = 'proof_of_address_verification_id_example'; // string | Proof of Address Verification Id

try {
    $result = $apiInstance->getVerificationsProofsOfAddressId($proof_of_address_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProofOfAddressVerificationApi->getVerificationsProofsOfAddressId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proof_of_address_verification_id** | **string**| Proof of Address Verification Id | |

### Return type

[**\OpenAPI\Client\Model\ProofOfAddressFull**](../Model/ProofOfAddressFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsProofsOfAddress()`

```php
postVerificationsProofsOfAddress($file, $natural_person, $workspace_id): \OpenAPI\Client\Model\ProofOfAddressFull
```

Initiate a new Proof of Address Verification

Ask for a Proof of Address Verification by sending a supported document type (see our guide for more info).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProofOfAddressVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | The proof of address document. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx.
$natural_person = new \OpenAPI\Client\Model\InitiateProofOfAddressNaturalPerson(); // \OpenAPI\Client\Model\InitiateProofOfAddressNaturalPerson
$workspace_id = 'workspace_id_example'; // string | Scopes the verification to a specific workspace. Defaults to the default workspace if not specified.

try {
    $result = $apiInstance->postVerificationsProofsOfAddress($file, $natural_person, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProofOfAddressVerificationApi->postVerificationsProofsOfAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| The proof of address document. Accepted formats: PNG, JPEG, JPG, PDF. Max size: 10 MB. Max resolution: 20 mpx. | |
| **natural_person** | [**\OpenAPI\Client\Model\InitiateProofOfAddressNaturalPerson**](../Model/InitiateProofOfAddressNaturalPerson.md)|  | [optional] |
| **workspace_id** | **string**| Scopes the verification to a specific workspace. Defaults to the default workspace if not specified. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProofOfAddressFull**](../Model/ProofOfAddressFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
