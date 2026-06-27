# Plan


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | [**PlanTier**](PlanTier.md) |  | [optional] 
**monthly_price_usd** | **float** |  | [optional] 
**yearly_price_usd** | **float** |  | [optional] 
**monthly_transaction_limit** | **int** |  | [optional] 
**overage_cost_per_tx** | **float** |  | [optional] 
**webhook_support** | **bool** |  | [optional] 
**webhook_limit** | **int** |  | [optional] 
**ip_whitelist** | **bool** |  | [optional] 
**api_rate_limit_per_minute** | **int** |  | [optional] 
**api_rate_limit_per_hour** | **int** |  | [optional] 
**custom_pricing** | **bool** |  | [optional] 

## Example

```python
from cryptogate.models.plan import Plan

# TODO update the JSON string below
json = "{}"
# create an instance of Plan from a JSON string
plan_instance = Plan.from_json(json)
# print the JSON string representation of the object
print(Plan.to_json())

# convert the object into a dict
plan_dict = plan_instance.to_dict()
# create an instance of Plan from a dict
plan_from_dict = Plan.from_dict(plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


