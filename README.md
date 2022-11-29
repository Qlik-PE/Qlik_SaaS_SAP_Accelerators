# **Qlik SaaS SAP Accelerators**

The SAP Accelerators are quick start templated designed against a STANDARD SAP IDES install to demonstrate the art of the possible for extraction, transformation, and analytics using the Qlik SaaS Platform which includes both Qlik Cloud Data Integration and Qlik Cloud Analytics.

![SAP Accelerators Architecture](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/Slide2.png?raw=true)

## Description:
The SAP Accelerators take RAW SAP data from ECC or HANA and turn into Analytics ready data with Qlik SaaS Analytics using prebuilt dashboards.

The process extracts the data required for three initial SAP use cases 
 - Orders to Cash 
 - Inventory Management 
 - Financial Analytics

The extracted data is then transformed using the Qlik Cloud Data Integration engine into Analytic ready data marts. The process also turns RAW shorthand german codes into readable business terms and consolidates the dimensional data into reusable and shared assets for the various SAP Fact data. That end result is then cataloged and fed into the Qlik SaaS Analytics layer for consumption by business users.

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/Slide3.png?raw=true)

## Prerequisite Configuration Instructions :

First - a guide of the Qlik Cloud Data Integration process:
[Qlik Cloud Data Integration Overview - YouTube](https://youtu.be/bdVQa5LKmvE)

We will need to configure a few things first ([Link to Help Guide)](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/DataIntegration/Introduction/Data-project-export-import.htm):

 - We will need to establish a **Cloud Database Platform** and **Database Name** to use for the SAP Accelerators (this example will use Snowflake, and a database called "SAP_Accel_Import"
 - Supported Cloud Database platforms include
	 - Databricks (all clouds)
	 - Snowflake (all clouds)
	 - Google Big Query
	 - Azure Synapse
	 - Qlik Cloud (QVD's on S3) 
 - This connection can be setup during import or ahead of time, but the database name to be used must already be created. ([Instructions here](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/DataIntegration/TargetConnections/data-project-connections.htm))
 - The Data Movement Gateway will also need to be installed and configured to connect to the SAP system used in the accelerators.  ([Instructions Here](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/Gateways/replication-gateway.htm))![enter image description here](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Resources/Images/data-movement-gateway_architecture_v2.png)

**Once the above prerequisites have been met - we can proceed with importing the SAP Accelerator content**

## Importing the SAP Accelerators - Qlik Cloud Data Integration 

From inside your Qlik SaaS system, select Data Services
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/dataservices.png?raw=true)

Click the "Add New" button in the top right corner, select "Import Data Project"
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import1.png?raw=true)

Using the JSON file from the GitHub ([here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/raw/main/Snowflake/SAP%20Accelerators%20V2_Snowflake_2022-11-22.json)) drag or browse and add to the Import Data Project window and give it a name.
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import2.png?raw=true)

Choose the "Space" you want to Import into - make sure it is a "Space" that the Data Movement Gateway can access:
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import3.png?raw=true)

Choose the Data platform:
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import4.png?raw=true)
and the data connection:
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import5.png?raw=true)
Next map the SAP Extractor Connector to the Source Connection, this connection should have been setup during the Gateway setup if not instructions here ([SAP Extractor Setup](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/DataIntegration/SourcesConnections/SAP-Extractor/SAP-Extractor-source.htm)):
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import6.png?raw=true)
Keep the other defaults if desired.
