### Usage Log Service
This service is used by the UPoint Mobile app to log usage and business events. This service will collect the necessary elements for logging and then make a call to UMA logic layer through ASG in order to do the server side logging. This service does not support logging through NextGen. Logging through UMA is a temporary solution until the UPN logging framework supports the business requirements for logging usage and business events.

### Introduction
 When the channel/usagelog service is called directly from UPoint Mobile Application, it can create a usage.log or a business event.log depending on the parameters passed.

	- Usage.log - Logs all mobile app screen views for a person.
	- Event.log for HM_TOOL_USAGE - Logs the usage of a tool(s) for which a person is eligible. Find a Doctor is the only tool supported to date.See openapi.yaml for details on required parameters for logging.


### Service Owner
 Mike Pozen <mike.pozen@alight.com>; Jeff Baisden <jeff.baisden@alight.com>; Melissa Johnson <melissa.johnson.2@alight.com>;
 
### Development Team
Adit Majmudar <adit.majmudar@alight.com >; Uday Chudasama <uday.chudasama.2@alight.com>; Sandip Patel <sandip.patel.2@alight.com>; Vinay Solanki <vinay.solanki@alight.com>; Rohit Parmar <rohit.parmar@alight.com>;
 
### Technical Contact: 
 Jeff Baisden <jeff.baisden@alight.com>;   Tarun Malhotra <tarun.malhotra.2@alight.com>;  Adit Majmudar <adit.majmudar@alight.com>;

### Service Dependencies:
 - **channel-widgetconfigurations service** :   [https://bitbucket.alight.com/projects/UPN/repos/load-properties-service/browse](https://bitbucket.alight.com/projects/UPN/repos/load-properties-service/browse)
 - **channel-cache-clientconfigurations**  :[https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse](https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse)

### Backend Systems Interacted With: 
 - UPoint Configuration
 - UCE
 
### Angular Widgets Calling This Service: 
 This service is called from mobile application (Xamarin forms). The project for App is:  https://bitbucket.alight.com/projects/DIL/repos/upointappv2/browse
 

### New Relic Dashboard
 - Prod: https://rpm.newrelic.com/accounts/752702/applications/120063341

### Monitoring Alerts Specification
- **Kibana logs**
 
	 - DEV/QA : https://l4dvitap7487.hewitt.com:5601/app/kibana
	 - QC/PROD : https://kb.alight.com:5601/app/kibana
 
### Support Contacts 
 UPoint Support (CTS Portal Support)

### JIRA Type
https://jira.alight.com/projects/MBL/summary

 
### Service Failure Criticality: **Major**

### OpenAPI Spec: 
https://bitbucket.alight.com/projects/UPN/repos/channel-usagelog-service/browse/api/openapi.yaml
 
## Service Maps
### Service End-Point details
 - **Path Mapping**: /api/channel/usagelog/uxpageusage - POST Mapping <br> 
 - The **/uxpageusage**  Thie endpoint Generate logs for events like click and page render.
  Obtain  alightRequestHeader and alightPersonSessionTokenfrom this API
  https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md 
  Details on the request payload as well as valid responses are in the OpenAPI Specification at following location:
  https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader :  {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::f02e863a-f1b1-47d1-b41e-5c3157a571ab_2020-08-24-06.11.02.400000::sessionCreatedTimestamp::2020-08-24-06.11.02.400000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : eyJhbGciOiJSUzI1NiJ9.eyJicm9rZXJVc2VySWQi****************************...
	```
	- Query Parameter
	```
			NA		
	```
	- Request Body
	```
			{

			"ActionTarget": "DC - Savings Plan Main",

			"ActionType": "Internal Link Card Click",

			"Domain": "DC",

			"Message": "Title: Investment Mix",

			"Process": "Change Contributions",

			"ProcessDetail": "Change Contributions - Confirmation",

			"UserAction": "Click"

			}
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
		   {"status":"OK"}
	```
	
 - **Path Mapping**: /api/channel/usagelog/uxpageusage/public - POST Mapping <br> 
 - The **/uxpageusage/public** endpoint Generate logs for mobile screen's events like click and page render for AlightOne MobileApp services. 
 Obtain alightRequestHeader and alightPersonSessionToken from this API
 https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
 Details on the request payload as well as valid responses are in the OpenAPI Specification at following location:
 https://upoint-dv.alight.com/specmgmt/#/
 
	- Request Header
	```
			 **alightRequestHeader :  {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::f02e863a-f1b1-47d1-b41e-5c3157a571ab_2020-08-24-06.11.02.400000::sessionCreatedTimestamp::2020-08-24-06.11.02.400000::srcPlatform::upointmbl"}
			 **alightPersonSessionToken : eyJhbGciOiJSUzI1NiJ9.eyJicm9rZXJVc2VySWQi****************************...
	```
	- Query Parameter
	```
			NA
	```
	- Request Body
	```
			{

			"ActionTarget": "DC - Savings Plan Main",

			"ActionType": "Internal Link Card Click",

			"Domain": "DC",

			"Message": "Title: Investment Mix",

			"Process": "Change Contributions",

			"ProcessDetail": "Change Contributions - Confirmation",

			"UserAction": "Click"

			}
	```	
	- Response Header
	```
	 		NA
	```
	- Response Body
	``` 
			Success
	  ``` 
	  
 - **Path Mapping**: /api/channel/usagelog/businessevent - POST Mapping<br> 
 - The **/businessevent** This endpoint generate logs for business event log. 
Obtain  alightRequestHeader and alightPersonSessionToken from this API
https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
https://upoint-dv.alight.com/specmgmt/#/
	-  Request Header
	```
			  **alightRequestHeader :  {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::f02e863a-f1b1-47d1-b41e-5c3157a571ab_2020-08-24-06.11.02.400000::sessionCreatedTimestamp::2020-08-24-06.11.02.400000::srcPlatform::upointmbl"}
			  **alightPersonSessionToken : eyJhbGciOiJSUzI1NiJ9.eyJicm9rZXJVc2VySWQi****************************...		
	```

	-  Query Parameter
	 ```
			    NA
	 ```
	 - Request Body
	 ```
				 {
	
				"businessEventId":"HM_TOOL_ELIGIBILITY",

				"reportingFields": {

				"ACT_REF_NMBR_ID": "0",

				"EVNT_CLSN_CD": "INQRY",

				"EVNT_SMRY_CD": "INQRY",

				"ACT_EFDT": "2020/12/31",

				"TOOL_CD_TO_PLAN_ID": "GEO,1000",

				"CGE_PLAN_ID_IND": "0"

				}

				}	
	 ```	
	 - Response Header
	  ```
			    NA
	  ```
	-  Response Body
	 ```
			   {"status":"OK"}
	 ```
  
