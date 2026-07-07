# GriffNode\BillingApi

All URIs are relative to https://api.griffnode.com/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBillingCheckout()**](BillingApi.md#createBillingCheckout) | **POST** /billing/checkout | Start a plan upgrade or account top-up |


## `createBillingCheckout()`

```php
createBillingCheckout($create_billing_checkout_request): \GriffNode\Model\TransactionEnvelope
```

Start a plan upgrade or account top-up

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_billing_checkout_request = new \GriffNode\Model\CreateBillingCheckoutRequest(); // \GriffNode\Model\CreateBillingCheckoutRequest

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
| **create_billing_checkout_request** | [**\GriffNode\Model\CreateBillingCheckoutRequest**](../Model/CreateBillingCheckoutRequest.md)|  | |

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
