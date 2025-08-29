# OpenAPI\Client\IdentityVideoVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsIdentityVideos()**](IdentityVideoVerificationApi.md#getVerificationsIdentityVideos) | **GET** /verifications/identity_videos | List Identity Videos |
| [**getVerificationsIdentityVideosId()**](IdentityVideoVerificationApi.md#getVerificationsIdentityVideosId) | **GET** /verifications/identity_videos/{identityVideoVerificationId} | Retrieve an Identity Video |
| [**postVerificationsIdentityVideos()**](IdentityVideoVerificationApi.md#postVerificationsIdentityVideos) | **POST** /verifications/identity_videos | Initiate a new Identity Video |


## `getVerificationsIdentityVideos()`

```php
getVerificationsIdentityVideos($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsIdentityVideos200Response
```

List Identity Videos

Returns the list of all Identity Videos within your organization. You can limit the number of items returned by using filters and pagination. Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IdentityVideoVerificationApi(
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
    $result = $apiInstance->getVerificationsIdentityVideos($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityVideoVerificationApi->getVerificationsIdentityVideos: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GetVerificationsIdentityVideos200Response**](../Model/GetVerificationsIdentityVideos200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsIdentityVideosId()`

```php
getVerificationsIdentityVideosId($identity_video_verification_id): \OpenAPI\Client\Model\IdentityVideoFull
```

Retrieve an Identity Video

Get the detailed results of an Identity Video Verification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IdentityVideoVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identity_video_verification_id = 'identity_video_verification_id_example'; // string | Identity Video Verification Id

try {
    $result = $apiInstance->getVerificationsIdentityVideosId($identity_video_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityVideoVerificationApi->getVerificationsIdentityVideosId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identity_video_verification_id** | **string**| Identity Video Verification Id | |

### Return type

[**\OpenAPI\Client\Model\IdentityVideoFull**](../Model/IdentityVideoFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsIdentityVideos()`

```php
postVerificationsIdentityVideos($initiate_identity_video): \OpenAPI\Client\Model\IdentityVideoFull
```

Initiate a new Identity Video

Request verification of a person's identity by recording their documents and/or themselves.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IdentityVideoVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$initiate_identity_video = new \OpenAPI\Client\Model\InitiateIdentityVideo(); // \OpenAPI\Client\Model\InitiateIdentityVideo

try {
    $result = $apiInstance->postVerificationsIdentityVideos($initiate_identity_video);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityVideoVerificationApi->postVerificationsIdentityVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **initiate_identity_video** | [**\OpenAPI\Client\Model\InitiateIdentityVideo**](../Model/InitiateIdentityVideo.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\IdentityVideoFull**](../Model/IdentityVideoFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
