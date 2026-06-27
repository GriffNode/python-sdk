# ListCryptocurrencies200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cryptocurrencies** | [**List[Cryptocurrency]**](Cryptocurrency.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from cryptogate.models.list_cryptocurrencies200_response_data import ListCryptocurrencies200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of ListCryptocurrencies200ResponseData from a JSON string
list_cryptocurrencies200_response_data_instance = ListCryptocurrencies200ResponseData.from_json(json)
# print the JSON string representation of the object
print(ListCryptocurrencies200ResponseData.to_json())

# convert the object into a dict
list_cryptocurrencies200_response_data_dict = list_cryptocurrencies200_response_data_instance.to_dict()
# create an instance of ListCryptocurrencies200ResponseData from a dict
list_cryptocurrencies200_response_data_from_dict = ListCryptocurrencies200ResponseData.from_dict(list_cryptocurrencies200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


