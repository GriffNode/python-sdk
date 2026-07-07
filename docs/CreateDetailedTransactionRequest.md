# CreateDetailedTransactionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**crypto** | [**CryptoSymbol**](CryptoSymbol.md) |  | 
**currency_fiat** | [**FiatCurrency**](FiatCurrency.md) |  | [optional] [default to FiatCurrency.USD]
**items** | [**List[LineItem]**](LineItem.md) |  | 
**order_id** | **str** |  | 
**metadata** | **Dict[str, str]** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional] 
**customer_email** | **str** |  | [optional] 
**success_url** | **str** |  | [optional] 
**cancel_url** | **str** |  | [optional] 

## Example

```python
from griffnode.models.create_detailed_transaction_request import CreateDetailedTransactionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateDetailedTransactionRequest from a JSON string
create_detailed_transaction_request_instance = CreateDetailedTransactionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateDetailedTransactionRequest.to_json())

# convert the object into a dict
create_detailed_transaction_request_dict = create_detailed_transaction_request_instance.to_dict()
# create an instance of CreateDetailedTransactionRequest from a dict
create_detailed_transaction_request_from_dict = CreateDetailedTransactionRequest.from_dict(create_detailed_transaction_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


