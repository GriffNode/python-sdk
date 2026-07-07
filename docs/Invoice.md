# Invoice


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_id** | **str** |  | [optional] 
**purchase_type** | **str** |  | [optional] 
**amount_fiat** | **float** |  | [optional] 
**currency_fiat** | [**FiatCurrency**](FiatCurrency.md) |  | [optional] [default to FiatCurrency.USD]
**status** | **str** |  | [optional] 
**crypto_symbol** | [**CryptoSymbol**](CryptoSymbol.md) |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**confirmed_at** | **datetime** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from griffnode.models.invoice import Invoice

# TODO update the JSON string below
json = "{}"
# create an instance of Invoice from a JSON string
invoice_instance = Invoice.from_json(json)
# print the JSON string representation of the object
print(Invoice.to_json())

# convert the object into a dict
invoice_dict = invoice_instance.to_dict()
# create an instance of Invoice from a dict
invoice_from_dict = Invoice.from_dict(invoice_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


