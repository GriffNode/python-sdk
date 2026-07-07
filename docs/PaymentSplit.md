# PaymentSplit

One on-chain payment toward the transaction.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**txid** | **str** | On-chain transaction hash (blockchain id, NOT the GriffNode transaction_id). | [optional] 
**amount_crypto** | **float** |  | [optional] 
**confirmations** | **int** |  | [optional] 
**status** | **str** |  | [optional] 
**detected_at** | **datetime** |  | [optional] 
**confirmed_at** | **datetime** |  | [optional] 

## Example

```python
from griffnode.models.payment_split import PaymentSplit

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSplit from a JSON string
payment_split_instance = PaymentSplit.from_json(json)
# print the JSON string representation of the object
print(PaymentSplit.to_json())

# convert the object into a dict
payment_split_dict = payment_split_instance.to_dict()
# create an instance of PaymentSplit from a dict
payment_split_from_dict = PaymentSplit.from_dict(payment_split_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


