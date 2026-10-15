# griffnode.SystemApi

All URIs are relative to *https://api.griffnode.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_health**](SystemApi.md#get_health) | **GET** /health | API health check
[**hosted_checkout_redirect**](SystemApi.md#hosted_checkout_redirect) | **GET** /pay | Hosted-checkout redirect (browser flow, publishable key)


# **get_health**
> GetHealth200Response get_health()

API health check

### Example


```python
import griffnode
from griffnode.models.get_health200_response import GetHealth200Response
from griffnode.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.griffnode.com/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = griffnode.Configuration(
    host = "https://api.griffnode.com/v1"
)


# Enter a context with an instance of the API client
with griffnode.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = griffnode.SystemApi(api_client)

    try:
        # API health check
        api_response = api_instance.get_health()
        print("The response of SystemApi->get_health:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SystemApi->get_health: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetHealth200Response**](GetHealth200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Service status (intentionally NOT wrapped in the success envelope). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **hosted_checkout_redirect**
> hosted_checkout_redirect(pk, amount, crypto, currency=currency, link=link)

Hosted-checkout redirect (browser flow, publishable key)

Browser-facing redirect to the hosted payment page, authenticated by a **publishable** key in the query string (safe to expose client-side). Not used by the server-side SDKs — included for completeness. 

### Example


```python
import griffnode
from griffnode.models.crypto_symbol import CryptoSymbol
from griffnode.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.griffnode.com/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = griffnode.Configuration(
    host = "https://api.griffnode.com/v1"
)


# Enter a context with an instance of the API client
with griffnode.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = griffnode.SystemApi(api_client)
    pk = 'pk_example' # str | Publishable key, pk_live_… / pk_test_…
    amount = 'amount_example' # str | Fiat amount (≥ 1.00 USD equivalent).
    crypto = griffnode.CryptoSymbol() # CryptoSymbol | 
    currency = USD # str | Fiat currency of `amount`. Ignored when `link` is set: a payment link always uses its own amount and currency. (optional) (default to USD)
    link = 'link_example' # str | Payment-link slug. The link's own amount, currency, expiry and single-use rules apply (410 if expired, 409 if a single-use link was already paid). (optional)

    try:
        # Hosted-checkout redirect (browser flow, publishable key)
        api_instance.hosted_checkout_redirect(pk, amount, crypto, currency=currency, link=link)
    except Exception as e:
        print("Exception when calling SystemApi->hosted_checkout_redirect: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pk** | **str**| Publishable key, pk_live_… / pk_test_… | 
 **amount** | **str**| Fiat amount (≥ 1.00 USD equivalent). | 
 **crypto** | [**CryptoSymbol**](.md)|  | 
 **currency** | **str**| Fiat currency of &#x60;amount&#x60;. Ignored when &#x60;link&#x60; is set: a payment link always uses its own amount and currency. | [optional] [default to USD]
 **link** | **str**| Payment-link slug. The link&#39;s own amount, currency, expiry and single-use rules apply (410 if expired, 409 if a single-use link was already paid). | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**302** | Redirect to https://griffnode.com/transaction/{transaction_id} |  -  |
**400** | Validation error (INVALID_REQUEST, INVALID_CRYPTO, INVALID_AMOUNT, AMOUNT_TOO_LOW, INVALID_CURRENCY, INVALID_METADATA, WALLET_NOT_CONFIGURED, MISSING_ITEMS, MISSING_ORDER_ID, …). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

