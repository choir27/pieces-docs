---
title: Relationship API | TypeScript SDK
---

# Relationship API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**relationshipsSpecificRelationshipSnapshot**](RelationshipApi#relationshipsspecificrelationshipsnapshot) | **GET** /relationship/\{relationship\} | /relationship/\{relationship\} [GET]


## **relationshipsSpecificRelationshipSnapshot** {#relationshipsspecificrelationshipsnapshot}
> Relationship relationshipsSpecificRelationshipSnapshot()

This will return a single relationship object.

### Example {#relationshipsspecificrelationshipsnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.RelationshipApi(configuration)

const body: Pieces.RelationshipsSpecificRelationshipSnapshotRequest = {
// string | this is a specific relationship uuid.
relationship: relationship_example,
};

apiInstance.relationshipsSpecificRelationshipSnapshot(body).then((data: Relationship) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#relationshipsspecificrelationshipsnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **relationship** | [**string**] | this is a specific relationship uuid. | defaults to undefined


### Return type {#relationshipsspecificrelationshipsnapshot-return-type}

[**Relationship**](../models/Relationship)

### HTTP request headers {#relationshipsspecificrelationshipsnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details {#relationshipsspecificrelationshipsnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |


