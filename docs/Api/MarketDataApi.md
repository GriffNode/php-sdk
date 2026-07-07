# GriffNode\MarketDataApi

All URIs are relative to https://api.griffnode.com/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPrices()**](MarketDataApi.md#getPrices) | **GET** /prices | Current crypto and fiat exchange rates (USD-denominated) |
| [**listCryptocurrencies()**](MarketDataApi.md#listCryptocurrencies) | **GET** /cryptos/list | All supported cryptocurrencies and tokens |
| [**listMerchantCryptocurrencies()**](MarketDataApi.md#listMerchantCryptocurrencies) | **GET** /merchant/cryptos | Cryptocurrencies this merchant has wallets configured for |


## `getPrices()`

```php
getPrices(): \GriffNode\Model\GetPrices200Response
```

Current crypto and fiat exchange rates (USD-denominated)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\MarketDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getPrices();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketDataApi->getPrices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\GriffNode\Model\GetPrices200Response**](../Model/GetPrices200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCryptocurrencies()`

```php
listCryptocurrencies(): \GriffNode\Model\ListCryptocurrencies200Response
```

All supported cryptocurrencies and tokens

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\MarketDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listCryptocurrencies();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketDataApi->listCryptocurrencies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\GriffNode\Model\ListCryptocurrencies200Response**](../Model/ListCryptocurrencies200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listMerchantCryptocurrencies()`

```php
listMerchantCryptocurrencies(): \GriffNode\Model\ListCryptocurrencies200Response
```

Cryptocurrencies this merchant has wallets configured for

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\MarketDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listMerchantCryptocurrencies();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketDataApi->listMerchantCryptocurrencies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\GriffNode\Model\ListCryptocurrencies200Response**](../Model/ListCryptocurrencies200Response.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
