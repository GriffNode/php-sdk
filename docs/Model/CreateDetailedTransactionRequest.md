# # CreateDetailedTransactionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**crypto** | [**\GriffNode\Model\CryptoSymbol**](CryptoSymbol.md) |  |
**currency_fiat** | [**\GriffNode\Model\FiatCurrency**](FiatCurrency.md) |  | [optional]
**items** | [**\GriffNode\Model\LineItem[]**](LineItem.md) |  |
**order_id** | **string** |  |
**metadata** | **array<string,string>** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional]
**customer_email** | **string** |  | [optional]
**success_url** | **string** |  | [optional]
**cancel_url** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
