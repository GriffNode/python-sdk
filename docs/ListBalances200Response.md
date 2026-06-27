# ListBalances200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **object** |  | 
**data** | [**ListBalances200ResponseData**](ListBalances200ResponseData.md) |  | 

## Example

```python
from cryptogate.models.list_balances200_response import ListBalances200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListBalances200Response from a JSON string
list_balances200_response_instance = ListBalances200Response.from_json(json)
# print the JSON string representation of the object
print(ListBalances200Response.to_json())

# convert the object into a dict
list_balances200_response_dict = list_balances200_response_instance.to_dict()
# create an instance of ListBalances200Response from a dict
list_balances200_response_from_dict = ListBalances200Response.from_dict(list_balances200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


