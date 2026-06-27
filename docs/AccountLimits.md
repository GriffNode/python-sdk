# AccountLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_rate_limit_per_minute** | **int** |  | [optional] 
**api_rate_limit_per_hour** | **int** |  | [optional] 
**webhook_support** | **bool** |  | [optional] 

## Example

```python
from cryptogate.models.account_limits import AccountLimits

# TODO update the JSON string below
json = "{}"
# create an instance of AccountLimits from a JSON string
account_limits_instance = AccountLimits.from_json(json)
# print the JSON string representation of the object
print(AccountLimits.to_json())

# convert the object into a dict
account_limits_dict = account_limits_instance.to_dict()
# create an instance of AccountLimits from a dict
account_limits_from_dict = AccountLimits.from_dict(account_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


