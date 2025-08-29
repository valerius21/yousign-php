# OpenAPI\Client\FollowerApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getSignatureRequestsSignatureRequestIdFollowers()**](FollowerApi.md#getSignatureRequestsSignatureRequestIdFollowers) | **GET** /signature_requests/{signatureRequestId}/followers | List the Signature Request&#39;s Followers |
| [**postSignatureRequestsSignatureRequestIdFollowers()**](FollowerApi.md#postSignatureRequestsSignatureRequestIdFollowers) | **POST** /signature_requests/{signatureRequestId}/followers | Create new Followers |


## `getSignatureRequestsSignatureRequestIdFollowers()`

```php
getSignatureRequestsSignatureRequestIdFollowers($signature_request_id): \OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdFollowers200Response
```

List the Signature Request's Followers

Returns a list of Followers for a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FollowerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id

try {
    $result = $apiInstance->getSignatureRequestsSignatureRequestIdFollowers($signature_request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FollowerApi->getSignatureRequestsSignatureRequestIdFollowers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |

### Return type

[**\OpenAPI\Client\Model\GetSignatureRequestsSignatureRequestIdFollowers200Response**](../Model/GetSignatureRequestsSignatureRequestIdFollowers200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSignatureRequestsSignatureRequestIdFollowers()`

```php
postSignatureRequestsSignatureRequestIdFollowers($signature_request_id, $create_followers_inner): \OpenAPI\Client\Model\Follower[]
```

Create new Followers

Adds a Follower to a given Signature Request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FollowerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$create_followers_inner = array(new \OpenAPI\Client\Model\CreateFollowersInner()); // \OpenAPI\Client\Model\CreateFollowersInner[]

try {
    $result = $apiInstance->postSignatureRequestsSignatureRequestIdFollowers($signature_request_id, $create_followers_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FollowerApi->postSignatureRequestsSignatureRequestIdFollowers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **signature_request_id** | **string**| Signature Request Id | |
| **create_followers_inner** | [**\OpenAPI\Client\Model\CreateFollowersInner[]**](../Model/CreateFollowersInner.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Follower[]**](../Model/Follower.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
