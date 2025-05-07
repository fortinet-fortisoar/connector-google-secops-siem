## About the connector
Google Security Operations (SecOps) is a cloud-native security information and event management (SIEM) platform built on Google Cloud's infrastructure. It is designed to help enterprises detect, investigate, and respond to cybersecurity threats at scale and speed. By normalizing, indexing, and analyzing vast amounts of security telemetry, Google SecOps provides real-time insights into potential risks, enabling security teams to act swiftly and effectively.
<p>This document provides information about the Google SecOps SIEM Connector, which facilitates automated interactions, with a Google SecOps SIEM server using FortiSOAR&trade; playbooks. Add the Google SecOps SIEM Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Google SecOps SIEM.</p>

### Version information

Connector Version: 1.0.0

Contributor: Daehyeob Kim

Authored By: Fortinet CSE

Certified: No

## Installing the connector
<p>From FortiSOAR&trade; 7.0.0 onwards, use the <strong>Connector Store</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.<br>You can also use the following <code>yum</code> command as a root user to install connectors from an SSH session:</p>
`yum install cyops-connector-google-secops-siem`

## Prerequisites to configuring the connector
- You must have the URL of Google SecOps SIEM server to which you will connect and perform automated operations and credentials to access that server.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Google SecOps SIEM server.

## Minimum Permissions Required
- N/A

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Google SecOps SIEM</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations&nbsp;</strong> tab enter the required configuration details:&nbsp;</p>
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Project ID<br></td><td>Specify the ID of the project to access the Google SecOps SIEM endpoint to which you will connect and perform the automated operations.<br>
<tr><td>Instance ID<br></td><td>Specify the ID of the instance to access the Google SecOps SIEM endpoint to which you will connect and perform the automated operations.<br>
<tr><td>Regional Endpoint<br></td><td>Specify the regional endpoint to access the Google SecOps SIEM endpoint to which you will connect and perform the automated operations.<br>
<tr><td>Service Account JSON File<br></td><td>Specify the JSON file of the service account to access the Google SecOps SIEM endpoint to which you will connect and perform the automated operations.<br>
<tr><td>Verify SSL<br></td><td>Specifies whether the SSL certificate for the server is to be verified or not. <br/>By default, this option is set as True.<br></td></tr>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function<br></th><th>Description<br></th><th>Annotation and Category<br></th></tr></thead><tbody><tr><td>Check Health<br></td><td>This operation will perform a health check on the connector to ensure it is functioning properly.<br></td><td> <br/><br></td></tr>
<tr><td>Execute API Endpoint<br></td><td>Sends an API request to an API endpoint based on specified HTTP method, endpoint, and other input parameters that you have specified, enabling flexible API interactions tailored to user needs.<br></td><td>execute_api_endpoint <br/><br></td></tr>
<tr><td>Get Legacy Alert<br></td><td>Retrieves a legacy alert from Google SecOps SIEM based on the input parameters that you have specified.<br></td><td>legacygetalert <br/>Investigation<br></td></tr>
<tr><td>Fetch Legacy Alerts View<br></td><td>Retrieves a legacy alerts view from Google SecOps SIEM based on the input parameters that you have specified.<br></td><td>legacyfetchalertsview <br/>Investigation<br></td></tr>
<tr><td>UDM Search<br></td><td>It enables customers to programmatically complete a UDM Search query and retrieve matches.<br></td><td>udm_search <br/>Investigation<br></td></tr>
</tbody></table>

### operation: Check Health
#### Input parameters
None.
#### Output

 No output schema is available at this time.
### operation: Execute API Endpoint
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>API Domain<br></td><td>Select an API domain for the request. You can select from the following options: backstory or chronicle.<br>
</td></tr><tr><td>Method<br></td><td>Select an HTTP action for the request. You can select from the following options:  

DELETE 

GET 

PATCH 

POST 

PUT 

HEAD 

OPTIONS 

TRACE<br>
</td></tr><tr><td>API Endpoint<br></td><td>Specify the target API URL path for the request. For example, if the website is https://example.com and URL path is https://example.com/images/pic.jpg, the endpoint would be /images/pic.jpg.<br>
</td></tr><tr><td>Headers<br></td><td>Specify the headers for the request.<br>
</td></tr><tr><td>Body<br></td><td>Specify any optional parameters to add to the URL and refine the request.<br>
</td></tr><tr><td>Query Parameters<br></td><td>Specify data, as JSON, to be sent as the request payload.<br>
</td></tr></tbody></table>

#### Output

 No output schema is available at this time.
### operation: Get Legacy Alert
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Alert ID<br></td><td>Specify the alert ID based on which you want to retrieve legacy alert from Google SecOps SIEM.<br>
</td></tr><tr><td>Include Detections<br></td><td>Select this checkbox, i.e., set it to True to include detections for legacy alert.By default, this is set as False.<br>
</td></tr></tbody></table>

#### Output

 No output schema is available at this time.
### operation: Fetch Legacy Alerts View
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Base Line Query<br></td><td>Specify the base line query to search within legacy alerts.<br>
</td></tr><tr><td>StartTime<br></td><td>Specify the date and time from when to search legacy alerts view on Google SecOps SIEM.<br>
</td></tr><tr><td>EndTime<br></td><td>Specify the date and time till when to search legacy alerts view on Google SecOps SIEM.<br>
</td></tr><tr><td>Limit<br></td><td>Specify the maximum number of results this operation should return, per page, in the response.<br>
</td></tr></tbody></table>

#### Output

 No output schema is available at this time.
### operation: UDM Search
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>UDM Type<br></td><td>UDM search query.
link: https://cloud.google.com/chronicle/docs/reference/search-api#udmsearch<br>
</td></tr><tr><td>Query<br></td><td>Specify the UDM search query.
link: https://cloud.google.com/chronicle/docs/reference/search-api#udmsearch<br>
</td></tr><tr><td>StartTime<br></td><td>Specify the date and time from when to search legacy alerts view on Google SecOps SIEM.<br>
</td></tr><tr><td>EndTime<br></td><td>Specify the date and time till when to search legacy alerts view on Google SecOps SIEM.<br>
</td></tr><tr><td>Limit<br></td><td>Specify the maximum number of results this operation should return, per page, in the response. Must be less than or equal to 10,000.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
## Included playbooks
The `Sample - Googel SecOps SIEM - 1.0.0` playbook collection comes bundled with the Google SecOps SIEM connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR<sup>TM</sup> after importing the Google SecOps SIEM connector.

- Execute API Endpoint
- Fetch Legacy Alerts View
- Get Legacy Alert
- Google SecOps SIEM > Create
- Google SecOps SIEM > Fetch
- Google SecOps SIEM > Ingest
- UDM Search

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection, since the sample playbook collection gets deleted during connector upgrade and delete.
## Data Ingestion Support
Use the Data Ingestion Wizard to easily ingest data into FortiSOAR&trade; by pulling events/alerts/incidents, based on the requirement.

**TODO:** provide the list of steps to configure the ingestion with the screen shots and limitations if any in this section.