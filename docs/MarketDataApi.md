# cryptogate.MarketDataApi

All URIs are relative to *https://api.cryptogate.live/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_prices**](MarketDataApi.md#get_prices) | **GET** /prices | Current crypto and fiat exchange rates (USD-denominated)
[**list_cryptocurrencies**](MarketDataApi.md#list_cryptocurrencies) | **GET** /cryptos/list | All supported cryptocurrencies and tokens
[**list_merchant_cryptocurrencies**](MarketDataApi.md#list_merchant_cryptocurrencies) | **GET** /merchant/cryptos | Cryptocurrencies this merchant has wallets configured for


# **get_prices**
> GetPrices200Response get_prices()

Current crypto and fiat exchange rates (USD-denominated)

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.get_prices200_response import GetPrices200Response
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
    api_instance = cryptogate.MarketDataApi(api_client)

    try:
        # Current crypto and fiat exchange rates (USD-denominated)
        api_response = api_instance.get_prices()
        print("The response of MarketDataApi->get_prices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MarketDataApi->get_prices: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetPrices200Response**](GetPrices200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Live rates. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |
**500** | Internal error (RATE_FETCH_FAILED, ADDRESS_GENERATION_FAILED, MIDAS_ERROR, …). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_cryptocurrencies**
> ListCryptocurrencies200Response list_cryptocurrencies()

All supported cryptocurrencies and tokens

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.list_cryptocurrencies200_response import ListCryptocurrencies200Response
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
    api_instance = cryptogate.MarketDataApi(api_client)

    try:
        # All supported cryptocurrencies and tokens
        api_response = api_instance.list_cryptocurrencies()
        print("The response of MarketDataApi->list_cryptocurrencies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MarketDataApi->list_cryptocurrencies: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ListCryptocurrencies200Response**](ListCryptocurrencies200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Supported-currency catalogue. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_merchant_cryptocurrencies**
> ListCryptocurrencies200Response list_merchant_cryptocurrencies()

Cryptocurrencies this merchant has wallets configured for

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
from cryptogate.models.list_cryptocurrencies200_response import ListCryptocurrencies200Response
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
    api_instance = cryptogate.MarketDataApi(api_client)

    try:
        # Cryptocurrencies this merchant has wallets configured for
        api_response = api_instance.list_merchant_cryptocurrencies()
        print("The response of MarketDataApi->list_merchant_cryptocurrencies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MarketDataApi->list_merchant_cryptocurrencies: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ListCryptocurrencies200Response**](ListCryptocurrencies200Response.md)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The merchant&#39;s configured currencies. |  -  |
**401** | Missing or invalid API key (UNAUTHORIZED). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

