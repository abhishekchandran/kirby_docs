
<a name="getclusters"></a>
### Fetches clusters satisfying the query criteria
```
GET /data/foundation/compute/clusters
```


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Header**|**x-api-key**  <br>*required*|The API key belonging to the calling client.|string||
|**Header**|**x-request-id**  <br>*optional*|A unique id generated by Adobe.io.|string||
|**Query**|**limit**  <br>*optional*|Number of records to fetch per page|integer (int32)|`10`|
|**Query**|**orderby**  <br>*optional*|Field to order results by.Can be multivalued, separated by comma.Supported fields: createdAt.Prepend property name with + for ASC,- for DESC order|string|`"-createdAt"`|
|**Query**|**property**  <br>*optional*|Comma separated property filters.Supported filters are on date range, status and userId(contains check) e.g createdAt>=2017-04-05T13:30:00Z,status==Active,userId~acp_testing@AdobeId|string||
|**Query**|**start**  <br>*optional*|Start value of property specified using orderby|string||


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Clusters retrieved|[ClusterListResponse](../definitions/ClusterListResponse.md#clusterlistresponse)|
|**401**|Unauthorized access|No Content|
|**406**|Non Acceptable Response Type.Only application/json allowed|No Content|
|**414**|Request URI is longer than allowed 2000 chars|No Content|
|**422**|Input validation failure|No Content|
|**503**|Request failed|No Content|


#### Produces

* `application/json`


#### Tags

* ComputeClusters


#### Example HTTP request

##### Request path
```
/data/foundation/compute/clusters
```


##### Request header
```
json :
"string"
```


##### Request query
```
json :
{
  "limit" : 0,
  "orderby" : "string",
  "property" : "string",
  "start" : "string"
}
```


#### Example HTTP response

##### Response 200
```
json :
{
  "result" : [ {
    "id" : "8a475fbd-4a58-4b90-bb9b-bb23b6c873ff",
    "name" : "Reporting Jobs Cluster",
    "status" : "string",
    "tags" : {
      "batch" : "123"
    },
    "workerType" : "ML_SIZE_LARGE",
    "minInstance" : 4,
    "maxInstance" : 16,
    "userId" : "[MCDP_HARVESTER@AdobeID]",
    "createdAt" : "2017-10-02T18:17:19Z",
    "updatedAt" : "2017-10-03T18:17:19Z",
    "property" : "ethos_role:8a475fbd-4a58-4b90-bb9b-bb23b6c873ff"
  } ],
  "_page" : {
    "orderBy" : "-createdAt",
    "property" : "id==123",
    "start" : "2017-05-05T00:00:00Z",
    "next" : "2017-05-01T00:00:00Z",
    "count" : 3
  },
  "next" : "string"
}
```


