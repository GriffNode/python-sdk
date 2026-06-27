# ListPlans200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plans** | [**List[Plan]**](Plan.md) |  | [optional] 
**billing_cycles** | **List[str]** |  | [optional] 

## Example

```python
from cryptogate.models.list_plans200_response_data import ListPlans200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of ListPlans200ResponseData from a JSON string
list_plans200_response_data_instance = ListPlans200ResponseData.from_json(json)
# print the JSON string representation of the object
print(ListPlans200ResponseData.to_json())

# convert the object into a dict
list_plans200_response_data_dict = list_plans200_response_data_instance.to_dict()
# create an instance of ListPlans200ResponseData from a dict
list_plans200_response_data_from_dict = ListPlans200ResponseData.from_dict(list_plans200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


