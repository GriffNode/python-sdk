# AccountPlan


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | [**PlanTier**](PlanTier.md) |  | [optional] 
**billing_cycle** | **str** |  | [optional] 
**auto_renewal** | **bool** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from griffnode.models.account_plan import AccountPlan

# TODO update the JSON string below
json = "{}"
# create an instance of AccountPlan from a JSON string
account_plan_instance = AccountPlan.from_json(json)
# print the JSON string representation of the object
print(AccountPlan.to_json())

# convert the object into a dict
account_plan_dict = account_plan_instance.to_dict()
# create an instance of AccountPlan from a dict
account_plan_from_dict = AccountPlan.from_dict(account_plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


