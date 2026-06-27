# CryptoGate\BillingApi

All URIs are relative to https://api.cryptogate.live/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBillingCheckout()**](BillingApi.md#createBillingCheckout) | **POST** /billing/checkout | Start a plan upgrade or account top-up |


## `createBillingCheckout()`

```php
createBillingCheckout($create_billing_checkout_request): \CryptoGate\Model\TransactionEnvelope
```

Start a plan upgrade or account top-up

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = CryptoGate\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new CryptoGate\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_billing_checkout_request = new \CryptoGate\Model\CreateBillingCheckoutRequest(); // \CryptoGate\Model\CreateBillingCheckoutRequest

try {
    $result = $apiInstance->createBillingCheckout($create_billing_checkout_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->createBillingCheckout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_billing_checkout_request** | [**\CryptoGate\Model\CreateBillingCheckoutRequest**](../Model/CreateBillingCheckoutRequest.md)|  | |

### Return type

[**\CryptoGate\Model\TransactionEnvelope**](../Model/TransactionEnvelope.md)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
