---
title: WorkstreamSummaries API | TypeScript SDK
---

# WorkstreamSummaries API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**workstreamSummariesCreateNewWorkstreamSummary**](WorkstreamSummariesApi#workstreamsummariescreatenewworkstreamsummary) | **POST** /workstream_summaries/create | /workstream_summaries/create [POST]
[**workstreamSummariesDeleteSpecificWorkstreamSummary**](WorkstreamSummariesApi#workstreamsummariesdeletespecificworkstreamsummary) | **POST** /workstream_summaries/\{workstream_summary\}/delete | /workstream_summaries/\{workstream_summary\}/delete [POST]
[**workstreamSummariesSnapshot**](WorkstreamSummariesApi#workstreamsummariessnapshot) | **GET** /workstream_summaries | /workstream_summaries [GET]


## **workstreamSummariesCreateNewWorkstreamSummary** {#workstreamsummariescreatenewworkstreamsummary}
> WorkstreamSummary workstreamSummariesCreateNewWorkstreamSummary()

This will create a new WorkstreamSummary in the database.

### Example {#workstreamsummariescreatenewworkstreamsummary-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.WorkstreamSummariesApi(configuration)

const body: Pieces.WorkstreamSummariesCreateNewWorkstreamSummaryRequest = {
// boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
transferables: true,
// SeededWorkstreamSummary (optional)
seededWorkstreamSummary: ,
};

apiInstance.workstreamSummariesCreateNewWorkstreamSummary(body).then((data: WorkstreamSummary) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#workstreamsummariescreatenewworkstreamsummary-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededWorkstreamSummary** | **SeededWorkstreamSummary**|  |
 **transferables** | [**boolean**] | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | (optional) defaults to undefined


### Return type {#workstreamsummariescreatenewworkstreamsummary-return-type}

[**WorkstreamSummary**](../models/WorkstreamSummary)

### HTTP request headers {#workstreamsummariescreatenewworkstreamsummary-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#workstreamsummariescreatenewworkstreamsummary-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **workstreamSummariesDeleteSpecificWorkstreamSummary** {#workstreamsummariesdeletespecificworkstreamsummary}
> workstreamSummariesDeleteSpecificWorkstreamSummary()

This will delete a specific workstream_summary from the database!

### Example {#workstreamsummariesdeletespecificworkstreamsummary-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.WorkstreamSummariesApi(configuration)

const body: Pieces.WorkstreamSummariesDeleteSpecificWorkstreamSummaryRequest = {
// string | This is a identifier that is used to identify a specific workstream_summary.
workstreamSummary: workstreamSummary_example,
};

apiInstance.workstreamSummariesDeleteSpecificWorkstreamSummary(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#workstreamsummariesdeletespecificworkstreamsummary-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workstreamSummary** | [**string**] | This is a identifier that is used to identify a specific workstream_summary. | defaults to undefined


### Return type {#workstreamsummariesdeletespecificworkstreamsummary-return-type}

void (empty response body)

### HTTP request headers {#workstreamsummariesdeletespecificworkstreamsummary-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#workstreamsummariesdeletespecificworkstreamsummary-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **workstreamSummariesSnapshot** {#workstreamsummariessnapshot}
> WorkstreamSummaries workstreamSummariesSnapshot()

This will get a snapshot of all your workstream summaries.

### Example {#workstreamsummariessnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.WorkstreamSummariesApi(configuration)

const body: Pieces.WorkstreamSummariesSnapshotRequest = {
// boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
transferables: true,
};

apiInstance.workstreamSummariesSnapshot(body).then((data: WorkstreamSummaries) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#workstreamsummariessnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | [**boolean**] | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | (optional) defaults to undefined


### Return type {#workstreamsummariessnapshot-return-type}

[**WorkstreamSummaries**](../models/WorkstreamSummaries)

### HTTP request headers {#workstreamsummariessnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#workstreamsummariessnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |


