---
title: WorkstreamEvents API | TypeScript SDK
---

# WorkstreamEvents API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**workstreamEventsCreateNewWorkstreamEvent**](WorkstreamEventsApi#workstreameventscreatenewworkstreamevent) | **POST** /workstream_events/create | /workstream_events/create [POST]
[**workstreamEventsDeleteSpecificWorkstreamEvent**](WorkstreamEventsApi#workstreameventsdeletespecificworkstreamevent) | **POST** /workstream_events/\{workstream_event\}/delete | /workstream_events/\{workstream_event\}/delete [POST]
[**workstreamEventsSnapshot**](WorkstreamEventsApi#workstreameventssnapshot) | **GET** /workstream_events | /workstream_events [GET]


## **workstreamEventsCreateNewWorkstreamEvent** {#workstreameventscreatenewworkstreamevent}
> WorkstreamEvent workstreamEventsCreateNewWorkstreamEvent()

This will create a new WorkstreamEvent in the database.

### Example {#workstreameventscreatenewworkstreamevent-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.WorkstreamEventsApi(configuration)

const body: Pieces.WorkstreamEventsCreateNewWorkstreamEventRequest = {
// boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
transferables: true,
// SeededWorkstreamEvent (optional)
seededWorkstreamEvent: ,
};

apiInstance.workstreamEventsCreateNewWorkstreamEvent(body).then((data: WorkstreamEvent) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#workstreameventscreatenewworkstreamevent-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededWorkstreamEvent** | **SeededWorkstreamEvent**|  |
 **transferables** | [**boolean**] | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | (optional) defaults to undefined


### Return type {#workstreameventscreatenewworkstreamevent-return-type}

[**WorkstreamEvent**](../models/WorkstreamEvent)

### HTTP request headers {#workstreameventscreatenewworkstreamevent-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#workstreameventscreatenewworkstreamevent-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **workstreamEventsDeleteSpecificWorkstreamEvent** {#workstreameventsdeletespecificworkstreamevent}
> workstreamEventsDeleteSpecificWorkstreamEvent()

This will delete a specific workstream_event from the database!

### Example {#workstreameventsdeletespecificworkstreamevent-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.WorkstreamEventsApi(configuration)

const body: Pieces.WorkstreamEventsDeleteSpecificWorkstreamEventRequest = {
// string | This is a identifier that is used to identify a specific workstream_event.
workstreamEvent: workstreamEvent_example,
};

apiInstance.workstreamEventsDeleteSpecificWorkstreamEvent(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#workstreameventsdeletespecificworkstreamevent-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workstreamEvent** | [**string**] | This is a identifier that is used to identify a specific workstream_event. | defaults to undefined


### Return type {#workstreameventsdeletespecificworkstreamevent-return-type}

void (empty response body)

### HTTP request headers {#workstreameventsdeletespecificworkstreamevent-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#workstreameventsdeletespecificworkstreamevent-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **workstreamEventsSnapshot** {#workstreameventssnapshot}
> WorkstreamEvents workstreamEventsSnapshot()

This will get a snapshot of all your workstream events.

### Example {#workstreameventssnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.WorkstreamEventsApi(configuration)

const body: Pieces.WorkstreamEventsSnapshotRequest = {
// boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
transferables: true,
};

apiInstance.workstreamEventsSnapshot(body).then((data: WorkstreamEvents) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#workstreameventssnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | [**boolean**] | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | (optional) defaults to undefined


### Return type {#workstreameventssnapshot-return-type}

[**WorkstreamEvents**](../models/WorkstreamEvents)

### HTTP request headers {#workstreameventssnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#workstreameventssnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |


