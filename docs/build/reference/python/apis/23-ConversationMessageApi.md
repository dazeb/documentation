---
title: ConversationMessage API | Python SDK
---

# ConversationMessage API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**message_associate_annotation**](ConversationMessageApi#message_associate_annotation) | **POST** /message/\{message\}/annotations/associate/\{annotation\} | /message/\{message\}/annotations/associate/\{annotation\} [POST]
[**message_disassociate_annotation**](ConversationMessageApi#message_disassociate_annotation) | **POST** /message/\{message\}/annotations/disassociate/\{annotation\} | /message/\{message\}/annotations/disassociate/\{annotation\} [POST]
[**message_scores_increment**](ConversationMessageApi#message_scores_increment) | **POST** /message/\{message\}/scores/increment | '/message/\{message\}/scores/increment' [POST]
[**message_specific_message_snapshot**](ConversationMessageApi#message_specific_message_snapshot) | **GET** /message/\{message\} | /message/\{message\} [GET]
[**message_specific_message_update**](ConversationMessageApi#message_specific_message_update) | **POST** /message/update | /message/update [GET]
[**message_update_value**](ConversationMessageApi#message_update_value) | **POST** /message/update/value | /message/update/value [POST]


## **message_associate_annotation** {#message_associate_annotation}
> message_associate_annotation(annotation, message)

/message/\{message\}/annotations/associate/\{annotation\} [POST]

This will associate a message with an annotation.

### Example {#message_associate_annotation-example}


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
    api_instance = pieces_os_client.ConversationMessageApi(api_client)
    annotation = 'annotation_example' # str | This is a specific annotation uuid.
    message = 'message_example' # str | This is the uuid of a message.

    try:
        # /message/\{message\}/annotations/associate/\{annotation\} [POST]
        api_instance.message_associate_annotation(annotation, message)
    except Exception as e:
        print("Exception when calling ConversationMessageApi->message_associate_annotation: %s\n" % e)
```



### Parameters {#message_associate_annotation-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation** | **str**| This is a specific annotation uuid. | 
 **message** | **str**| This is the uuid of a message. | 

### Return type {#message_associate_annotation-return-type}

void (empty response body)

### Authorization {#message_associate_annotation-authorization}

No authorization required

### HTTP request headers {#message_associate_annotation-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain


### HTTP response details {#message_associate_annotation-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **message_disassociate_annotation** {#message_disassociate_annotation}
> message_disassociate_annotation(annotation, message)

/message/\{message\}/annotations/disassociate/\{annotation\} [POST]

This will enable us to dissassociate a message from an annotation.

### Example {#message_disassociate_annotation-example}


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
    api_instance = pieces_os_client.ConversationMessageApi(api_client)
    annotation = 'annotation_example' # str | This is a specific annotation uuid.
    message = 'message_example' # str | This is the uuid of a message.

    try:
        # /message/\{message\}/annotations/disassociate/\{annotation\} [POST]
        api_instance.message_disassociate_annotation(annotation, message)
    except Exception as e:
        print("Exception when calling ConversationMessageApi->message_disassociate_annotation: %s\n" % e)
```



### Parameters {#message_disassociate_annotation-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation** | **str**| This is a specific annotation uuid. | 
 **message** | **str**| This is the uuid of a message. | 

### Return type {#message_disassociate_annotation-return-type}

void (empty response body)

### Authorization {#message_disassociate_annotation-authorization}

No authorization required

### HTTP request headers {#message_disassociate_annotation-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain


### HTTP response details {#message_disassociate_annotation-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **message_scores_increment** {#message_scores_increment}
> message_scores_increment(message, seeded_score_increment=seeded_score_increment)

'/message/\{message\}/scores/increment' [POST]

This will take in a SeededScoreIncrement and will increment the material relative to the incoming body.

### Example {#message_scores_increment-example}


```python
import pieces_os_client
from pieces_os_client.models.seeded_score_increment import SeededScoreIncrement
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
    api_instance = pieces_os_client.ConversationMessageApi(api_client)
    message = 'message_example' # str | This is the uuid of a message.
    seeded_score_increment = pieces_os_client.SeededScoreIncrement() # SeededScoreIncrement |  (optional)

    try:
        # '/message/\{message\}/scores/increment' [POST]
        api_instance.message_scores_increment(message, seeded_score_increment=seeded_score_increment)
    except Exception as e:
        print("Exception when calling ConversationMessageApi->message_scores_increment: %s\n" % e)
```



### Parameters {#message_scores_increment-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message** | **str**| This is the uuid of a message. | 
 **seeded_score_increment** | [**SeededScoreIncrement**](../models/SeededScoreIncrement)|  | [optional] 

### Return type {#message_scores_increment-return-type}

void (empty response body)

### Authorization {#message_scores_increment-authorization}

No authorization required

### HTTP request headers {#message_scores_increment-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain


### HTTP response details {#message_scores_increment-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **message_specific_message_snapshot** {#message_specific_message_snapshot}
> ConversationMessage message_specific_message_snapshot(message, transferables=transferables)

/message/\{message\} [GET]

This will get a specific snapshot of a message

### Example {#message_specific_message_snapshot-example}


```python
import pieces_os_client
from pieces_os_client.models.conversation_message import ConversationMessage
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
    api_instance = pieces_os_client.ConversationMessageApi(api_client)
    message = 'message_example' # str | This is the uuid of a message.
    transferables = True # bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)

    try:
        # /message/\{message\} [GET]
        api_response = api_instance.message_specific_message_snapshot(message, transferables=transferables)
        print("The response of ConversationMessageApi->message_specific_message_snapshot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConversationMessageApi->message_specific_message_snapshot: %s\n" % e)
```



### Parameters {#message_specific_message_snapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message** | **str**| This is the uuid of a message. | 
 **transferables** | **bool**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#message_specific_message_snapshot-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#message_specific_message_snapshot-authorization}

No authorization required

### HTTP request headers {#message_specific_message_snapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain


### HTTP response details {#message_specific_message_snapshot-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**410** | Website not found. |  -  |

## **message_specific_message_update** {#message_specific_message_update}
> ConversationMessage message_specific_message_update(transferables=transferables, conversation_message=conversation_message)

/message/update [GET]

This will update a conversation message.

### Example {#message_specific_message_update-example}


```python
import pieces_os_client
from pieces_os_client.models.conversation_message import ConversationMessage
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
    api_instance = pieces_os_client.ConversationMessageApi(api_client)
    transferables = True # bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
    conversation_message = pieces_os_client.ConversationMessage() # ConversationMessage |  (optional)

    try:
        # /message/update [GET]
        api_response = api_instance.message_specific_message_update(transferables=transferables, conversation_message=conversation_message)
        print("The response of ConversationMessageApi->message_specific_message_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConversationMessageApi->message_specific_message_update: %s\n" % e)
```



### Parameters {#message_specific_message_update-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 
 **conversation_message** | [**ConversationMessage**](../models/ConversationMessage)|  | [optional] 

### Return type {#message_specific_message_update-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#message_specific_message_update-authorization}

No authorization required

### HTTP request headers {#message_specific_message_update-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#message_specific_message_update-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **message_update_value** {#message_update_value}
> ConversationMessage message_update_value(transferables=transferables, conversation_message=conversation_message)

/message/update/value [POST]

This will update the value of a conversation message.

### Example {#message_update_value-example}


```python
import pieces_os_client
from pieces_os_client.models.conversation_message import ConversationMessage
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
    api_instance = pieces_os_client.ConversationMessageApi(api_client)
    transferables = True # bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
    conversation_message = pieces_os_client.ConversationMessage() # ConversationMessage |  (optional)

    try:
        # /message/update/value [POST]
        api_response = api_instance.message_update_value(transferables=transferables, conversation_message=conversation_message)
        print("The response of ConversationMessageApi->message_update_value:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConversationMessageApi->message_update_value: %s\n" % e)
```



### Parameters {#message_update_value-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 
 **conversation_message** | [**ConversationMessage**](../models/ConversationMessage)|  | [optional] 

### Return type {#message_update_value-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#message_update_value-authorization}

No authorization required

### HTTP request headers {#message_update_value-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#message_update_value-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

