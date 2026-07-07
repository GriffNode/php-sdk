# # Transaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_id** | **string** |  |
**status** | [**\GriffNode\Model\TransactionStatus**](TransactionStatus.md) |  |
**type** | **string** |  | [optional]
**crypto** | [**\GriffNode\Model\CryptoSymbol**](CryptoSymbol.md) |  |
**deposit_address** | **string** |  | [optional]
**amount_crypto** | **float** |  | [optional]
**amount_fiat** | **float** |  |
**amount_usd** | **float** |  |
**amount_paid** | **float** |  | [optional]
**amount_remaining** | **float** |  | [optional]
**currency_fiat** | [**\GriffNode\Model\FiatCurrency**](FiatCurrency.md) |  |
**fiat_to_usd_rate** | **float** |  | [optional]
**exchange_rate** | **float** | USD per unit of crypto, locked at creation. | [optional]
**confirmations_required** | **int** |  | [optional]
**payment_url** | **string** |  | [optional]
**order_id** | **string** |  | [optional]
**customer_email** | **string** |  | [optional]
**items** | [**\GriffNode\Model\LineItem[]**](LineItem.md) |  | [optional]
**payments** | [**\GriffNode\Model\PaymentSplit[]**](PaymentSplit.md) | On-chain payments detected toward this transaction. | [optional]
**metadata** | **array<string,string>** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional]
**success_url** | **string** |  | [optional]
**cancel_url** | **string** |  | [optional]
**created_at** | **\DateTime** |  |
**updated_at** | **\DateTime** |  | [optional]
**expires_at** | **\DateTime** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
