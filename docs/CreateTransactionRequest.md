# CreateTransactionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**crypto** | [**CryptoSymbol**](CryptoSymbol.md) |  | 
**amount** | **float** | Fiat amount (≥ 1.00 USD equivalent). | 
**currency_fiat** | [**FiatCurrency**](FiatCurrency.md) |  | [optional] [default to FiatCurrency.USD]
**metadata** | **Dict[str, str]** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional] 
**customer_email** | **str** |  | [optional] 
**success_url** | **str** |  | [optional] 
**cancel_url** | **str** |  | [optional] 

## Example

```python
from cryptogate.models.create_transaction_request import CreateTransactionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTransactionRequest from a JSON string
create_transaction_request_instance = CreateTransactionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTransactionRequest.to_json())

# convert the object into a dict
create_transaction_request_dict = create_transaction_request_instance.to_dict()
# create an instance of CreateTransactionRequest from a dict
create_transaction_request_from_dict = CreateTransactionRequest.from_dict(create_transaction_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


