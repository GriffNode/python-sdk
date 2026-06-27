# LineItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**quantity** | **int** |  | [optional] [default to 1]
**price** | **float** |  | 

## Example

```python
from cryptogate.models.line_item import LineItem

# TODO update the JSON string below
json = "{}"
# create an instance of LineItem from a JSON string
line_item_instance = LineItem.from_json(json)
# print the JSON string representation of the object
print(LineItem.to_json())

# convert the object into a dict
line_item_dict = line_item_instance.to_dict()
# create an instance of LineItem from a dict
line_item_from_dict = LineItem.from_dict(line_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


