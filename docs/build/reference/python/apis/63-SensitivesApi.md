---
title: Sensitives API | Python SDK
---

# Sensitives API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**sensitives_create_new_sensitive**](SensitivesApi#sensitives_create_new_sensitive) | **POST** /sensitives/create | /sensitives/create [POST]
[**sensitives_delete_sensitive**](SensitivesApi#sensitives_delete_sensitive) | **POST** /sensitives/\{sensitive\}/delete | /sensitives/\{sensitive\}/delete [POST]
[**sensitives_snapshot**](SensitivesApi#sensitives_snapshot) | **GET** /sensitives | /sensitives [GET]


## **sensitives_create_new_sensitive** {#sensitives_create_new_sensitive}
> Sensitive sensitives_create_new_sensitive(seeded_sensitive=seeded_sensitive)

/sensitives/create [POST]

This will create a new sensitive model.

### Example {#sensitives_create_new_sensitive-example}


```python
import pieces_os_client
from pieces_os_client.models.seeded_sensitive import SeededSensitive
from pieces_os_client.models.sensitive import Sensitive
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.SensitivesApi(api_client)
    seeded_sensitive = pieces_os_client.SeededSensitive() # SeededSensitive |  (optional)

    try:
        # /sensitives/create [POST]
        api_response = api_instance.sensitives_create_new_sensitive(seeded_sensitive=seeded_sensitive)
        print("The response of SensitivesApi->sensitives_create_new_sensitive:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SensitivesApi->sensitives_create_new_sensitive: %s\n" % e)
```



### Parameters {#sensitives_create_new_sensitive-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seeded_sensitive** | [**SeededSensitive**](../models/SeededSensitive)|  | [optional] 

### Return type {#sensitives_create_new_sensitive-return-type}

[**Sensitive**](../models/Sensitive)

### Authorization {#sensitives_create_new_sensitive-authorization}

No authorization required

### HTTP request headers {#sensitives_create_new_sensitive-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#sensitives_create_new_sensitive-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **sensitives_delete_sensitive** {#sensitives_delete_sensitive}
> sensitives_delete_sensitive(sensitive)

/sensitives/\{sensitive\}/delete [POST]

This will delete a sensitive based on the sensitive uuid.

### Example {#sensitives_delete_sensitive-example}


```python
import pieces_os_client
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.SensitivesApi(api_client)
    sensitive = 'sensitive_example' # str | This is a uuid that represents a sensitive.

    try:
        # /sensitives/\{sensitive\}/delete [POST]
        api_instance.sensitives_delete_sensitive(sensitive)
    except Exception as e:
        print("Exception when calling SensitivesApi->sensitives_delete_sensitive: %s\n" % e)
```



### Parameters {#sensitives_delete_sensitive-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sensitive** | **str**| This is a uuid that represents a sensitive. | 

### Return type {#sensitives_delete_sensitive-return-type}

void (empty response body)

### Authorization {#sensitives_delete_sensitive-authorization}

No authorization required

### HTTP request headers {#sensitives_delete_sensitive-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain


### HTTP response details {#sensitives_delete_sensitive-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**500** |  |  -  |

## **sensitives_snapshot** {#sensitives_snapshot}
> Sensitives sensitives_snapshot()

/sensitives [GET]

This will get a snapshot of all of the sensitives.

### Example {#sensitives_snapshot-example}


```python
import pieces_os_client
from pieces_os_client.models.sensitives import Sensitives
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.SensitivesApi(api_client)

    try:
        # /sensitives [GET]
        api_response = api_instance.sensitives_snapshot()
        print("The response of SensitivesApi->sensitives_snapshot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SensitivesApi->sensitives_snapshot: %s\n" % e)
```



### Parameters {#sensitives_snapshot-parameters}

This endpoint does not need any parameters.

### Return type {#sensitives_snapshot-return-type}

[**Sensitives**](../models/Sensitives)

### Authorization {#sensitives_snapshot-authorization}

No authorization required

### HTTP request headers {#sensitives_snapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain


### HTTP response details {#sensitives_snapshot-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

