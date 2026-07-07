# TransactionEnvelope


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **object** |  | 
**data** | [**Transaction**](Transaction.md) |  | 

## Example

```python
from griffnode.models.transaction_envelope import TransactionEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of TransactionEnvelope from a JSON string
transaction_envelope_instance = TransactionEnvelope.from_json(json)
# print the JSON string representation of the object
print(TransactionEnvelope.to_json())

# convert the object into a dict
transaction_envelope_dict = transaction_envelope_instance.to_dict()
# create an instance of TransactionEnvelope from a dict
transaction_envelope_from_dict = TransactionEnvelope.from_dict(transaction_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


