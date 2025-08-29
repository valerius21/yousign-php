# OpenAPI\Client\ConsumptionApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getConsumptionAddon()**](ConsumptionApi.md#getConsumptionAddon) | **GET** /consumptions/addons | Get detailed addon consumption. |
| [**getConsumptionDetail()**](ConsumptionApi.md#getConsumptionDetail) | **GET** /consumptions/detail | Get detailed Consumption data |
| [**getConsumptions()**](ConsumptionApi.md#getConsumptions) | **GET** /consumptions | Get Consumptions |
| [**getConsumptionsExport()**](ConsumptionApi.md#getConsumptionsExport) | **GET** /consumptions/export | Export Consumption data |


## `getConsumptionAddon()`

```php
getConsumptionAddon($addons): \OpenAPI\Client\Model\GetConsumptionAddon200Response
```

Get detailed addon consumption.

Retrieves detailed addon consumption for the current subscription period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ConsumptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$addons = array('addons_example'); // string[] | A list of add-ons to filter the results on.

try {
    $result = $apiInstance->getConsumptionAddon($addons);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsumptionApi->getConsumptionAddon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **addons** | [**string[]**](../Model/string.md)| A list of add-ons to filter the results on. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetConsumptionAddon200Response**](../Model/GetConsumptionAddon200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConsumptionDetail()`

```php
getConsumptionDetail($from, $to, $after, $limit, $breakdown_type, $workspace_ids): \OpenAPI\Client\Model\GetConsumptionDetail200Response
```

Get detailed Consumption data

Returns the consumption of your organization over a specified period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ConsumptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The starting date for data retrieval.
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date for data retrieval. The `to` date must be later than the `from` date and within one year of the `from` date.
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$breakdown_type = 'organization'; // string | Specifies how data is grouped. By default, it returns the total consumption for the entire organization. If set to `workspace`, the data will be grouped by Workspace.
$workspace_ids = array('workspace_ids_example'); // string[] | A list of Workspace IDs to filter the results.

try {
    $result = $apiInstance->getConsumptionDetail($from, $to, $after, $limit, $breakdown_type, $workspace_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsumptionApi->getConsumptionDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**| The starting date for data retrieval. | |
| **to** | **\DateTime**| The end date for data retrieval. The &#x60;to&#x60; date must be later than the &#x60;from&#x60; date and within one year of the &#x60;from&#x60; date. | |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **breakdown_type** | **string**| Specifies how data is grouped. By default, it returns the total consumption for the entire organization. If set to &#x60;workspace&#x60;, the data will be grouped by Workspace. | [optional] [default to &#39;organization&#39;] |
| **workspace_ids** | [**string[]**](../Model/string.md)| A list of Workspace IDs to filter the results. | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetConsumptionDetail200Response**](../Model/GetConsumptionDetail200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConsumptions()`

```php
getConsumptions($from, $to, $authentication_key): \OpenAPI\Client\Model\Consumption
```

Get Consumptions

Get signatures Consumption by source

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ConsumptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The \"from\" date must not be more than 1 year in the past
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The \"to\" date must be more recent than the \"from\" date
$authentication_key = 'authentication_key_example'; // string | The API authentication key to use to retrieve the data

try {
    $result = $apiInstance->getConsumptions($from, $to, $authentication_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsumptionApi->getConsumptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**| The \&quot;from\&quot; date must not be more than 1 year in the past | |
| **to** | **\DateTime**| The \&quot;to\&quot; date must be more recent than the \&quot;from\&quot; date | |
| **authentication_key** | **string**| The API authentication key to use to retrieve the data | [optional] |

### Return type

[**\OpenAPI\Client\Model\Consumption**](../Model/Consumption.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConsumptionsExport()`

```php
getConsumptionsExport($from, $to, $authentication_key): string
```

Export Consumption data

Get a binary .csv file containing all the Consumption data of the underlying signatures

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ConsumptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The \"from\" date must not be more than 1 year in the past
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The \"to\" date must be more recent than the \"from\" date
$authentication_key = 'authentication_key_example'; // string | The API authentication key to use to retrieve the data

try {
    $result = $apiInstance->getConsumptionsExport($from, $to, $authentication_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsumptionApi->getConsumptionsExport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**| The \&quot;from\&quot; date must not be more than 1 year in the past | |
| **to** | **\DateTime**| The \&quot;to\&quot; date must be more recent than the \&quot;from\&quot; date | |
| **authentication_key** | **string**| The API authentication key to use to retrieve the data | [optional] |

### Return type

**string**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/csv`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
