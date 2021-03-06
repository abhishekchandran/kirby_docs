
<a name="post_data_set"></a>
### Saves a new DataSet.
```
POST /dataSets
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-api-key**  <br>*required*|The API key belonging to the calling client.|string|
|**Header**|**x-gw-ims-org-id**  <br>*required*|The owning IMS organization identifier.|string|
|**Query**|**requestDataSource**  <br>*optional*|Set to true if you want Catalog to create a dataSource on your behalf; otherwise, pass a dataSourceId in the body.|string|


#### Body parameter
Data set to be posted

*Name* : dataSet  
*Flags* : required  
*Type* : [dataSetRequest](../definitions/dataSetRequest.md#datasetrequest)


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**201**|Array[ @/dataSets/dataSetId ]  <br>**Headers** :   <br>`Location` (string) : The URI of the newly created resource.|< string > array|
|**400**|Bad request|No Content|
|**403**|Forbidden|No Content|
|**500**|Internal server error|No Content|
|**default**|Unexpected error|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Security

|Type|Name|
|---|---|
|**apiKey**|**[Bearer](security.md#bearer)**|


#### Example HTTP request

##### Request path
```
/dataSets
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
  "requestDataSource" : "string"
}
```


##### Request body
```
json :
{
  "connectorId" : "string",
  "connectionId" : "string",
  "name" : "string",
  "description" : "string",
  "namespace" : "string",
  "tags" : {
    "string" : [ "string" ]
  },
  "statsCache" : "object",
  "lastBatchId" : "string",
  "lastBatchStatus" : "string",
  "lastSuccessfulBatch" : "string",
  "lastFailedBatch" : "string",
  "aspect" : "string",
  "observableSchema" : "object",
  "status" : "string",
  "requestStartDate" : "string",
  "editable" : true,
  "dependencies" : [ {
    "dataSetId" : "string",
    "dataSetViewId" : "string",
    "type" : "string"
  } ],
  "fields" : [ {
    "dataType" : {
      "type" : "string",
      "precision" : 0.0,
      "scale" : 0.0,
      "subType" : {
        "type" : "string",
        "precision" : 0.0,
        "scale" : 0.0,
        "subType" : "...",
        "subFields" : "...",
        "keyType" : "string",
        "valueType" : "..."
      },
      "subFields" : "...",
      "keyType" : "string",
      "valueType" : "..."
    },
    "name" : "string",
    "definition" : "object",
    "meta" : "object",
    "dule" : "object"
  } ],
  "basePath" : "string",
  "fileDescription" : "object",
  "partitions" : [ "string" ],
  "saveStrategy" : "string",
  "schema" : "string",
  "dule" : "object",
  "dataSourceId" : 0
}
```


#### Example HTTP response

##### Response 201
```
json :
[ "string" ]
```



