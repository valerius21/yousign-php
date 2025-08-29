# OpenAPI\Client\WorkspaceApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteWorkspace()**](WorkspaceApi.md#deleteWorkspace) | **DELETE** /workspaces/{workspaceId} | Delete a Workspace |
| [**getWorkspaces()**](WorkspaceApi.md#getWorkspaces) | **GET** /workspaces | List Workspaces |
| [**getWorkspacesDefault()**](WorkspaceApi.md#getWorkspacesDefault) | **GET** /workspaces/default | Get the default Workspace |
| [**getWorkspacesWorkspaceId()**](WorkspaceApi.md#getWorkspacesWorkspaceId) | **GET** /workspaces/{workspaceId} | Get a Workspace |
| [**markWorkspaceAsDefault()**](WorkspaceApi.md#markWorkspaceAsDefault) | **POST** /workspaces/default | Mark the given Workspace as default |
| [**patchWorkspacesWorkspaceId()**](WorkspaceApi.md#patchWorkspacesWorkspaceId) | **PATCH** /workspaces/{workspaceId} | Update a Workspace |
| [**postWorkspace()**](WorkspaceApi.md#postWorkspace) | **POST** /workspaces | Create a Workspace |


## `deleteWorkspace()`

```php
deleteWorkspace($workspace_id, $delete_workspace)
```

Delete a Workspace

Deletes a given Workspace and transfers everything that is attached to this Workspace to a another specified Workspace.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string | Workspace Id
$delete_workspace = new \OpenAPI\Client\Model\DeleteWorkspace(); // \OpenAPI\Client\Model\DeleteWorkspace

try {
    $apiInstance->deleteWorkspace($workspace_id, $delete_workspace);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->deleteWorkspace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**| Workspace Id | |
| **delete_workspace** | [**\OpenAPI\Client\Model\DeleteWorkspace**](../Model/DeleteWorkspace.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWorkspaces()`

```php
getWorkspaces($after, $limit): \OpenAPI\Client\Model\GetWorkspaces200Response
```

List Workspaces

Returns the list of all Workspaces within your Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 10; // int | The limit of items count to retrieve.

try {
    $result = $apiInstance->getWorkspaces($after, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->getWorkspaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 10] |

### Return type

[**\OpenAPI\Client\Model\GetWorkspaces200Response**](../Model/GetWorkspaces200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWorkspacesDefault()`

```php
getWorkspacesDefault(): \OpenAPI\Client\Model\Workspace
```

Get the default Workspace

Retrieves the default Workspace.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getWorkspacesDefault();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->getWorkspacesDefault: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Workspace**](../Model/Workspace.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWorkspacesWorkspaceId()`

```php
getWorkspacesWorkspaceId($workspace_id): \OpenAPI\Client\Model\Workspace
```

Get a Workspace

Retrieves a given Workspace.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string | Workspace Id

try {
    $result = $apiInstance->getWorkspacesWorkspaceId($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->getWorkspacesWorkspaceId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**| Workspace Id | |

### Return type

[**\OpenAPI\Client\Model\Workspace**](../Model/Workspace.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markWorkspaceAsDefault()`

```php
markWorkspaceAsDefault($mark_workspace_as_default)
```

Mark the given Workspace as default

Marks the given Workspace as default.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$mark_workspace_as_default = new \OpenAPI\Client\Model\MarkWorkspaceAsDefault(); // \OpenAPI\Client\Model\MarkWorkspaceAsDefault

try {
    $apiInstance->markWorkspaceAsDefault($mark_workspace_as_default);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->markWorkspaceAsDefault: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **mark_workspace_as_default** | [**\OpenAPI\Client\Model\MarkWorkspaceAsDefault**](../Model/MarkWorkspaceAsDefault.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchWorkspacesWorkspaceId()`

```php
patchWorkspacesWorkspaceId($workspace_id, $update_workspace): \OpenAPI\Client\Model\Workspace
```

Update a Workspace

Updates a given Workspace. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string | Workspace Id
$update_workspace = new \OpenAPI\Client\Model\UpdateWorkspace(); // \OpenAPI\Client\Model\UpdateWorkspace

try {
    $result = $apiInstance->patchWorkspacesWorkspaceId($workspace_id, $update_workspace);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->patchWorkspacesWorkspaceId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**| Workspace Id | |
| **update_workspace** | [**\OpenAPI\Client\Model\UpdateWorkspace**](../Model/UpdateWorkspace.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Workspace**](../Model/Workspace.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postWorkspace()`

```php
postWorkspace($create_workspace): \OpenAPI\Client\Model\Workspace
```

Create a Workspace

Creates a new Workspace in the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspaceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_workspace = new \OpenAPI\Client\Model\CreateWorkspace(); // \OpenAPI\Client\Model\CreateWorkspace

try {
    $result = $apiInstance->postWorkspace($create_workspace);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspaceApi->postWorkspace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_workspace** | [**\OpenAPI\Client\Model\CreateWorkspace**](../Model/CreateWorkspace.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Workspace**](../Model/Workspace.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
