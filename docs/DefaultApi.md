# cryptogate.DefaultApi

All URIs are relative to *https://api.cryptogate.live/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**payment_webhook**](DefaultApi.md#payment_webhook) | **POST** /paymentEvent | Payment lifecycle event delivered to the merchant&#39;s webhook URL


# **payment_webhook**
> payment_webhook(webhook_payload=webhook_payload)

Payment lifecycle event delivered to the merchant's webhook URL

Signed with HMAC-SHA256 over the RAW request body. Verify by comparing `X-CryptoGate-Signature: sha256=<hex>` to `hex(hmac_sha256(webhook_secret, raw_body))` using a constant-time compare. Also sent: `X-CryptoGate-Event` (the event type) and `X-Webhook-ID` (unique delivery id — use for idempotency). 

### Example

* Bearer Authentication (SecretKey):

```python
import cryptogate
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
    api_instance = cryptogate.DefaultApi(api_client)
    webhook_payload = cryptogate.WebhookPayload() # WebhookPayload |  (optional)

    try:
        # Payment lifecycle event delivered to the merchant's webhook URL
        api_instance.payment_webhook(webhook_payload=webhook_payload)
    except Exception as e:
        print("Exception when calling DefaultApi->payment_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_payload** | [**WebhookPayload**](WebhookPayload.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[SecretKey](../README.md#SecretKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Acknowledge within 15s. Non-2xx is retried with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

