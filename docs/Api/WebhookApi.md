# OpenAPI\Client\WebhookApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteWebhooksWebhookId()**](WebhookApi.md#deleteWebhooksWebhookId) | **DELETE** /webhooks/{webhookId} | Delete a Webhook subscription |
| [**getWebhooks()**](WebhookApi.md#getWebhooks) | **GET** /webhooks | List Webhook subscriptions |
| [**getWebhooksWebhookId()**](WebhookApi.md#getWebhooksWebhookId) | **GET** /webhooks/{webhookId} | Get a Webhook subscription |
| [**patchWebhooksWebhookId()**](WebhookApi.md#patchWebhooksWebhookId) | **PATCH** /webhooks/{webhookId} | Update a Webhook subscription |
| [**postWebhooksSubscriptions()**](WebhookApi.md#postWebhooksSubscriptions) | **POST** /webhooks | Create a Webhook subscription |


## `deleteWebhooksWebhookId()`

```php
deleteWebhooksWebhookId($webhook_id)
```

Delete a Webhook subscription

Deletes a given Webhook subscription.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_id = 'webhook_id_example'; // string | Webhook Id

try {
    $apiInstance->deleteWebhooksWebhookId($webhook_id);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->deleteWebhooksWebhookId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_id** | **string**| Webhook Id | |

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

## `getWebhooks()`

```php
getWebhooks(): \OpenAPI\Client\Model\WebhookSubscription[]
```

List Webhook subscriptions

Returns the list of all Webhook subscriptions in your Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getWebhooks();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->getWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\WebhookSubscription[]**](../Model/WebhookSubscription.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebhooksWebhookId()`

```php
getWebhooksWebhookId($webhook_id): \OpenAPI\Client\Model\WebhookSubscription
```

Get a Webhook subscription

Retrieves a given Webhook subscription.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_id = 'webhook_id_example'; // string | Webhook Id

try {
    $result = $apiInstance->getWebhooksWebhookId($webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->getWebhooksWebhookId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_id** | **string**| Webhook Id | |

### Return type

[**\OpenAPI\Client\Model\WebhookSubscription**](../Model/WebhookSubscription.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchWebhooksWebhookId()`

```php
patchWebhooksWebhookId($webhook_id, $update_webhook_subscription): \OpenAPI\Client\Model\WebhookSubscription
```

Update a Webhook subscription

Updates a given Webhook subscription. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_id = 'webhook_id_example'; // string | Webhook Id
$update_webhook_subscription = new \OpenAPI\Client\Model\UpdateWebhookSubscription(); // \OpenAPI\Client\Model\UpdateWebhookSubscription

try {
    $result = $apiInstance->patchWebhooksWebhookId($webhook_id, $update_webhook_subscription);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->patchWebhooksWebhookId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_id** | **string**| Webhook Id | |
| **update_webhook_subscription** | [**\OpenAPI\Client\Model\UpdateWebhookSubscription**](../Model/UpdateWebhookSubscription.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WebhookSubscription**](../Model/WebhookSubscription.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postWebhooksSubscriptions()`

```php
postWebhooksSubscriptions($create_webhook_subscription): \OpenAPI\Client\Model\WebhookSubscription
```

Create a Webhook subscription

Creates a new Webhook subscription in your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_webhook_subscription = new \OpenAPI\Client\Model\CreateWebhookSubscription(); // \OpenAPI\Client\Model\CreateWebhookSubscription

try {
    $result = $apiInstance->postWebhooksSubscriptions($create_webhook_subscription);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->postWebhooksSubscriptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_webhook_subscription** | [**\OpenAPI\Client\Model\CreateWebhookSubscription**](../Model/CreateWebhookSubscription.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WebhookSubscription**](../Model/WebhookSubscription.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
