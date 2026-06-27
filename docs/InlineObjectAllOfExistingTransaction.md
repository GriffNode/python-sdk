# InlineObjectAllOfExistingTransaction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_id** | **str** |  | [optional] 
**status** | [**TransactionStatus**](TransactionStatus.md) |  | [optional] 
**payment_url** | **str** |  | [optional] 

## Example

```python
from cryptogate.models.inline_object_all_of_existing_transaction import InlineObjectAllOfExistingTransaction

# TODO update the JSON string below
json = "{}"
# create an instance of InlineObjectAllOfExistingTransaction from a JSON string
inline_object_all_of_existing_transaction_instance = InlineObjectAllOfExistingTransaction.from_json(json)
# print the JSON string representation of the object
print(InlineObjectAllOfExistingTransaction.to_json())

# convert the object into a dict
inline_object_all_of_existing_transaction_dict = inline_object_all_of_existing_transaction_instance.to_dict()
# create an instance of InlineObjectAllOfExistingTransaction from a dict
inline_object_all_of_existing_transaction_from_dict = InlineObjectAllOfExistingTransaction.from_dict(inline_object_all_of_existing_transaction_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


