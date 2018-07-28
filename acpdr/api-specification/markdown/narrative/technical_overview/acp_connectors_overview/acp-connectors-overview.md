# ACP Data Connectors - Technical Overview


Adobe provides multiple connectors to ingest data from your data sources to the Adobe Cloud Platform (ACP), including Microsoft Dynamics 365, Salesforce, Amazon S3, and Azure Blob. 

<add> 

Data is ingested through the ACP user interface or by employing RESTful APIs. 

<what APIs are we using here? Catalog, >

## New API Features

A new set of ACP Connector APIs provide these new features, allowing you to:

* Call a single Platform Service rather than multiple services.
* Build applications on the platform using a minimal set of APIs.
* Provide consistency by using all connector types.
* Employ credentials before allowing data to persist. 

## Design
The Adobe Cloud Platform employs various components during data ingestion from third-party source through the Adobe Platform data connectors:

Platform UI/Client
connectors-rest APIs
Platform Pipeline
Connector Observer
Azure Data Factory
Azure Event Hub
Batch tracker
Data tracker

## Requirements
* Files in the source location should adhere to the same schema or an error will be returned.
* Configure new connection for files with different schema and provide new folder location.
* User token will be used to access connectors APIs. User token can be fetched via https://console.adobe.io - https://www.adobe.io/apis/cloudplatform/console/authentication/gettingstarted.html or use IMS API - https://ims-na1-stg1.adobelogin.com/ims/login/v1/token?client_id=<YourIMSClientId>&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext&username=<userName>&password=<password>