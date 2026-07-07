# griffnode.BillingApi

All URIs are relative to *https://api.griffnode.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_billing_checkout**](BillingApi.md#create_billing_checkout) | **POST** /billing/checkout | Start a plan upgrade or account top-up


# **create_billing_checkout**
> TransactionEnvelope create_billing_checkout(create_billing_checkout_request)

Start a plan upgrade or account top-up

### Example

* Bearer Authentication (SecretKey):

```python
import griffnode
from griffnode.models.create_billing_checkout_request import CreateBillingCheckoutRequest
from griffnode.models.transaction_envelope import TransactionEnvelope
from griffnode.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.griffnode.com/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = griffnode.Configuration(
    host = "https://api.griffnode.com/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: SecretKey
configuration = griffnode.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with griffnode.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = griffnode.BillingApi(api_client)
    create_billing_checkout_request = griffnode.CreateBillingCheckoutRequest() # CreateBillingCheckoutRequest | 

    try:
        # Start a plan upgrade or account top-up
        api_response = api_instance.create_billing_checkout(create_billing_checkout_request)
        print("The response of BillingApi->create_billing_checkout:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_billing_checkout: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_billing_checkout_request** | [**CreateBillingCheckoutRequest**](CreateBillingCheckoutRequest.md)|  | 

### Return type

[**TransactionEnvelope**](TransactionEnvelope.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Billing transaction created. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**402** | Merchant platform balance too low for overage fees (INSUFFICIENT_BALANCE). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

