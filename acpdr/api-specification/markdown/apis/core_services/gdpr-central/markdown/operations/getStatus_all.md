
<a name="getstatus-all"></a>
### Retrieve details of all JobId's for a specific UserId/Logged in Users id
```
GET /data/privacy/gdpr
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**Authorization**  <br>*required*|Bearer XXXXX|string|
|**Header**|**Content-Type**  <br>*required*|application/json|string|
|**Header**|**x-api-key**  <br>*required*|acp_XXX_XXXX, IMS Client id which is whitelisted and subscribed to consume services on adobe.io|string|
|**Header**|**x-gw-ims-org-id**  <br>*required*|XXXXX47E56F59C747FXXXXX@AdobeOrg|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|If found, The details of requested jobId is returned.|[A GDPR Request model](../definitions/A_GDPR_Request_model.md#a-gdpr-request-model)|
|**400**|Bad Request. The request is malformed|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**401**|Unauthorized. The request has not been applied because it  lacks valid authentication credentials for the target resource.|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**403**|Forbidden. That combination of arguments is not allowed.|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**404**|Not Found. The resource the client is looking for isn't there.|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**405**|Method Not Allowed. Client sent a request using a HTTP method that the server doesn't support.|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**406**|Not Acceptable. Unacceptable content type. The caller sent an <b>Accept</b> header for a content type which does not exist on the server|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**422**|Unprocessable Entity. Client sent a correct request that contained invalid values for one or more parameters.|[Problem Detail](../definitions/Problem_Detail.md#problem-detail)|
|**500**|Internal Server Error. This is an indicator of a server-side error.|No Content|
|**502**|Bad Gateway. This is an indicator that the search back-end did not send a valid response.|No Content|
|**503**|Service Unavailable. This is an indicator of a potential server overload.|No Content|
|**504**|Gateway Timeout. This is an indicator that the search back-end did not complete a response within an allowed time period.|No Content|


#### Tags

* GDPR central API


#### Example HTTP request

##### Request path
```
/data/privacy/gdpr
```


##### Request header
```
json :
"string"
```


#### Example HTTP response

##### Response 200
```
json :
{
  "companyContexts" : [ {
    "namespace" : "string",
    "value" : "string"
  } ],
  "users" : [ {
    "key" : "string",
    "action" : [ "string" ],
    "userIDs" : [ {
      "namespace" : "string",
      "value" : "string",
      "type" : "string",
      "namespaceId" : 0,
      "isDeletedClientSide" : true
    } ]
  } ],
  "exclude" : [ "string" ]
  "include" : [ "string" ]
}
```


##### Response 400
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```


##### Response 401
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```


##### Response 403
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```


##### Response 404
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```


##### Response 405
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```


##### Response 406
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```


##### Response 422
```
json :
{
  "errorType" : "https://mcloud.io/client-error",
  "errorCode" : "4xx",
  "title" : "Client side error",
  "detail" : "Invalid ID format"
}
```



