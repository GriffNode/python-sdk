# cryptogate.AccountApi

All URIs are relative to *https://api.cryptogate.live/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_account**](AccountApi.md#get_account) | **GET** /account | Merchant plan, usage and limits
[**get_stats**](AccountApi.md#get_stats) | **GET** /stats | Merchant transaction analytics
[**list_balances**](AccountApi.md#list_balances) | **GET** /balances | On-platform balances (for overage/top-up; NOT crypto settlement)
[**list_invoices**](AccountApi.md#list_invoices) | **GET** /invoices | CryptoGate billing invoices (platform ↔ merchant)
[**list_plans**](AccountApi.md#list_plans) | **GET** /plans | Plan catalogue and pricing


# **get_account**
> GetAccount200Response get_account()

Merchant plan, usage and limits

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.get_account200_response import GetAccount200Response
from cryptogate.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.cryptogate.live/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cryptogate.Configuration(
    host = "https://api.cryptogate.live/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: SecretKey
configuration = cryptogate.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with cryptogate.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cryptogate.AccountApi(api_client)

    try:
        # Merchant plan, usage and limits
        api_response = api_instance.get_account()
        print("The response of AccountApi->get_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_account: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetAccount200Response**](GetAccount200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Account details. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_stats**
> GetStats200Response get_stats()

Merchant transaction analytics

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.get_stats200_response import GetStats200Response
from cryptogate.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.cryptogate.live/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cryptogate.Configuration(
    host = "https://api.cryptogate.live/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: SecretKey
configuration = cryptogate.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with cryptogate.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cryptogate.AccountApi(api_client)

    try:
        # Merchant transaction analytics
        api_response = api_instance.get_stats()
        print("The response of AccountApi->get_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_stats: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetStats200Response**](GetStats200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Stats. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_balances**
> ListBalances200Response list_balances()

On-platform balances (for overage/top-up; NOT crypto settlement)

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.list_balances200_response import ListBalances200Response
from cryptogate.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.cryptogate.live/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cryptogate.Configuration(
    host = "https://api.cryptogate.live/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: SecretKey
configuration = cryptogate.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with cryptogate.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cryptogate.AccountApi(api_client)

    try:
        # On-platform balances (for overage/top-up; NOT crypto settlement)
        api_response = api_instance.list_balances()
        print("The response of AccountApi->list_balances:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->list_balances: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ListBalances200Response**](ListBalances200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Balances. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_invoices**
> ListInvoices200Response list_invoices(limit=limit, offset=offset)

CryptoGate billing invoices (platform ↔ merchant)

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.list_invoices200_response import ListInvoices200Response
from cryptogate.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.cryptogate.live/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cryptogate.Configuration(
    host = "https://api.cryptogate.live/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: SecretKey
configuration = cryptogate.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with cryptogate.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cryptogate.AccountApi(api_client)
    limit = 20 # int |  (optional) (default to 20)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # CryptoGate billing invoices (platform ↔ merchant)
        api_response = api_instance.list_invoices(limit=limit, offset=offset)
        print("The response of AccountApi->list_invoices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->list_invoices: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**|  | [optional] [default to 20]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**ListInvoices200Response**](ListInvoices200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Invoices. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_plans**
> ListPlans200Response list_plans()

Plan catalogue and pricing

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.list_plans200_response import ListPlans200Response
from cryptogate.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.cryptogate.live/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cryptogate.Configuration(
    host = "https://api.cryptogate.live/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: SecretKey
configuration = cryptogate.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with cryptogate.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cryptogate.AccountApi(api_client)

    try:
        # Plan catalogue and pricing
        api_response = api_instance.list_plans()
        print("The response of AccountApi->list_plans:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->list_plans: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ListPlans200Response**](ListPlans200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plans. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

