# # CreateTransactionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**crypto** | [**\GriffNode\Model\CryptoSymbol**](CryptoSymbol.md) |  |
**amount** | **float** | Fiat amount (≥ 1.00 USD equivalent). |
**currency_fiat** | [**\GriffNode\Model\FiatCurrency**](FiatCurrency.md) |  | [optional]
**metadata** | **array<string,string>** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional]
**customer_email** | **string** |  | [optional]
**success_url** | **string** |  | [optional]
**cancel_url** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
