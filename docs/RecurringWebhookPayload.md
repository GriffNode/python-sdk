# RecurringWebhookPayload

Recurring payment request event. schedule_id + your own reference identify the customer/order. The period's payment also fires the normal payment.* events. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**event** | **str** |  | 
**timestamp** | **datetime** |  | 
**schedule_id** | **str** |  | 
**reference** | **str** | Your own customer/order id, as entered on the schedule. | [optional] 
**customer_email** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**amount_fiat** | **str** | Decimal string. | [optional] 
**currency_fiat** | **str** |  | [optional] 
**interval** | **str** |  | [optional] 
**status** | **str** |  | 
**period_no** | **int** | recurring.payment.* only. | [optional] 
**transaction_id** | **str** | recurring.payment.completed only. | [optional] 
**reason** | **str** | recurring.stopped only. | [optional] 

## Example

```python
from griffnode.models.recurring_webhook_payload import RecurringWebhookPayload

# TODO update the JSON string below
json = "{}"
# create an instance of RecurringWebhookPayload from a JSON string
recurring_webhook_payload_instance = RecurringWebhookPayload.from_json(json)
# print the JSON string representation of the object
print(RecurringWebhookPayload.to_json())

# convert the object into a dict
recurring_webhook_payload_dict = recurring_webhook_payload_instance.to_dict()
# create an instance of RecurringWebhookPayload from a dict
recurring_webhook_payload_from_dict = RecurringWebhookPayload.from_dict(recurring_webhook_payload_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


