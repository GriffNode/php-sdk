# # RecurringWebhookPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**event** | **string** |  |
**timestamp** | **\DateTime** |  |
**schedule_id** | **string** |  |
**reference** | **string** | Your own customer/order id, as entered on the schedule. | [optional]
**customer_email** | **string** |  | [optional]
**description** | **string** |  | [optional]
**amount_fiat** | **string** | Decimal string. | [optional]
**currency_fiat** | **string** |  | [optional]
**interval** | **string** |  | [optional]
**status** | **string** |  |
**period_no** | **int** | recurring.payment.* only. | [optional]
**transaction_id** | **string** | recurring.payment.completed only. | [optional]
**reason** | **string** | recurring.stopped only. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
