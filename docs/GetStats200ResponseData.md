# GetStats200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_transactions** | **int** |  | [optional] 
**monthly_transactions** | **int** |  | [optional] 
**total_volume_fiat** | **float** |  | [optional] 
**unique_customers** | **int** |  | [optional] 

## Example

```python
from cryptogate.models.get_stats200_response_data import GetStats200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetStats200ResponseData from a JSON string
get_stats200_response_data_instance = GetStats200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetStats200ResponseData.to_json())

# convert the object into a dict
get_stats200_response_data_dict = get_stats200_response_data_instance.to_dict()
# create an instance of GetStats200ResponseData from a dict
get_stats200_response_data_from_dict = GetStats200ResponseData.from_dict(get_stats200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


