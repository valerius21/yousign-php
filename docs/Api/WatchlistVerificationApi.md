# OpenAPI\Client\WatchlistVerificationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVerificationsWatchlists()**](WatchlistVerificationApi.md#getVerificationsWatchlists) | **GET** /verifications/watchlists | List Watchlist Verifications |
| [**getVerificationsWatchlistsId()**](WatchlistVerificationApi.md#getVerificationsWatchlistsId) | **GET** /verifications/watchlists/{watchlistVerificationId} | Retrieve a Watchlist Verification |
| [**postVerificationsWatchlists()**](WatchlistVerificationApi.md#postVerificationsWatchlists) | **POST** /verifications/watchlists | Initiate a Watchlist Verification |


## `getVerificationsWatchlists()`

```php
getVerificationsWatchlists($after, $limit, $status, $workspace_id): \OpenAPI\Client\Model\GetVerificationsWatchlists200Response
```

List Watchlist Verifications

Returns the list of all Watchlist Verifications within your organization.  You can limit the number of items returned by using filters and pagination.  Consult our guide for more details and examples.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WatchlistVerificationApi(
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
    $result = $apiInstance->getVerificationsWatchlists($after, $limit, $status, $workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WatchlistVerificationApi->getVerificationsWatchlists: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GetVerificationsWatchlists200Response**](../Model/GetVerificationsWatchlists200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVerificationsWatchlistsId()`

```php
getVerificationsWatchlistsId($watchlist_verification_id): \OpenAPI\Client\Model\WatchlistFull
```

Retrieve a Watchlist Verification

Retrieve a specific Watchlist Verification by its ID. Returns details about sanctions and politically exposed person status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WatchlistVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$watchlist_verification_id = 'watchlist_verification_id_example'; // string | Watchlist Verification Id

try {
    $result = $apiInstance->getVerificationsWatchlistsId($watchlist_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WatchlistVerificationApi->getVerificationsWatchlistsId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **watchlist_verification_id** | **string**| Watchlist Verification Id | |

### Return type

[**\OpenAPI\Client\Model\WatchlistFull**](../Model/WatchlistFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postVerificationsWatchlists()`

```php
postVerificationsWatchlists($initiate_watchlist): \OpenAPI\Client\Model\WatchlistFull
```

Initiate a Watchlist Verification

Initiate a verification to check if a person appears on international sanctions lists or as a politically exposed person (PEP).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WatchlistVerificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$initiate_watchlist = new \OpenAPI\Client\Model\InitiateWatchlist(); // \OpenAPI\Client\Model\InitiateWatchlist

try {
    $result = $apiInstance->postVerificationsWatchlists($initiate_watchlist);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WatchlistVerificationApi->postVerificationsWatchlists: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **initiate_watchlist** | [**\OpenAPI\Client\Model\InitiateWatchlist**](../Model/InitiateWatchlist.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WatchlistFull**](../Model/WatchlistFull.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
