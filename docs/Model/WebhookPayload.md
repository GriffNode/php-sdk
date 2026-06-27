# # WebhookPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **string** |  |
**timestamp** | **\DateTime** |  |
**transaction_id** | **string** |  |
**status** | [**\CryptoGate\Model\TransactionStatus**](TransactionStatus.md) |  |
**currency_crypto** | [**\CryptoGate\Model\CryptoSymbol**](CryptoSymbol.md) |  | [optional]
**currency_fiat** | [**\CryptoGate\Model\FiatCurrency**](FiatCurrency.md) |  | [optional]
**amount_fiat** | **string** | Decimal string. | [optional]
**amount_usd** | **string** | Decimal string. | [optional]
**amount_crypto** | **string** | Decimal string. | [optional]
**order_id** | **string** |  | [optional]
**receipt_url** | **string** | Present on completed/overpaid. | [optional]
**metadata** | **array<string,string>** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
