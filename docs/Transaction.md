# Transaction

The canonical, curated public view of a transaction (same shape from create, get and list). Internal fields (capability tokens, client_ip, address_index, derivation/db internals) are deliberately NOT exposed. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_id** | **str** |  | 
**status** | [**TransactionStatus**](TransactionStatus.md) |  | 
**type** | **str** |  | [optional] 
**crypto** | [**CryptoSymbol**](CryptoSymbol.md) |  | 
**deposit_address** | **str** |  | [optional] 
**amount_crypto** | **float** |  | [optional] 
**amount_fiat** | **float** |  | 
**amount_usd** | **float** |  | 
**amount_paid** | **float** |  | [optional] 
**amount_remaining** | **float** |  | [optional] 
**currency_fiat** | [**FiatCurrency**](FiatCurrency.md) |  | [default to FiatCurrency.USD]
**fiat_to_usd_rate** | **float** |  | [optional] 
**exchange_rate** | **float** | USD per unit of crypto, locked at creation. | [optional] 
**confirmations_required** | **int** |  | [optional] 
**payment_url** | **str** |  | [optional] 
**order_id** | **str** |  | [optional] 
**customer_email** | **str** |  | [optional] 
**items** | [**List[LineItem]**](LineItem.md) |  | [optional] 
**payments** | [**List[PaymentSplit]**](PaymentSplit.md) | On-chain payments detected toward this transaction. | [optional] 
**metadata** | **Dict[str, str]** | Free-form key/value (≤20 keys, string values ≤500 chars, ≤4 KB total). | [optional] 
**success_url** | **str** |  | [optional] 
**cancel_url** | **str** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | [optional] 
**expires_at** | **datetime** |  | 

## Example

```python
from cryptogate.models.transaction import Transaction

# TODO update the JSON string below
json = "{}"
# create an instance of Transaction from a JSON string
transaction_instance = Transaction.from_json(json)
# print the JSON string representation of the object
print(Transaction.to_json())

# convert the object into a dict
transaction_dict = transaction_instance.to_dict()
# create an instance of Transaction from a dict
transaction_from_dict = Transaction.from_dict(transaction_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


