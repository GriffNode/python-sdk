# WebhookPayload

Payment-event payload. AMOUNTS ARE STRINGS (e.g. \"100.00\", \"0.00109462\") to preserve decimal precision — parse before arithmetic. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **str** |  | 
**timestamp** | **datetime** |  | 
**transaction_id** | **str** |  | 
**status** | [**TransactionStatus**](TransactionStatus.md) |  | 
**currency_crypto** | [**CryptoSymbol**](CryptoSymbol.md) |  | [optional] 
**currency_fiat** | [**FiatCurrency**](FiatCurrency.md) |  | [optional] [default to FiatCurrency.USD]
**amount_fiat** | **str** | Decimal string. | [optional] 
**amount_usd** | **str** | Decimal string. | [optional] 
**amount_crypto** | **str** | Decimal string. | [optional] 
**order_id** | **str** |  | [optional] 
**receipt_url** | **str** | Present on completed/overpaid. | [optional] 
**metadata** | **Dict[str, str]** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional] 

## Example

```python
from griffnode.models.webhook_payload import WebhookPayload

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookPayload from a JSON string
webhook_payload_instance = WebhookPayload.from_json(json)
# print the JSON string representation of the object
print(WebhookPayload.to_json())

# convert the object into a dict
webhook_payload_dict = webhook_payload_instance.to_dict()
# create an instance of WebhookPayload from a dict
webhook_payload_from_dict = WebhookPayload.from_dict(webhook_payload_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


