# GriffNode\TransactionsApi

All URIs are relative to https://api.griffnode.com/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDetailedTransaction()**](TransactionsApi.md#createDetailedTransaction) | **POST** /transactions/create-detailed | Create an itemized transaction (Professional/Enterprise plans) |
| [**createTransaction()**](TransactionsApi.md#createTransaction) | **POST** /transactions/create | Create a payment transaction |
| [**getTransaction()**](TransactionsApi.md#getTransaction) | **GET** /transactions/{transaction_id} | Retrieve a single transaction |
| [**listTransactions()**](TransactionsApi.md#listTransactions) | **GET** /transactions/list | List the merchant&#39;s transactions (newest first) |


## `createDetailedTransaction()`

```php
createDetailedTransaction($create_detailed_transaction_request, $x_idempotency_key): \GriffNode\Model\TransactionEnvelope
```

Create an itemized transaction (Professional/Enterprise plans)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_detailed_transaction_request = new \GriffNode\Model\CreateDetailedTransactionRequest(); // \GriffNode\Model\CreateDetailedTransactionRequest
$x_idempotency_key = 'x_idempotency_key_example'; // string | Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can't double-charge the customer.

try {
    $result = $apiInstance->createDetailedTransaction($create_detailed_transaction_request, $x_idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->createDetailedTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_detailed_transaction_request** | [**\GriffNode\Model\CreateDetailedTransactionRequest**](../Model/CreateDetailedTransactionRequest.md)|  | |
| **x_idempotency_key** | **string**| Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can&#39;t double-charge the customer. | [optional] |

### Return type

[**\GriffNode\Model\TransactionEnvelope**](../Model/TransactionEnvelope.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createTransaction()`

```php
createTransaction($create_transaction_request, $x_idempotency_key): \GriffNode\Model\TransactionEnvelope
```

Create a payment transaction

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_transaction_request = new \GriffNode\Model\CreateTransactionRequest(); // \GriffNode\Model\CreateTransactionRequest
$x_idempotency_key = 'x_idempotency_key_example'; // string | Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can't double-charge the customer.

try {
    $result = $apiInstance->createTransaction($create_transaction_request, $x_idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->createTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_transaction_request** | [**\GriffNode\Model\CreateTransactionRequest**](../Model/CreateTransactionRequest.md)|  | |
| **x_idempotency_key** | **string**| Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can&#39;t double-charge the customer. | [optional] |

### Return type

[**\GriffNode\Model\TransactionEnvelope**](../Model/TransactionEnvelope.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTransaction()`

```php
getTransaction($transaction_id): \GriffNode\Model\TransactionEnvelope
```

Retrieve a single transaction

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transaction_id = 'transaction_id_example'; // string

try {
    $result = $apiInstance->getTransaction($transaction_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->getTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transaction_id** | **string**|  | |

### Return type

[**\GriffNode\Model\TransactionEnvelope**](../Model/TransactionEnvelope.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTransactions()`

```php
listTransactions($limit, $offset, $status, $crypto): \GriffNode\Model\ListTransactions200Response
```

List the merchant's transactions (newest first)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 20; // int
$offset = 0; // int
$status = new \GriffNode\Model\\GriffNode\Model\TransactionStatus(); // \GriffNode\Model\TransactionStatus
$crypto = new \GriffNode\Model\\GriffNode\Model\CryptoSymbol(); // \GriffNode\Model\CryptoSymbol

try {
    $result = $apiInstance->listTransactions($limit, $offset, $status, $crypto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->listTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 20] |
| **offset** | **int**|  | [optional] [default to 0] |
| **status** | [**\GriffNode\Model\TransactionStatus**](../Model/.md)|  | [optional] |
| **crypto** | [**\GriffNode\Model\CryptoSymbol**](../Model/.md)|  | [optional] |

### Return type

[**\GriffNode\Model\ListTransactions200Response**](../Model/ListTransactions200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
