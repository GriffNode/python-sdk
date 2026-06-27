# ListBalances200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**balances** | [**List[Balance]**](Balance.md) |  | [optional] 

## Example

```python
from cryptogate.models.list_balances200_response_data import ListBalances200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of ListBalances200ResponseData from a JSON string
list_balances200_response_data_instance = ListBalances200ResponseData.from_json(json)
# print the JSON string representation of the object
print(ListBalances200ResponseData.to_json())

# convert the object into a dict
list_balances200_response_data_dict = list_balances200_response_data_instance.to_dict()
# create an instance of ListBalances200ResponseData from a dict
list_balances200_response_data_from_dict = ListBalances200ResponseData.from_dict(list_balances200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


