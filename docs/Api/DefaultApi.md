# GriffNode\DefaultApi

All URIs are relative to https://api.griffnode.com/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**paymentWebhook()**](DefaultApi.md#paymentWebhook) | **POST** /paymentEvent | Payment lifecycle event delivered to the merchant&#39;s webhook URL |


## `paymentWebhook()`

```php
paymentWebhook($webhook_payload)
```

Payment lifecycle event delivered to the merchant's webhook URL

Signed with HMAC-SHA256 over the RAW request body. Verify by comparing `X-GriffNode-Signature: sha256=<hex>` to `hex(hmac_sha256(webhook_secret, raw_body))` using a constant-time compare. Also sent: `X-GriffNode-Event` (the event type) and `X-Webhook-ID` (unique delivery id — use for idempotency).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: SecretKey
$config = GriffNode\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GriffNode\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_payload = new \GriffNode\Model\WebhookPayload(); // \GriffNode\Model\WebhookPayload

try {
    $apiInstance->paymentWebhook($webhook_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->paymentWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_payload** | [**\GriffNode\Model\WebhookPayload**](../Model/WebhookPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[SecretKey](../../README.md#SecretKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
