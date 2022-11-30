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

Keep the other defaults if desired. And select IMPORT to start the import.

## Running the Imported Project

We should now see this:
![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import7.png?raw=true)

Assuming our connections are setup correctly - we can start executing the model. Currently each element needs to be "Prepared" and "Run" individually. There is a feature update coming to execute in batch coming soon.

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import8.png?raw=true)

Run the Prepare on all the "Landing" tasks. You will see "Creating Artifacts" and when complete, "Ready to run" will display. Go ahead and "Run" the "Landing" tasks. Depending on the size of your SAP system and the sizing of the Cloud Data Warehouse system...

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/image9.png?raw=true)

While "Landing" is loading, we can "Prepare" the "Storage" layer. Select all "Store" tasks and "Prepare". It should look like this now:

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/image10.png?raw=true)

Once the data is finished loading into the "Landing" layer.  We can "Prepare" and "Run" all the other tasks. The final state should look similar to this:

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/image11.png?raw=true)

## Start of Qlik Data Analytics Install (Orders to Cash example)

We move back into the "Analytic Service" side of the SaaS platform. 

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import12.png?raw=true)

Moving into our selected analytics space in the catalog, we need to import the three SAP Accelerator apps. 

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import13.png?raw=true)

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/image14.png?raw=true)

## SAP Extraction App (Orders to Cash)

The first app we need to adjust is the SAP Extract App. This app pulls the data from Snowflake and creates a stage/merge file in Qlik. We need to make an adjustment in the script to adjust for your Qlik SaaS setup. 

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/import15.png?raw=true)

This section will need to be adjusted for the Analytics Snowflake connection and the "Space" for said connection.
*// 📝 Step 1 - Identify what library connection will be used to talk to the datamart source
LIB CONNECT TO 'SAP_QCDI:Snowflake QCDI V2';*

In the next section, need to adjust for "Space" name and QVD storage (default is DataFiles). Also, need to set the Database and Schema from the Qlik Cloud Integration DataMart output (orders2cash_dm is the default).
/*/ 📝 Step 2 - Identify what connection and path will be used to store the raw data QVD's and what vendor we are pulling for
SET vStorageConnection = 'SAP_QCDI:DataFiles/';
// Vendor names can be anything. QCDI represents the expected base model. If base modifications are required then it can be changed to be vendor specific
SET vVendor = 'QCDI';
Set vDatabase = 'SAP_ACCEL_IMPORT';
Set vSchema = 'orders2cash_dm';*

Once those changes are made, run the Load Data option. The merge/stage files will be automatically created in Qlik SaaS.

## SAP Transform App (Orders to Cash)

Similarly in the SAP Transform App we need to update locations/spaces. Just make sure the "Space" and "DataFiles" setting are correct, and everything else will run automatically. This app turns the 2-D datamart data into the multidimensional construct Qlik uses for complex calculations and data mapppings.

*SET vRawStorageConnection = 'SAP_QCDI:DataFiles/QCDI_';
SET vStage2StorageConnection = 'SAP_QCDI:DataFiles/QCDI_';*

## SAP Analytics App (Orders to Cash)

This is the final app and what the users will consume. 

![enter image description here](https://github.com/Qlik-PE/Qlik_SaaS_SAP_Accelerators/blob/main/images/Slide10.png?raw=true)

We need to update locations/spaces. Just make sure the "Space" and "DataFiles" setting are correct, and everything else will run automatically.

*SET vStage2StorageConnection = 'SAP_QCDI:DataFiles/QCDI_';*

Repeat the Qllik Analytics steps above for the other two subject areas **Financial Analytics** and **Inventory Management.**
