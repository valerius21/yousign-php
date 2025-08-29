# OpenAPI\Client\UserApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteUsersUserId()**](UserApi.md#deleteUsersUserId) | **DELETE** /users/{userId} | Delete a User |
| [**deleteWorkspaceWorkspaceIdUsersUserId()**](UserApi.md#deleteWorkspaceWorkspaceIdUsersUserId) | **DELETE** /workspaces/{workspaceId}/users/{userId} | Remove a user from a workspace |
| [**getUsers()**](UserApi.md#getUsers) | **GET** /users | List Users |
| [**getUsersUserId()**](UserApi.md#getUsersUserId) | **GET** /users/{userId} | Get a User |
| [**patchUsersUserId()**](UserApi.md#patchUsersUserId) | **PATCH** /users/{userId} | Update a User |
| [**postUsers()**](UserApi.md#postUsers) | **POST** /users | Create a new User |
| [**putWorkspacesWorkspaceIdUsers()**](UserApi.md#putWorkspacesWorkspaceIdUsers) | **PUT** /workspaces/{workspaceId}/users/{userId} | Associate a user to a workspace |


## `deleteUsersUserId()`

```php
deleteUsersUserId($user_id)
```

Delete a User

Deletes a given User and its Invitation, only possible when the User is in `invited` status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User Id

try {
    $apiInstance->deleteUsersUserId($user_id);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->deleteUsersUserId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User Id | |

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

## `deleteWorkspaceWorkspaceIdUsersUserId()`

```php
deleteWorkspaceWorkspaceIdUsersUserId($workspace_id, $user_id)
```

Remove a user from a workspace

Removes a User from a given Workspace.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string | Workspace Id
$user_id = 'user_id_example'; // string | User Id

try {
    $apiInstance->deleteWorkspaceWorkspaceIdUsersUserId($workspace_id, $user_id);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->deleteWorkspaceWorkspaceIdUsersUserId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**| Workspace Id | |
| **user_id** | **string**| User Id | |

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

## `getUsers()`

```php
getUsers($after, $limit, $email): \OpenAPI\Client\Model\GetUsers200Response
```

List Users

Returns the list of all the Users within your Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$email = {"eq":["user@example.com"]}; // object | Filter by `email`. Allowed operators: `eq`. Example: `email[eq]=user@example.com`

try {
    $result = $apiInstance->getUsers($after, $limit, $email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **email** | [**object**](../Model/.md)| Filter by &#x60;email&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;email[eq]&#x3D;user@example.com&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetUsers200Response**](../Model/GetUsers200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUsersUserId()`

```php
getUsersUserId($user_id): \OpenAPI\Client\Model\User
```

Get a User

Retrieves a given User within your Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User Id

try {
    $result = $apiInstance->getUsersUserId($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUsersUserId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User Id | |

### Return type

[**\OpenAPI\Client\Model\User**](../Model/User.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchUsersUserId()`

```php
patchUsersUserId($user_id, $update_user): \OpenAPI\Client\Model\User
```

Update a User

Updates a given User. Any parameters not provided are left unchanged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User Id
$update_user = new \OpenAPI\Client\Model\UpdateUser(); // \OpenAPI\Client\Model\UpdateUser

try {
    $result = $apiInstance->patchUsersUserId($user_id, $update_user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->patchUsersUserId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User Id | |
| **update_user** | [**\OpenAPI\Client\Model\UpdateUser**](../Model/UpdateUser.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\User**](../Model/User.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postUsers()`

```php
postUsers($create_user): \OpenAPI\Client\Model\User
```

Create a new User

Creates a new application User and sends them an invitation email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_user = new \OpenAPI\Client\Model\CreateUser(); // \OpenAPI\Client\Model\CreateUser

try {
    $result = $apiInstance->postUsers($create_user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->postUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_user** | [**\OpenAPI\Client\Model\CreateUser**](../Model/CreateUser.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\User**](../Model/User.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `putWorkspacesWorkspaceIdUsers()`

```php
putWorkspacesWorkspaceIdUsers($workspace_id, $user_id)
```

Associate a user to a workspace

Associates a User with a given Workspace.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string | Workspace Id
$user_id = 'user_id_example'; // string | User Id

try {
    $apiInstance->putWorkspacesWorkspaceIdUsers($workspace_id, $user_id);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->putWorkspacesWorkspaceIdUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**| Workspace Id | |
| **user_id** | **string**| User Id | |

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
