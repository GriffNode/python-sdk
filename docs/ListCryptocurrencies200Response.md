# ListCryptocurrencies200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **object** |  | 
**data** | [**ListCryptocurrencies200ResponseData**](ListCryptocurrencies200ResponseData.md) |  | 

## Example

```python
from cryptogate.models.list_cryptocurrencies200_response import ListCryptocurrencies200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListCryptocurrencies200Response from a JSON string
list_cryptocurrencies200_response_instance = ListCryptocurrencies200Response.from_json(json)
# print the JSON string representation of the object
print(ListCryptocurrencies200Response.to_json())

# convert the object into a dict
list_cryptocurrencies200_response_dict = list_cryptocurrencies200_response_instance.to_dict()
# create an instance of ListCryptocurrencies200Response from a dict
list_cryptocurrencies200_response_from_dict = ListCryptocurrencies200Response.from_dict(list_cryptocurrencies200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


