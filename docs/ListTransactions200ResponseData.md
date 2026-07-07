# ListTransactions200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transactions** | [**List[Transaction]**](Transaction.md) |  | 
**pagination** | [**Pagination**](Pagination.md) |  | 

## Example

```python
from griffnode.models.list_transactions200_response_data import ListTransactions200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of ListTransactions200ResponseData from a JSON string
list_transactions200_response_data_instance = ListTransactions200ResponseData.from_json(json)
# print the JSON string representation of the object
print(ListTransactions200ResponseData.to_json())

# convert the object into a dict
list_transactions200_response_data_dict = list_transactions200_response_data_instance.to_dict()
# create an instance of ListTransactions200ResponseData from a dict
list_transactions200_response_data_from_dict = ListTransactions200ResponseData.from_dict(list_transactions200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


