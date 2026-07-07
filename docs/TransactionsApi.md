# griffnode.TransactionsApi

All URIs are relative to *https://api.griffnode.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_detailed_transaction**](TransactionsApi.md#create_detailed_transaction) | **POST** /transactions/create-detailed | Create an itemized transaction (Professional/Enterprise plans)
[**create_transaction**](TransactionsApi.md#create_transaction) | **POST** /transactions/create | Create a payment transaction
[**get_transaction**](TransactionsApi.md#get_transaction) | **GET** /transactions/{transaction_id} | Retrieve a single transaction
[**list_transactions**](TransactionsApi.md#list_transactions) | **GET** /transactions/list | List the merchant&#39;s transactions (newest first)


# **create_detailed_transaction**
> TransactionEnvelope create_detailed_transaction(create_detailed_transaction_request, x_idempotency_key=x_idempotency_key)

Create an itemized transaction (Professional/Enterprise plans)

### Example

* Bearer Authentication (SecretKey):

```python
import griffnode
from griffnode.models.create_detailed_transaction_request import CreateDetailedTransactionRequest
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
    api_instance = griffnode.TransactionsApi(api_client)
    create_detailed_transaction_request = griffnode.CreateDetailedTransactionRequest() # CreateDetailedTransactionRequest | 
    x_idempotency_key = 'x_idempotency_key_example' # str | Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can't double-charge the customer.  (optional)

    try:
        # Create an itemized transaction (Professional/Enterprise plans)
        api_response = api_instance.create_detailed_transaction(create_detailed_transaction_request, x_idempotency_key=x_idempotency_key)
        print("The response of TransactionsApi->create_detailed_transaction:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->create_detailed_transaction: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_detailed_transaction_request** | [**CreateDetailedTransactionRequest**](CreateDetailedTransactionRequest.md)|  | 
 **x_idempotency_key** | **str**| Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can&#39;t double-charge the customer.  | [optional] 

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
**201** | Transaction created. |  -  |
**400** | Validation error (INVALID_REQUEST, INVALID_CRYPTO, INVALID_AMOUNT, AMOUNT_TOO_LOW, INVALID_CURRENCY, INVALID_METADATA, WALLET_NOT_CONFIGURED, MISSING_ITEMS, MISSING_ORDER_ID, …). |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**402** | Merchant platform balance too low for overage fees (INSUFFICIENT_BALANCE). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |
**429** | Rate limit or quota exceeded. &#x60;error&#x60; is &#x60;RATE_LIMIT_EXCEEDED&#x60; (per-minute request rate — honour &#x60;Retry-After&#x60;) or &#x60;MONTHLY_LIMIT_REACHED&#x60; (the plan&#39;s monthly transaction quota). Rate-limit headers accompany the &#x60;RATE_LIMIT_EXCEEDED&#x60; case.  |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_transaction**
> TransactionEnvelope create_transaction(create_transaction_request, x_idempotency_key=x_idempotency_key)

Create a payment transaction

### Example

* Bearer Authentication (SecretKey):

```python
import griffnode
from griffnode.models.create_transaction_request import CreateTransactionRequest
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
    api_instance = griffnode.TransactionsApi(api_client)
    create_transaction_request = griffnode.CreateTransactionRequest() # CreateTransactionRequest | 
    x_idempotency_key = 'x_idempotency_key_example' # str | Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can't double-charge the customer.  (optional)

    try:
        # Create a payment transaction
        api_response = api_instance.create_transaction(create_transaction_request, x_idempotency_key=x_idempotency_key)
        print("The response of TransactionsApi->create_transaction:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->create_transaction: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_transaction_request** | [**CreateTransactionRequest**](CreateTransactionRequest.md)|  | 
 **x_idempotency_key** | **str**| Optional unique key for a create request (e.g. a UUID). A retried create with the same key returns the original transaction instead of creating a duplicate — send it on every create so a network retry can&#39;t double-charge the customer.  | [optional] 

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
**201** | Transaction created. |  -  |
**400** | Validation error (INVALID_REQUEST, INVALID_CRYPTO, INVALID_AMOUNT, AMOUNT_TOO_LOW, INVALID_CURRENCY, INVALID_METADATA, WALLET_NOT_CONFIGURED, MISSING_ITEMS, MISSING_ORDER_ID, …). |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**402** | Merchant platform balance too low for overage fees (INSUFFICIENT_BALANCE). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |
**409** | This client IP already has an active transaction (ACTIVE_TRANSACTION_EXISTS). Body includes an &#x60;existing_transaction&#x60; object. |  -  |
**429** | Rate limit or quota exceeded. &#x60;error&#x60; is &#x60;RATE_LIMIT_EXCEEDED&#x60; (per-minute request rate — honour &#x60;Retry-After&#x60;) or &#x60;MONTHLY_LIMIT_REACHED&#x60; (the plan&#39;s monthly transaction quota). Rate-limit headers accompany the &#x60;RATE_LIMIT_EXCEEDED&#x60; case.  |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_transaction**
> TransactionEnvelope get_transaction(transaction_id)

Retrieve a single transaction

### Example

* Bearer Authentication (SecretKey):

```python
import griffnode
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
    api_instance = griffnode.TransactionsApi(api_client)
    transaction_id = 'transaction_id_example' # str | 

    try:
        # Retrieve a single transaction
        api_response = api_instance.get_transaction(transaction_id)
        print("The response of TransactionsApi->get_transaction:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->get_transaction: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **str**|  | 

### Return type

[**TransactionEnvelope**](TransactionEnvelope.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The transaction. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |
**404** | Resource not found (TRANSACTION_NOT_FOUND). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_transactions**
> ListTransactions200Response list_transactions(limit=limit, offset=offset, status=status, crypto=crypto)

List the merchant's transactions (newest first)

### Example

* Bearer Authentication (SecretKey):

```python
import griffnode
from griffnode.models.crypto_symbol import CryptoSymbol
from griffnode.models.list_transactions200_response import ListTransactions200Response
from griffnode.models.transaction_status import TransactionStatus
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
    api_instance = griffnode.TransactionsApi(api_client)
    limit = 20 # int |  (optional) (default to 20)
    offset = 0 # int |  (optional) (default to 0)
    status = griffnode.TransactionStatus() # TransactionStatus |  (optional)
    crypto = griffnode.CryptoSymbol() # CryptoSymbol |  (optional)

    try:
        # List the merchant's transactions (newest first)
        api_response = api_instance.list_transactions(limit=limit, offset=offset, status=status, crypto=crypto)
        print("The response of TransactionsApi->list_transactions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->list_transactions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**|  | [optional] [default to 20]
 **offset** | **int**|  | [optional] [default to 0]
 **status** | [**TransactionStatus**](.md)|  | [optional] 
 **crypto** | [**CryptoSymbol**](.md)|  | [optional] 

### Return type

[**ListTransactions200Response**](ListTransactions200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A page of transactions. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**403** | Key lacks permission — e.g. a publishable key on a secret-only endpoint, or plan too low (FORBIDDEN, USE_PAY_ENDPOINT, PLAN_UPGRADE_REQUIRED, NO_ACTIVE_PLAN). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

