# GriffNode\SystemApi

All URIs are relative to https://api.griffnode.com/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getHealth()**](SystemApi.md#getHealth) | **GET** /health | API health check |
| [**hostedCheckoutRedirect()**](SystemApi.md#hostedCheckoutRedirect) | **GET** /pay | Hosted-checkout redirect (browser flow, publishable key) |


## `getHealth()`

```php
getHealth(): \GriffNode\Model\GetHealth200Response
```

API health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new GriffNode\Api\SystemApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getHealth();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemApi->getHealth: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\GriffNode\Model\GetHealth200Response**](../Model/GetHealth200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `hostedCheckoutRedirect()`

```php
hostedCheckoutRedirect($pk, $amount, $crypto, $currency, $link)
```

Hosted-checkout redirect (browser flow, publishable key)

Browser-facing redirect to the hosted payment page, authenticated by a **publishable** key in the query string (safe to expose client-side). Not used by the server-side SDKs — included for completeness.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new GriffNode\Api\SystemApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pk = 'pk_example'; // string | Publishable key, pk_live_… / pk_test_…
$amount = 'amount_example'; // string | Fiat amount (≥ 1.00 USD equivalent).
$crypto = new \GriffNode\Model\\GriffNode\Model\CryptoSymbol(); // \GriffNode\Model\CryptoSymbol
$currency = 'USD'; // string | Fiat currency of `amount`. Ignored when `link` is set: a payment link always uses its own amount and currency.
$link = 'link_example'; // string | Payment-link slug. The link's own amount, currency, expiry and single-use rules apply (410 if expired, 409 if a single-use link was already paid).

try {
    $apiInstance->hostedCheckoutRedirect($pk, $amount, $crypto, $currency, $link);
} catch (Exception $e) {
    echo 'Exception when calling SystemApi->hostedCheckoutRedirect: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pk** | **string**| Publishable key, pk_live_… / pk_test_… | |
| **amount** | **string**| Fiat amount (≥ 1.00 USD equivalent). | |
| **crypto** | [**\GriffNode\Model\CryptoSymbol**](../Model/.md)|  | |
| **currency** | **string**| Fiat currency of &#x60;amount&#x60;. Ignored when &#x60;link&#x60; is set: a payment link always uses its own amount and currency. | [optional] [default to &#39;USD&#39;] |
| **link** | **string**| Payment-link slug. The link&#39;s own amount, currency, expiry and single-use rules apply (410 if expired, 409 if a single-use link was already paid). | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
