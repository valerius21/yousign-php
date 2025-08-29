# OpenAPI\Client\UserInvitationApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInvitations()**](UserInvitationApi.md#getInvitations) | **GET** /users/invitations | List User Invitations |
| [**getUsersInvitationInvitationId()**](UserInvitationApi.md#getUsersInvitationInvitationId) | **GET** /users/invitations/{invitationId} | Get an Invitation |
| [**getUsersUserIdInvitation()**](UserInvitationApi.md#getUsersUserIdInvitation) | **GET** /users/{userId}/invitation | Get a User Invitation via the User |


## `getInvitations()`

```php
getInvitations($after, $limit, $email): \OpenAPI\Client\Model\GetInvitations200Response
```

List User Invitations

Returns the list of all the Users Invitations within your Organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserInvitationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$email = {"eq":["user@example.com"]}; // object | Filter by `email`. Allowed operators: `eq`. Example: `email[eq]=user@example.com`

try {
    $result = $apiInstance->getInvitations($after, $limit, $email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserInvitationApi->getInvitations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **email** | [**object**](../Model/.md)| Filter by &#x60;email&#x60;. Allowed operators: &#x60;eq&#x60;. Example: &#x60;email[eq]&#x3D;user@example.com&#x60; | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetInvitations200Response**](../Model/GetInvitations200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUsersInvitationInvitationId()`

```php
getUsersInvitationInvitationId($invitation_id): \OpenAPI\Client\Model\UserInvitation
```

Get an Invitation

Retrieves a given User Invitation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserInvitationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invitation_id = 'invitation_id_example'; // string | Invitation Id

try {
    $result = $apiInstance->getUsersInvitationInvitationId($invitation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserInvitationApi->getUsersInvitationInvitationId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invitation_id** | **string**| Invitation Id | |

### Return type

[**\OpenAPI\Client\Model\UserInvitation**](../Model/UserInvitation.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUsersUserIdInvitation()`

```php
getUsersUserIdInvitation($user_id): \OpenAPI\Client\Model\UserInvitation
```

Get a User Invitation via the User

Retrieves the Invitation of a given User. The Invitation only exists when the User is in `invited` status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserInvitationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User Id

try {
    $result = $apiInstance->getUsersUserIdInvitation($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserInvitationApi->getUsersUserIdInvitation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User Id | |

### Return type

[**\OpenAPI\Client\Model\UserInvitation**](../Model/UserInvitation.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
