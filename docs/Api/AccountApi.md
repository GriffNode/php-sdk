# CryptoGate\AccountApi

All URIs are relative to https://api.cryptogate.live/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAccount()**](AccountApi.md#getAccount) | **GET** /account | Merchant plan, usage and limits |
| [**getStats()**](AccountApi.md#getStats) | **GET** /stats | Merchant transaction analytics |
| [**listBalances()**](AccountApi.md#listBalances) | **GET** /balances | On-platform balances (for overage/top-up; NOT crypto settlement) |
| [**listInvoices()**](AccountApi.md#listInvoices) | **GET** /invoices | CryptoGate billing invoices (platform ↔ merchant) |
| [**listPlans()**](AccountApi.md#listPlans) | **GET** /plans | Plan catalogue and pricing |


## `getAccount()`

```php
getAccount(): \CryptoGate\Model\GetAccount200Response
```

Merchant plan, usage and limits

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = CryptoGate\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new CryptoGate\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAccount();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->getAccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\CryptoGate\Model\GetAccount200Response**](../Model/GetAccount200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStats()`

```php
getStats(): \CryptoGate\Model\GetStats200Response
```

Merchant transaction analytics

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = CryptoGate\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new CryptoGate\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getStats();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->getStats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\CryptoGate\Model\GetStats200Response**](../Model/GetStats200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBalances()`

```php
listBalances(): \CryptoGate\Model\ListBalances200Response
```

On-platform balances (for overage/top-up; NOT crypto settlement)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = CryptoGate\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new CryptoGate\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listBalances();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->listBalances: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\CryptoGate\Model\ListBalances200Response**](../Model/ListBalances200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInvoices()`

```php
listInvoices($limit, $offset): \CryptoGate\Model\ListInvoices200Response
```

CryptoGate billing invoices (platform ↔ merchant)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = CryptoGate\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new CryptoGate\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 20; // int
$offset = 0; // int

try {
    $result = $apiInstance->listInvoices($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->listInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 20] |
| **offset** | **int**|  | [optional] [default to 0] |

### Return type

[**\CryptoGate\Model\ListInvoices200Response**](../Model/ListInvoices200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPlans()`

```php
listPlans(): \CryptoGate\Model\ListPlans200Response
```

Plan catalogue and pricing

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = CryptoGate\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new CryptoGate\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listPlans();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->listPlans: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\CryptoGate\Model\ListPlans200Response**](../Model/ListPlans200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
