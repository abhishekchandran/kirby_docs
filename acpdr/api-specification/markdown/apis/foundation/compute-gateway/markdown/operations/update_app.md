
<a name="update_app"></a>
### Update Application
```
PUT /data/foundation/compute/apps/{appID}
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-api-key**  <br>*required*|The API key belonging to the calling client.|string|
|**Header**|**x-request-id**  <br>*optional*|A unique id generated by Adobe.io.|string|
|**Path**|**appID**  <br>*required*|App ID|string|


#### Body parameter
App Request

*Name* : body  
*Flags* : required  
*Type* : [AppDef](../definitions/AppDef.md#appdef)


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**202**|Application successfully submitted for update|No Content|
|**401**|Unauthorized access|No Content|
|**404**|App does not exist|No Content|
|**414**|URI length exceeds 2000 characters limit|No Content|
|**422**|Input validation failure|No Content|
|**503**|Application creation failed|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* ComputeApplications


#### Example HTTP request

##### Request path
```
/data/foundation/compute/apps/4b3c4fae-212c-404f-9565-9b3fa0a9cb4f
```


##### Request header
```
json :
"string"
```


##### Request body
```
json :
{
  "name" : "SparkPi",
  "sparkConf" : {
    "string" : "string"
  },
  "envVars" : {
    "string" : "string"
  },
  "className" : "org.apache.spark.examples.SparkPi",
  "jar" : "https://aphatakstorageeast.blob.core.windows.net/campaign/spark-examples_2.11-2.1.0.jar",
  "args" : "[3]",
  "instances" : 1,
  "driverMemory" : 1024,
  "driverCores" : 1,
  "executorMemory" : 1024,
  "executorCores" : 1,
  "numExecutors" : 1,
  "tags" : {
    "string" : "string"
  },
  "clusterId" : "38b60713-68df-4b34-9030-bb85a5447bcd",
  "userId" : "ACP@Adobe.com",
  "cmd" : "string",
  "ports" : [ {
    "port" : 0,
    "sparkUI" : true,
    "healthCheck" : {
      "gracePeriodSeconds" : 0,
      "intervalSeconds" : 0,
      "maxConsecutiveFailures" : 0,
      "path" : "string",
      "protocol" : "string",
      "timeoutSeconds" : 0,
      "delaySeconds" : 0,
      "ignoreHttp1xx" : true
    }
  } ]
}
```


