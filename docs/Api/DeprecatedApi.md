# OpenAPI\Client\DeprecatedApi

All URIs are relative to https://api-sandbox.yousign.app/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createIdDocumentVerification()**](DeprecatedApi.md#createIdDocumentVerification) | **POST** /id_document_verifications | [DEPRECATED] Initiate a new ID document verification |
| [**getBankAccountVerifications()**](DeprecatedApi.md#getBankAccountVerifications) | **GET** /bank_account_verifications | [DEPRECATED] List Bank Account Verifications |
| [**getBankAccountVerificationsBankAccountVerificationId()**](DeprecatedApi.md#getBankAccountVerificationsBankAccountVerificationId) | **GET** /bank_account_verifications/{bankAccountVerificationId} | [DEPRECATED] Retrieve a bank account verification |
| [**getIdDocumentVerification()**](DeprecatedApi.md#getIdDocumentVerification) | **GET** /id_document_verifications/{idDocumentVerificationId} | [DEPRECATED] Retrieve an ID document verification |
| [**getIdDocumentVerifications()**](DeprecatedApi.md#getIdDocumentVerifications) | **GET** /id_document_verifications | [DEPRECATED] List ID Document Verifications |
| [**postBankAccountVerifications()**](DeprecatedApi.md#postBankAccountVerifications) | **POST** /bank_account_verifications | [DEPRECATED] Initiate a new Bank Account Verification |
| [**postDocuments()**](DeprecatedApi.md#postDocuments) | **POST** /documents | [DEPRECATED] Upload a Document |


## `createIdDocumentVerification()`

```php
createIdDocumentVerification($first_name, $last_name, $document_type, $file, $additional_file): \OpenAPI\Client\Model\LegacyIdDocumentVerificationCreated
```

[DEPRECATED] Initiate a new ID document verification

Deprecated endpoint, do not use. Verify a person’s ID document by sending the file containing their ID document (ID card, passport, residence permit or driving license).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$first_name = 'first_name_example'; // string | Please provide the holder first name, exactly as it appears on the ID document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don't provide it as part of the name.
$last_name = 'last_name_example'; // string | Please provide the holder last name, exactly as it appears on the ID document birth name. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don't provide it as part of the name.
$document_type = 'document_type_example'; // string | The document type to verify
$file = '/path/to/file.txt'; // \SplFileObject | Binary file
$additional_file = '/path/to/file.txt'; // \SplFileObject | Binary file

try {
    $result = $apiInstance->createIdDocumentVerification($first_name, $last_name, $document_type, $file, $additional_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->createIdDocumentVerification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **first_name** | **string**| Please provide the holder first name, exactly as it appears on the ID document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don&#39;t provide it as part of the name. | [optional] |
| **last_name** | **string**| Please provide the holder last name, exactly as it appears on the ID document birth name. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don&#39;t provide it as part of the name. | [optional] |
| **document_type** | **string**| The document type to verify | [optional] |
| **file** | **\SplFileObject****\SplFileObject**| Binary file | [optional] |
| **additional_file** | **\SplFileObject****\SplFileObject**| Binary file | [optional] |

### Return type

[**\OpenAPI\Client\Model\LegacyIdDocumentVerificationCreated**](../Model/LegacyIdDocumentVerificationCreated.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBankAccountVerifications()`

```php
getBankAccountVerifications($after, $limit, $status): \OpenAPI\Client\Model\GetBankAccountVerifications200Response
```

[DEPRECATED] List Bank Account Verifications

Deprecated endpoint, do not use. Returns the list of all Bank Account Verifications within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$status = 'status_example'; // string | Filter by status

try {
    $result = $apiInstance->getBankAccountVerifications($after, $limit, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->getBankAccountVerifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **status** | **string**| Filter by status | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetBankAccountVerifications200Response**](../Model/GetBankAccountVerifications200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBankAccountVerificationsBankAccountVerificationId()`

```php
getBankAccountVerificationsBankAccountVerificationId($bank_account_verification_id): \OpenAPI\Client\Model\GetBankAccountVerificationsBankAccountVerificationId200Response
```

[DEPRECATED] Retrieve a bank account verification

Deprecated endpoint, do not use. Get the detailed results of a bank account verification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bank_account_verification_id = 'bank_account_verification_id_example'; // string | The bank account verification ID

try {
    $result = $apiInstance->getBankAccountVerificationsBankAccountVerificationId($bank_account_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->getBankAccountVerificationsBankAccountVerificationId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bank_account_verification_id** | **string**| The bank account verification ID | |

### Return type

[**\OpenAPI\Client\Model\GetBankAccountVerificationsBankAccountVerificationId200Response**](../Model/GetBankAccountVerificationsBankAccountVerificationId200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIdDocumentVerification()`

```php
getIdDocumentVerification($id_document_verification_id): \OpenAPI\Client\Model\GetIdDocumentVerification200Response
```

[DEPRECATED] Retrieve an ID document verification

Deprecated endpoint, do not use. Get the detailed results of an ID document verification, including the status of the verification, the reasons in case of rejection and the data extracted from the ID document.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id_document_verification_id = 'id_document_verification_id_example'; // string | The ID document verification ID

try {
    $result = $apiInstance->getIdDocumentVerification($id_document_verification_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->getIdDocumentVerification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id_document_verification_id** | **string**| The ID document verification ID | |

### Return type

[**\OpenAPI\Client\Model\GetIdDocumentVerification200Response**](../Model/GetIdDocumentVerification200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIdDocumentVerifications()`

```php
getIdDocumentVerifications($after, $limit, $status): \OpenAPI\Client\Model\GetIdDocumentVerifications200Response
```

[DEPRECATED] List ID Document Verifications

Deprecated endpoint, do not use. Returns the list of all ID Document Verifications within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$after = 'after_example'; // string | After cursor (pagination)
$limit = 100; // int | The limit of items count to retrieve.
$status = 'status_example'; // string | Filter by status

try {
    $result = $apiInstance->getIdDocumentVerifications($after, $limit, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->getIdDocumentVerifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **after** | **string**| After cursor (pagination) | [optional] |
| **limit** | **int**| The limit of items count to retrieve. | [optional] [default to 100] |
| **status** | **string**| Filter by status | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetIdDocumentVerifications200Response**](../Model/GetIdDocumentVerifications200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postBankAccountVerifications()`

```php
postBankAccountVerifications($file, $first_name, $last_name, $iban, $bic, $legal_entity_name): \OpenAPI\Client\Model\LegacyBankAccountVerificationCreated
```

[DEPRECATED] Initiate a new Bank Account Verification

Deprecated endpoint, do not use. Creates a new Bank Account Verification resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | Binary file
$first_name = 'first_name_example'; // string | Please provide the holder first name, exactly as it appears on the bank account document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don't provide it as part of the name. The field can not be submitted if field \\\"legal_entity_name\\\" is provided.
$last_name = 'last_name_example'; // string | Please provide the holder last name, exactly as it appears on the bank account document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don't provide it as part of the name. The field can not be submitted if field \\\"legal_entity_name\\\" is provided.
$iban = 'iban_example'; // string | International Bank Account Number (IBAN)
$bic = 'bic_example'; // string | Business Identifier Codes (BIC)
$legal_entity_name = 'legal_entity_name_example'; // string | Please provide the legal entity name, exactly as it appears on the bank account document. Please match it exactly, with the same characters, same case. The field can not be submitted if fields \\\"first_name\\\" and \\\"last_name\\\" are provided.

try {
    $result = $apiInstance->postBankAccountVerifications($file, $first_name, $last_name, $iban, $bic, $legal_entity_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->postBankAccountVerifications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| Binary file | |
| **first_name** | **string**| Please provide the holder first name, exactly as it appears on the bank account document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don&#39;t provide it as part of the name. The field can not be submitted if field \\\&quot;legal_entity_name\\\&quot; is provided. | [optional] |
| **last_name** | **string**| Please provide the holder last name, exactly as it appears on the bank account document. Please match it exactly, with the same characters, same case. One exception: if the document mentions an honorary title, please don&#39;t provide it as part of the name. The field can not be submitted if field \\\&quot;legal_entity_name\\\&quot; is provided. | [optional] |
| **iban** | **string**| International Bank Account Number (IBAN) | [optional] |
| **bic** | **string**| Business Identifier Codes (BIC) | [optional] |
| **legal_entity_name** | **string**| Please provide the legal entity name, exactly as it appears on the bank account document. Please match it exactly, with the same characters, same case. The field can not be submitted if fields \\\&quot;first_name\\\&quot; and \\\&quot;last_name\\\&quot; are provided. | [optional] |

### Return type

[**\OpenAPI\Client\Model\LegacyBankAccountVerificationCreated**](../Model/LegacyBankAccountVerificationCreated.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postDocuments()`

```php
postDocuments($file, $nature, $insert_after_id, $password, $name, $initials, $parse_anchors): \OpenAPI\Client\Model\Document
```

[DEPRECATED] Upload a Document

Deprecated endpoint, do not use.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeprecatedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | Binary file
$nature = 'nature_example'; // string
$insert_after_id = 'insert_after_id_example'; // string | Insert just after the position of the specified document id
$password = 'password_example'; // string
$name = 'name_example'; // string | The document name. If not set, will use the uploaded document name. This value should contain any characters except \\\"\\\\\\\", \\\"/\\\" and can\\\\'t start and finish with a space.
$initials = new \OpenAPI\Client\Model\InitialsArea(); // \OpenAPI\Client\Model\InitialsArea
$parse_anchors = True; // bool

try {
    $result = $apiInstance->postDocuments($file, $nature, $insert_after_id, $password, $name, $initials, $parse_anchors);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeprecatedApi->postDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| Binary file | |
| **nature** | **string**|  | |
| **insert_after_id** | **string**| Insert just after the position of the specified document id | [optional] |
| **password** | **string**|  | [optional] |
| **name** | **string**| The document name. If not set, will use the uploaded document name. This value should contain any characters except \\\&quot;\\\\\\\&quot;, \\\&quot;/\\\&quot; and can\\\\&#39;t start and finish with a space. | [optional] |
| **initials** | [**\OpenAPI\Client\Model\InitialsArea**](../Model/InitialsArea.md)|  | [optional] |
| **parse_anchors** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Document**](../Model/Document.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
