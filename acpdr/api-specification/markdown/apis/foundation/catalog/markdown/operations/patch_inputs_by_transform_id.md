
<a name="patch_inputs_by_transform_id"></a>
### Updates inputs attributes of an existing transform.
```
PATCH /transforms/{id}/inputs
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**if-match**  <br>*optional*|Set to verify the right version of document to be modified by matching the updated date.|string|
|**Header**|**x-api-key**  <br>*required*|The API key belonging to the calling client.|string|
|**Header**|**x-gw-ims-org-id**  <br>*required*|The owning IMS organization identifier.|string|
|**Path**|**id**  <br>*required*|Object ID|string|


#### Body parameter
Array[ {"dataSet": "@/dataSets/dataSetId"}]

*Name* : inputs  
*Flags* : required  
*Type* : < [inputs](#patch_inputs_by_transform_id-inputs) > array

<a name="patch_inputs_by_transform_id-inputs"></a>
**inputs**

|Name|Description|Schema|
|---|---|---|
|**dataSet**  <br>*optional*|**Example** : `"string"`|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Array[ @/transforms/transformId ]|< string > array|
|**400**|Bad request|No Content|
|**403**|Forbidden|No Content|
|**404**|Not found|No Content|
|**500**|Internal server error|No Content|
|**default**|Unexpected error|No Content|


#### Consumes

* `application/json`
* `application/json-patch+json`


#### Security

|Type|Name|
|---|---|
|**apiKey**|**[Bearer](security.md#bearer)**|


#### Example HTTP request

##### Request path
```
/transforms/string/inputs
```


##### Request header
```
json :
"string"
```


##### Request body
```
json :
[ "object" ]
```


#### Example HTTP response

##### Response 200
```
json :
[ "string" ]
```



