# Cryptocurrency


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**symbol** | [**CryptoSymbol**](CryptoSymbol.md) |  | [optional] 
**name** | **str** |  | [optional] 
**blockchain** | **str** |  | [optional] 
**network** | **str** |  | [optional] 
**type** | **str** |  | [optional] 

## Example

```python
from cryptogate.models.cryptocurrency import Cryptocurrency

# TODO update the JSON string below
json = "{}"
# create an instance of Cryptocurrency from a JSON string
cryptocurrency_instance = Cryptocurrency.from_json(json)
# print the JSON string representation of the object
print(Cryptocurrency.to_json())

# convert the object into a dict
cryptocurrency_dict = cryptocurrency_instance.to_dict()
# create an instance of Cryptocurrency from a dict
cryptocurrency_from_dict = Cryptocurrency.from_dict(cryptocurrency_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


