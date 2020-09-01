### Person Defined Contribution Service
   -  This service is designed specifically for the DC Mobile App only and will provide the details about investment mix, contributions and ROR charts.	
	
### Service Owner
 Uday Chudasama <uday.chudasama.2@alight.com>; Sandip Patel <sandip.patel.2@alight.com>;  Adit Majmudar <adit.majmudar@alight.com >;  Tarun Malhotra <tarun.malhotra.2@alight.com>; Mukund Mohan Jha <mukund.mohan.jha@alight.com>;
 
### Development Team
Adit Majmudar <adit.majmudar@alight.com >; Uday Chudasama <uday.chudasama.2@alight.com>; Sandip Patel <sandip.patel.2@alight.com>; Vinay Solanki <vinay.solanki@alight.com>; Rohit Parmar <rohit.parmar@alight.com>;
 
### Technical Contact: 
 Jeff Baisden <jeff.baisden@alight.com>;   Tarun Malhotra <tarun.malhotra.2@alight.com>;  Adit Majmudar <adit.majmudar@alight.com>;



### Service Dependencies:

 - **channel-widgetconfigurations service** :   [https://bitbucket.alight.com/projects/UPN/repos/load-properties-service/browse](https://bitbucket.alight.com/projects/UPN/repos/load-properties-service/browse)
 - **channel-cache-clientconfigurations**  :[https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse](https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse)
  - **Balance Chart :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/dcbalancechartmobilewidget.json
 - **Investment Mix :** https://bitbucket.alight.com/projects/UPN/repos/channel-definedcontributionmobilewidgets-service/browse/src/main/resources/configset/dcinvestmentmixmobilewidget.json
 - **Contribution :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/dccontributionmobilewidget.json
 - **Boost (Landing Page) :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/boostdcmobilewidget.json
 - **Boost (Success Page) :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/boostdcpostmobilewidget.json
 - **Change contribution (Entire flow except success Page) :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/dcchgctrbmobilewidget.json
 - **Change Contribution (Success Page) :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/dcchgctrbpostmobilewidget.json
 - **Quick Enrollment (Landing Page) :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/quickenrollmentmobilewidget.json
 - **Quick Enrollment (Success Page) :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/quickenrollmentpostmobilewidget.json
 - **Monthly Retirement Projection :** https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse/src/main/resources/configset/monthlyretirementincomeprojection.json
 - **Fund Reallocation and Fund Transfer (Common page):** https://bitbucket.alight.com/projects/UPN/repos/channel-definedcontributionmobilewidgets-service/browse/src/main/resources/configset/dcchangeinvestmentwidget.json
 - **Fund Reallocation:** https://bitbucket.alight.com/projects/UPN/repos/channel-definedcontributionmobilewidgets-service/browse/src/main/resources/configset/fundreallocationwidget.json
 - **FundTransfer**: https://bitbucket.alight.com/projects/UPN/repos/channel-definedcontributionmobilewidgets-service/browse/src/main/resources/configset/directfundtransfer.json
 
  
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

https://bitbucket.alight.com/projects/UPN/repos/channel-definedcontributionmobilewidgets-service/browse/api/openapi.yaml
 
## Service Maps
### Service End-Point details
 - **Path Mapping**: /api/channel/definedcontributionmobilewidgets/dcBalanceChartMobileWidget?planId=plan_Id - GET Mapping <br> 
 - The **/dcBalanceChartMobileWidget?planId=planId** endpoint return mobile application will have plan summary page  where participant will
   be able to see YTD ROR Balance chart, current balance and gain/loss details.  
 Obtain alightRequestHeader and alightPersonSessionToken from this API
 https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			1) planId ::: 10
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
				"title": "Retirement & Pension Plan contributions",
				"asOfDateText": "As of Aug 21, 2020",
				"currentBalanceLabel": "Current Balance",
				"currentBalance": "$0.88",
				"loanBalanceExcludeText": "",
				"balanceChartLabel": "2020 Performance",
				"performanceChart": [
					{
						"rateOfReturnEndDate": "2020-01-06",
						"rateOfReturnInPercent": "0.00%",
						"rateOfReturnInPercentValue": 0.0
					},
					{
						"rateOfReturnEndDate": "2020-01-13",
						"rateOfReturnInPercent": "1.00%",
						"rateOfReturnInPercentValue": 1.0
					},
					{
						"rateOfReturnEndDate": "2020-01-21",
						"rateOfReturnInPercent": "1.00%",
						"rateOfReturnInPercentValue": 1.0
					},
					{
						"rateOfReturnEndDate": "2020-01-27",
						"rateOfReturnInPercent": "-2.00%",
						"rateOfReturnInPercentValue": -2.0
					},
					{
						"rateOfReturnEndDate": "2020-02-03",
						"rateOfReturnInPercent": "-2.00%",
						"rateOfReturnInPercentValue": -2.0
					},
					{
						"rateOfReturnEndDate": "2020-02-10",
						"rateOfReturnInPercent": "-1.00%",
						"rateOfReturnInPercentValue": -1.0
					},
					{
						"rateOfReturnEndDate": "2020-02-18",
						"rateOfReturnInPercent": "-1.00%",
						"rateOfReturnInPercentValue": -1.0
					},
					{
						"rateOfReturnEndDate": "2020-02-24",
						"rateOfReturnInPercent": "-5.00%",
						"rateOfReturnInPercentValue": -5.0
					},
					{
						"rateOfReturnEndDate": "2020-03-02",
						"rateOfReturnInPercent": "-12.00%",
						"rateOfReturnInPercentValue": -12.0
					},
					{
						"rateOfReturnEndDate": "2020-03-09",
						"rateOfReturnInPercent": "-25.00%",
						"rateOfReturnInPercentValue": -25.0
					},
					{
						"rateOfReturnEndDate": "2020-03-16",
						"rateOfReturnInPercent": "-40.00%",
						"rateOfReturnInPercentValue": -40.0
					},
					{
						"rateOfReturnEndDate": "2020-03-23",
						"rateOfReturnInPercent": "-45.00%",
						"rateOfReturnInPercentValue": -45.0
					},
					{
						"rateOfReturnEndDate": "2020-03-30",
						"rateOfReturnInPercent": "-36.00%",
						"rateOfReturnInPercentValue": -36.0
					},
					{
						"rateOfReturnEndDate": "2020-04-06",
						"rateOfReturnInPercent": "-38.00%",
						"rateOfReturnInPercentValue": -38.0
					},
					{
						"rateOfReturnEndDate": "2020-04-13",
						"rateOfReturnInPercent": "-32.00%",
						"rateOfReturnInPercentValue": -32.0
					},
					{
						"rateOfReturnEndDate": "2020-04-20",
						"rateOfReturnInPercent": "-34.00%",
						"rateOfReturnInPercentValue": -34.0
					},
					{
						"rateOfReturnEndDate": "2020-04-27",
						"rateOfReturnInPercent": "-30.00%",
						"rateOfReturnInPercentValue": -30.0
					},
					{
						"rateOfReturnEndDate": "2020-05-04",
						"rateOfReturnInPercent": "-29.00%",
						"rateOfReturnInPercentValue": -29.0
					},
					{
						"rateOfReturnEndDate": "2020-05-11",
						"rateOfReturnInPercent": "-27.00%",
						"rateOfReturnInPercentValue": -27.0
					},
					{
						"rateOfReturnEndDate": "2020-05-18",
						"rateOfReturnInPercent": "-26.00%",
						"rateOfReturnInPercentValue": -26.0
					},
					{
						"rateOfReturnEndDate": "2020-05-26",
						"rateOfReturnInPercent": "-21.00%",
						"rateOfReturnInPercentValue": -21.0
					},
					{
						"rateOfReturnEndDate": "2020-06-01",
						"rateOfReturnInPercent": "-20.00%",
						"rateOfReturnInPercentValue": -20.0
					},
					{
						"rateOfReturnEndDate": "2020-06-08",
						"rateOfReturnInPercent": "-10.00%",
						"rateOfReturnInPercentValue": -10.0
					},
					{
						"rateOfReturnEndDate": "2020-06-15",
						"rateOfReturnInPercent": "-18.00%",
						"rateOfReturnInPercentValue": -18.0
					},
					{
						"rateOfReturnEndDate": "2020-06-22",
						"rateOfReturnInPercent": "-18.00%",
						"rateOfReturnInPercentValue": -18.0
					},
					{
						"rateOfReturnEndDate": "2020-06-29",
						"rateOfReturnInPercent": "-18.00%",
						"rateOfReturnInPercentValue": -18.0
					},
					{
						"rateOfReturnEndDate": "2020-07-06",
						"rateOfReturnInPercent": "-17.00%",
						"rateOfReturnInPercentValue": -17.0
					},
					{
						"rateOfReturnEndDate": "2020-07-13",
						"rateOfReturnInPercent": "-19.00%",
						"rateOfReturnInPercentValue": -19.0
					},
					{
						"rateOfReturnEndDate": "2020-07-20",
						"rateOfReturnInPercent": "-15.00%",
						"rateOfReturnInPercentValue": -15.0
					},
					{
						"rateOfReturnEndDate": "2020-07-27",
						"rateOfReturnInPercent": "-14.00%",
						"rateOfReturnInPercentValue": -14.0
					},
					{
						"rateOfReturnEndDate": "2020-08-03",
						"rateOfReturnInPercent": "-13.00%",
						"rateOfReturnInPercentValue": -13.0
					},
					{
						"rateOfReturnEndDate": "2020-08-10",
						"rateOfReturnInPercent": "-10.00%",
						"rateOfReturnInPercentValue": -10.0
					},
					{
						"rateOfReturnEndDate": "2020-08-17",
						"rateOfReturnInPercent": "-10.00%",
						"rateOfReturnInPercentValue": -10.0
					},
					{
						"rateOfReturnEndDate": "2020-08-21",
						"rateOfReturnInPercent": "-12.00%",
						"rateOfReturnInPercentValue": -12.0
					}
				],
				"rateOfReturnDetails": {
					"text": "Rate of Return",
					"value": "-12.00%",
					"color": "#c05454"
				},
				"gainLossDetails": {
					"text": "Loss",
					"value": "-$0.12",
					"color": "#c05454"
				},
				"cards": [
					{
						"cardType": "investmentMixButton",
						"label": "Investment Mix",
						"description": "",
						"displayButton": true,
						"linkType": "app",
						"linkURL": ""
					},
					{
						"cardType": "contributionButton",
						"label": "Contributions",
						"description": "",
						"displayButton": true,
						"linkType": "app",
						"linkURL": ""
					},
					{
						"cardType": "brokerageLink",
						"label": "Set Up a Self-Directed Brokerage Account",
						"description": "",
						"displayButton": true,
						"linkType": "sso",
						"linkURL": "https://api.int.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_HFS_DTL_050&domain=DC"
					},
					{
						"cardType": "boostYourRetirement",
						"label": "Boost Your Retirement",
						"description": "Start saving a little more now.",
						"displayButton": true,
						"linkType": "app",
						"linkURL": "",
						"buttonType": "saveMore"
					},
					{
						"cardType": "wealthspark",
						"label": "Visit Your WealthSpark<sup>TM</sup> Dashboard",
						"description": "",
						"displayButton": true,
						"androidPackage": "com.alight.wealthspark",
						"androidAppUrl": "market://details?id=com.alight.wealthspark",
						"iosUrlSchema": "wealthspark://",
						"iosAppUrl": "itms-apps://itunes.apple.com/us/app/id1450444046"
					}
				],
				"remainingLoanDetail": {
					"text": "Remaining Loan Balance",
					"display": false,
					"loanAmount": "$0.00",
					"color": "#272f39"
				}
			} 
	```
 - **Path Mapping**:  /api/channel/definedcontributionmobilewidgets/dcContributionMobileWidget?planId={{dcPlanId}} - GET Mapping <br> 
 - The **/dcContributionMobileWidget?planId=planId**  endpoint return mobile application will have contribution page with 2 sets of
        information that is Donut chart of Person Defined YTD contributions and Contribution Strategy sources.
 Obtain alightRequestHeader and alightPersonSessionToken from this API
 https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			1) planId ::: 10
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
			"contributionsTitle": "Contributions",
			"contributionStrategy": {
				"tabTitle": "Retire Savings1 800 Strategy",
				"planTitle": "Retire Savings1 800 Contributions",
				"asOfDate": "as of Sep 30, 2018",
				"payCheckDetails": {
					"frequency": "per paycheck (estimated)",
					"amount": "$2.88",
					"detailsPage": {
						"footnote": {
							"title": "Estimated Paycheck Deduction",
							"asOfDate": "as of Sep 30, 2018",
							"amount": "$2.88",
							"frequency": "per paycheck",
							"text": "This is an estimated amount that will be deducted from each paycheck, based on your contribution choices and your current pay information. Any changes to your pay information or your contribution choices will impact your contribution amount."
						}
					}
				},
				"contributionSources": [
					{
						"title": "AR-Before-Tax Contribution 9Q",
						"cardType": "BT",
						"value": "3%",
						"sourceText": "(will increase by 2% in January 2019)",
						"detailsPage": {
							"title": "AR-Before-Tax Contribution 9Q",
							"currentContributionText": "Current Contribution",
							"value": "3%",
							"frequency": "per paycheck",
							"text": "Automatic Annual Increase",
							"sourceText": "(occurs every January until ending rate is reached)",
							"asOfDate": "as of Sep 30, 2018",
							"rates": [
								{
									"title": "Starting Rate",
									"amount": "3%"
								},
								{
									"title": "Annual Increase",
									"amount": "2%"
								},
								{
									"title": "Ending Rate",
									"amount": "10%"
								}
							]
						}
					}
				],
				"companyMatch": {
					"title": "Company Match",
					"frequency": "per paycheck (estimated)",
					"amount": "$51.92",
					"fullMatch": false,
					"sourceText": "You're not getting full company match.",
					"colorCode": "#f12f00",
					"detailsPage": {
						"title": "Premier Company Match",
						"asOfDate": "as of Sep 30, 2018",
						"matchText": "$1.00 for every dollar that you contribute to the plan, up to $0.00 of your pay.",
						"sourceText": "You're not getting full company match.",
						"fullMatch": false,
						"colorCode": "#f12f00",
						"fullText": "Increase your contribution to get up to <b> $51.92 more</b> per paycheck from Premier Company.",
						"amount": "$51.92",
						"footnote": {
							"title": "Estimated Premier Company Match",
							"asOfDate": "as of Sep 30, 2018",
							"amount": "$51.92",
							"frequency": "per paycheck",
							"text": "This is an estimated amount that the Premier Company will match, based on your contribution choices and your current pay information. Any changes to your pay information or your current contribution choices will impact the Premier Company’s contribution amount."
						}
					}
				},
				"cards": [
					{
						"btnType": "changeContribution",
						"label": "Change Contributions",
						"type": "sso",
						"linkURL": ""
					}
				]
			}
		}
	```

 - **Path Mapping**: /api/channel/definedcontributionmobilewidgets/dcInvestmentMixMobileWidget?planId={{dcPlanId}} - GET Mapping <br> 
 - The **/dcInvestmentMixMobileWidget?planId=planId** endpoint return mobile application will have investment mix page with donut chart on the asset investment done by the user based on the effective date.
Obtain alightRequestHeader and alightPersonSessionToken from this API
https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			  **alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			  **alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			1) planId ::: 10
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```		
			{
			   "investmentMixTitle":"Investment Mix",
			   "investmentMixLabel":"Current Investment Mix",
			   "investmentMixAsOfText":"as of Aug 27, 2018",
			   "investmentDetailsButton":{
				  "label":"Investment Details",
				  "displayOnUI":true,
				  "type":"sso",
				  "linkURL":"https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_PRTL_INVINQ_LINK"
			   },
			   "changeInvestmentButton":{
				  "label":"Change Investments ",
				  "displayOnUI":true,
				  "type":"sso",
				  "linkURL":"https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_PRTL_INV_INQRY_CHG_LNK"
			   },
			   "investmentMixTotalText":"Total",
			   "investmentMixTotalPercentage":"100.00%",
			   "investmentMix":[
				  {
					 "assetTitle":"GIC/StableVl",
					 "assetInvestmentAmount":6428.25,
					 "assetInvestmentPercentage":"18%",
					 "colorCode":"#3f6840"
				  },
				  {
					 "assetTitle":"LargeU.SEqty",
					 "assetInvestmentAmount":11254.25,
					 "assetInvestmentPercentage":"32%",
					 "colorCode":"#FFC530"
				  },
				  {
					 "assetTitle":"Bond",
					 "assetInvestmentAmount":2795.92,
					 "assetInvestmentPercentage":"8%",
					 "colorCode":"#005673"
				  },
				  {
					 "assetTitle":"Balanced",
					 "assetInvestmentAmount":2898.13,
					 "assetInvestmentPercentage":"8%",
					 "colorCode":"#6AAC3C"
				  },
				  {
					 "assetTitle":"Intl",
					 "assetInvestmentAmount":5990.95,
					 "assetInvestmentPercentage":"17%",
					 "colorCode":"#906200"
				  },
				  {
					 "assetTitle":"Small Cap",
					 "assetInvestmentAmount":5794.35,
					 "assetInvestmentPercentage":"17%",
					 "colorCode":"#B99AC8"
				  },
				  {
					 "assetTitle":"Stock",
					 "assetInvestmentAmount":0.0,
					 "assetInvestmentPercentage":"0%",
					 "colorCode":"#606060"
				  }
			   ],
			   "automaticRebalanceSection":{
				  "text":"",
				  "linkType":"",
				  "linkURL":"",
				  "linkText":"",
				  "displayOnUI":false
			   },
			   "professionalMgmtSection":{
				  "text":"Because you are enrolled in Professional Management, Financial Engines makes investment choices for you.",
				  "linkType":"sso",
				  "linkURL":"https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=CONTACT_US_LANDING_PAGE",
				  "linkText":"Financial Engines",
				  "displayOnUI":false
			   },
			   "managedAccountInformation": {
				  "display": true,
				  "enrolledInManagedAccountMessage": "Because you're enrolled in Professional Management, Financial Engines makes investment choices for you.",
				  "managedAccountContact": {
					 "text": "Contact Financial Engines",
					 "contactNumber": "18006015957"
				  }
			   },
				"isTransferParameterElig": true,
				"isMobileNewInvestmentMixAvailable": true,
				"isMobileMoveMoneyBetweenFundsAvailable": true,
				"hasActivityPending": true,
				"pendingActivityType": "REALLOCATION",
				"pendingActivityId": "360",
				"activityPendingData": {
					"activityPendingButtonTitle": "Your Pending Request",
					"activityPendingPageHeader": "New Investment Mix Request",
					"activityPendingPageText": "You may either cancel the pending request on the full site or wait to make a new request until the pending request completes at market close on <span class=\"ah-nowrap\">January 6, 2020</span>.",
					"activityPendingCancelButtonText": "Cancel This Request",
					"fullSuteLinkType": "sso",
					"fullSuteLinkUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_REALLOC&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
				},
				"hasInvalidAddressRestrictions": false,
				"invalidAddressMessage": {
					"invalidAddressHeaderText": "Invalid Address",
					"invalidAddressMessageText": "Correspondence to your address has been returned as undeliverable.",
					"invalidAddressFullSiteGuideText": "Visit the full site to update your address.",
					"personalInfomationLinkUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=PRTL_PRSN_INFO&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso",
					"personalInfomationLinkType": "sso"
				},
				"isUserEnrolledInManageAccount": false,
				"isUserEligForManageAccount": true,
				"managedAccountAddressMessage": {
					"managedAccountCardHeader": "Get Investment Help",
					"managedAccountCardMessage": "Contact Financial Engines at <span class =\"ah-nowrap\">1-800-601-5957</span>  and choose Investment Advice.",
					"managedAccountRestrictionHeader": "This Option Is Not Available",
					"managedAccountRestrictionMessage": "You can’t change your investments because you’re currently enrolled in professional management.",
					"callButtonText": "Call ",
					"phoneNumber": "<span class =\"ah-nowrap\">1-800-601-5957</span> "
				},
				"hasBrokerageAccount": false,
				"brokerageAccountMessage": {
					"brokeragAccountButtonText": "Work With Your Brokerage Account",
					"type": "SSO"
				}
			}
			 
	```

 - **Path Mapping**:  /api/channel/definedcontributionmobilewidgets/boostDCMobileWidget - GET Mapping <br> 
 - The **/boostDCMobileWidget** endpoint return Boost Retirement Mobile Widget.
Obtain alightRequestHeader and alightPersonSessionToken from this API
 https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location: 
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			NA
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
				"missingEmployerMatchAmount": "229.17",
				"receivingEmployerMatchAmount": "41.67",
				"nextEscalationDate": "Dec 31,2299",
				"contributions": [
					{
						"contributionRateId": "10",
						"contributionRateDescription": "S-Before Tax Contribution",
						"actualContributionPercent": 1,
						"actualContributionAmount": "0.00",
						"escalationPercent": 0,
						"targetPercent": 0,
						"contributionBeginDate": "May 22,2018"
					}
				],
				"totalContributionAmountPerPayCheck": "41.66",
				"businessProcessId": 350,
				"businessProcessNewBeginDate": "2018-11-16",
				"planId": 10,
				"planDescription": "Savings Qualified Plan 1",
				"increasedPayCheckDeductionText": "($208.34 more)",
				"companyMatchAmount": "270.83",
				"missingcompanyMatchAmount": "229.17",
				"packageContributions": [
					{
						"contributionRateId": "10",
						"contributionRateDescription": "S-Before Tax Contribution",
						"suggestedContributionPercent": 6,
						"suggestedContributionAmount": "0.00",
						"contributionDifferenceText": "(5% more)",
						"contributionDifference": 5
					}
				],
				"suggestedTotalContributionAmountPerPayCheck": "250.00",
				"headerText": "Get the Full Match! ",
				"ourSuggestedAmounntText": "SUGGESTED AMOUNT",
				"whyText": "Why?",
				"perPayCheckEstimatedText": "per paycheck (estimated)",
				"companyMatchText": "Company Match",
				"acceptSuggestionsText": "Accept Suggestion",
				"moreOptionsLink": {
					"text": "More options available on full site",
					"type": "sso",
					"url": "https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_CHNG_CTRB_LINK"
				},
				"currentContributionText": "Your Current Contribution",
				"behindSuggestionsDescriptionText": "<hr width='92%'/><p class= 'descText'>There are benefits to saving just a little more now for retirement:</p><ion-item text-wrap class= 'descPoints' no-lines><ul><li class= 'descPoints'>More free money from your company! Contribute enough so your company will match your contributions up to the match limit.</li><li class= 'descPoints'>Your contributions are made before your income is taxed so your current taxable income is less. Roth savings give you the opportunity for tax-free income during retirement.</li><li class= 'descPoints'>Your money may grow over time due to compounding of interest and earnings.</li></ul></ion-item>",
				"estimatedPaycheckText": "Estimated Paycheck Deduction",
				"perPayCheckText": "per paycheck",
				"estimatedPaycheckDescriptionText": "This is an estimated amount that will be deducted from each paycheck, based on your contribution choices and your current pay information. Any changes to your pay information or your contribution choices will impact your contribution amount.",
				"estimatedCompanyMatchText": "Estimated Premier Company Match",
				"moreContributionDetailsLink": {
					"text": "More contribution and company match details available on full site",
					"type": "sso",
					"url": "https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_PRTL_RTRM_SMRY_LND"
				},
				"notGettingFullMatchText": "You’re not getting the full company match.",
				"whatHappensText": "What Happens?",
				"whatHappensNextTitleText": "What Happens Next?",
				"whatHappensNextDescriptionText": "<hr width='100%'/><p class='whathappennext'>When you accept this suggestion:</p><ul class='whnul'><li class='descPoints'>You’ll save <strong>$208.34 more</strong> each paycheck.</li><li class='descPoints'>You’ll get the full company match! Your company will give you <strong>$270.83</strong> each paycheck.</li><li class='descPoints'>Your new Savings Qualified Plan 1 contributions will take effect within 2 paychecks.</li></ul>",
				"behindSuggestionsText": "Behind Our Suggestion",
				"estimatedCompanyMatchDescriptionText": "This is an estimated amount that will be deducted from each paycheck, based on your contribution choices and your current pay information. Any changes to your pay information or your contribution choices will impact your contribution amount.",
				"currentPlanContributionsText": "Current  Savings Qualified Plan 1  Contributions",
				"asOfCurrentDateText": "as of Nov 16, 2018",
				"willIncreaseText": "will increase by 0.0 in Dec 31,2299",
				"isGettingCompanyMatch": true
			} 
	```

 - **Path Mapping**: /api/channel/definedcontributionmobilewidgets/quickEnrollmentMobileWidget?planId=plan_Id - GET Mapping <br> 
 - The **/quickEnrollmentMobileWidget?planId=plan_Id** endpoint return Get Quick Enrollment Configuration Data and All Quick Enrollment.  
Obtain alightRequestHeader and alightPersonSessionToken from this API 
https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location: 
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			1) planId ::: 10
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
			"businessProcessId": "106881",
			"enrollmentType": "Q",
			"planId": "10",
			"planDescription": "Savings Qualified Plan 1",
			"matchTierInfo": "<ul><li class='descPoints'>$1.00 for every dollar that you contribute to the plan, on the first 3% of your pay</li><li class='descPoints'>$1.50 for every dollar that you contribute to the plan, on the next 2% of your pay</li><li class='descPoints'>$0.50 for every dollar that you contribute to the plan, on the next 1% of your pay</li></ul>",
			"payCheckAmount": "$500.00",
			"showCompanyMatch": true,
			"companyMatchAmount": "$300.00",
			"nextEscalationDate": "2020-01-06",
			"personContributionRates": [
				{
					"defaultContributionPercent": 3,
					"defaultContributionAmount": 0,
					"contributionRateDescription": "Before Tax",
					"contributionRateId": "10",
					"contributionRateTransactionId": "120",
					"defaultEscalationPercent": 2,
					"defaultTargetPercent": 10,
					"isContributionOfBonusType": false
				},
				{
					"defaultContributionPercent": 2,
					"defaultContributionAmount": 0,
					"contributionRateDescription": "Before Tax Bonus",
					"contributionRateId": "120",
					"contributionRateTransactionId": "964039",
					"defaultEscalationPercent": 1,
					"defaultTargetPercent": 12,
					"isContributionOfBonusType": true
				}
			],
			"investmentElectionGroupId": "180",
			"investmentElectionGroupTransactionId": "130",
			"investmentElectionGroupEffectiveDate": "2018-12-17",
			"assetClass": [
				{
					"assetClassId": "6",
					"assetClassDescription": "Large U.S. Equity",
					"fundDetails": [
						{
							"fundId": "50",
							"fundDescriptionwithTicker": "Trust Portfoli2",
							"electedInvestmentElectionPercent": 60
						},
						{
							"fundId": "60",
							"fundDescriptionwithTicker": "Trust Portfoli3 (PREME)",
							"electedInvestmentElectionPercent": 40
						}
					]
				}
			],
			"moreOptionsLink": {
				"text": "More options available on full site",
				"type": "sso",
				"url": "https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_ENRL_QLFY_CSTM_PRTL_NAV"
			},
			"moreContributionDetailsLink": {
				"text": "More contribution and company match details available on full site",
				"type": "sso",
				"url": "https://api-dv.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_PRTL_RTRM_SMRY_LND"
			},
			"headerText": "Quick Enrollment",
			"signUpText": "Sign up to save in one step with these enrolment details.",
			"contributionsText": "Contributions",
			"perPayCheckEstimatedText": "per paycheck (estimated)",
			"companyMatchText": "Company Match",
			"eligibleText": "(eligible)",
			"clntNameMatchHeaderText": "Premier Company Match",
			"automaticAnnualIncreaseText": "Automatic Annual Increase",
			"everyYearText": "<h1>+2%<span class=\"everyYearText\">every year (Before Tax)</span></h1>",
			"endingRateText": "2% Ending Rate",
			"investmentMixText": "Investment Mix",
			"estimatedPaycheckText": "Estimated Paycheck Deduction",
			"estimatedPaycheckDescriptionText": "This is an estimated amount that will be deducted from each paycheck, based on your contribution choices and your current pay information. Any changes to your pay information or your contribution choices will impact your contribution amount.",
			"perPaycheckText": "per paycheck",
			"estimatedCompanyMatchText": "Estimated Premier Company Match",
			"estimatedCompanyMatchDescriptionText": "This is the estimated Premier Company match based on your contributions and current pay. Changes to your pay or your contributions may impact the amount Premier Company contributes to your account.",
			"yourContributionsText": "Your contributions will increase automatically every year until you’re contributing at the Ending Rate. Your next contribution increase will start in January 2020.",
			"startingRateText": "Starting Rate",
			"annualIncreaseText": "Annual Increase",
			"endingRate": "Ending Rate",
			"confirmEnrollmentText": "Confirm Enrollment",
			"yourContributionsWillBeginText": "Your contributions will begin within 2 paychecks after submitting this request. You can change contributions or investments at any time.",
			"confirmText": "Confirm",
			"perBonusText": "per bonus"
		} 
	```

 - **Path Mapping**: /api/channel/definedcontributionmobilewidgets/changeContributionsDCMobileWidget?planId=10 - GET Mapping <br> 
 - The **/changeContributionsDCMobileWidget?planId=10** endpoint return Change Contributions Mobile Widget.
Obtain alightRequestHeader and alightPersonSessionToken from this API
https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			1) planId : 10
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
				{
				"planName": "Retire Savings 401(k)",
				"isCustomEscalationDateSupported": true,
				"isSingleCatchUpElectionSupported": false,
				"planWithholdingUSorPRorBoth": "P",
				"planLimitDescription": "Plan and IRC limits",
				"contributionLimitsHeaderText": "Contribution Limits",
				"planLimitText": "Plan Limit",
				"contributionLimitInPercent": 50,
				"contributionLimitInAmount": 185000,
				"contributionLimitDescription": "IRC Limit",
				"contributionLimitDescriptionAmount": 13500,
				"contributionLimitPerYearText": "per year",
				"contributionSecondCatchUpDescription": "IRC Catch-Up Limit",
				"contributionSecondCatchUpPerYearText": "per year",
				"contributionsLimitsFullSiteText": "Review all contribution limits on full site.",
				"dfltYes": false,
				"totalContributionAmountPerPayCheck": "291.65",
				"totalContributionInPercent": "7.00",
				"isShowContributionAmountPerPayCheck": true,
				"isShowTotalContributionInPercent": true,
				"receivingEmployerMatchAmount": "208.33",
				"isShowReceivingEmployerMatchAmount": true,
				"matchTierInfo": "<ul><li class='descPoints'><strong>$1.00</strong> for every dollar that you contribute to the plan, on the first <strong>2%</strong> of your pay</li><li class='descPoints'><strong>$1.50</strong> for every dollar that you contribute to the plan, on the next <strong>1%</strong> of your pay</li><li class='descPoints'><strong>$0.50</strong> for every dollar that you contribute to the plan, on the next <strong>3%</strong> of your pay</li></ul>",
				"isShowMatchAmountRow": true,
				"isGettingFullMatch": true,
				"IsChgCtrbHideAftrTaxSpilOvr": true,
				"businessProcessId": "350",
				"suggestedPackageContributions": [
					{
						"packageName": "Save More",
						"totalContributionAmount": "333.33",
						"isShowTotalContributionAmount": true,
						"isShowTotalContributionPercent": true,
						"totalContributionPercent": "8.00",
						"companyMatchAmount": 208.33,
						"isShowCompanyMatchAmount": true,
						"isShowMatchAmountRow": true,
						"isGettingFullMatch": true,
						"contributionDetails": [
							{
								"contributionRateId": "10",
								"contributionPercent": 6,
								"contributionAmount": 0,
								"contributionRateDescription": "Before Tax",
								"contributionRateType": "BT",
								"contributionInPercentOrDollar": "B",
								"isContributionRateEscalationSupported": true,
								"maximumContributionPercent": 50,
								"minimumContributionPercent": 1,
								"minimumContributionAmount": 18,
								"maximumContributionAmount": 7000,
								"validContributionIncrementInPercent": 0.1,
								"validEscalationIncrementInPercent": 0.1,
								"validTargetIncrementInPercent": 1,
								"escalationPercent": 0,
								"targetPercent": 0,
								"contributionBeginDate": "2019-04-10",
								"contributionEndDate": "2299-12-31",
								"isCtrbBonusAvlbl": true
							},
							{
								"contributionRateId": "20",
								"contributionPercent": 2,
								"contributionAmount": 0,
								"contributionRateDescription": "After Tax",
								"contributionRateType": "AT",
								"contributionInPercentOrDollar": "B",
								"isContributionRateEscalationSupported": true,
								"maximumContributionPercent": 50,
								"minimumContributionPercent": 2,
								"minimumContributionAmount": 19,
								"maximumContributionAmount": 6000,
								"validContributionIncrementInPercent": 0.1,
								"validEscalationIncrementInPercent": 0.2,
								"validTargetIncrementInPercent": 1,
								"escalationPercent": 0,
								"targetPercent": 0,
								"contributionBeginDate": "2019-04-10",
								"contributionEndDate": "2299-12-31",
								"isCtrbBonusAvlbl": false
							}
						]
					},
					{
						"packageName": "Save Even More",
						"totalContributionAmount": "375.00",
						"isShowTotalContributionAmount": true,
						"isShowTotalContributionPercent": true,
						"totalContributionPercent": "9.00",
						"companyMatchAmount": 208.33,
						"isShowCompanyMatchAmount": true,
						"isShowMatchAmountRow": true,
						"isGettingFullMatch": true,
						"contributionDetails": [
							{
								"contributionRateId": "10",
								"contributionPercent": 7,
								"contributionAmount": 0,
								"contributionRateDescription": "Before Tax",
								"contributionRateType": "BT",
								"contributionInPercentOrDollar": "B",
								"isContributionRateEscalationSupported": true,
								"maximumContributionPercent": 50,
								"minimumContributionPercent": 1,
								"minimumContributionAmount": 18,
								"maximumContributionAmount": 7000,
								"validContributionIncrementInPercent": 0.1,
								"validEscalationIncrementInPercent": 0.1,
								"validTargetIncrementInPercent": 1,
								"escalationPercent": 0,
								"targetPercent": 0,
								"contributionBeginDate": "2019-04-10",
								"contributionEndDate": "2299-12-31",
								"isCtrbBonusAvlbl": true
							},
							{
								"contributionRateId": "20",
								"contributionPercent": 2,
								"contributionAmount": 0,
								"contributionRateDescription": "After Tax",
								"contributionRateType": "AT",
								"contributionInPercentOrDollar": "B",
								"isContributionRateEscalationSupported": true,
								"maximumContributionPercent": 50,
								"minimumContributionPercent": 2,
								"minimumContributionAmount": 19,
								"maximumContributionAmount": 6000,
								"validContributionIncrementInPercent": 0.1,
								"validEscalationIncrementInPercent": 0.2,
								"validTargetIncrementInPercent": 1,
								"escalationPercent": 0,
								"targetPercent": 0,
								"contributionBeginDate": "2019-04-10",
								"contributionEndDate": "2299-12-31",
								"isCtrbBonusAvlbl": false
							}
						]
					}
				],
				"currentContributions": [
					{
						"contributionRateId": "10",
						"contributionRateDescription": "Before Tax",
						"contributionRateType": "BT",
						"contributionInPercentOrDollar": "B",
						"isContributionRateEscalationSupported": true,
						"maximumContributionPercent": 50,
						"minimumContributionPercent": 1,
						"minimumContributionAmount": 18,
						"maximumContributionAmount": 7000,
						"validContributionIncrementInPercent": 0.1,
						"validEscalationIncrementInPercent": 0.1,
						"validTargetIncrementInPercent": 1,
						"isEmployerMatchEligible": true,
						"contributionCompanyMatchText": "This contribution is eligible for company match.",
						"contributionDefinition": "<h5>Before-Tax Contribution Rate Id 10</h5><p>updated for manual testing Contributions reduce the taxable income in your pay. However, these contributions and their earnings are taxed when you withdraw them from the plan.</p>",
						"contributionDescriptionDisplayed": true,
						"isCtrbBonusAvlbl": true,
						"contributionPercent": 4,
						"contributionAmount": 0,
						"escalationPercent": 0,
						"targetPercent": 0,
						"contributionBeginDate": "2019-04-10",
						"contributionEndDate": "2299-12-31"
					},
					{
						"contributionRateId": "20",
						"contributionRateDescription": "After Tax",
						"contributionRateType": "AT",
						"contributionInPercentOrDollar": "B",
						"isContributionRateEscalationSupported": true,
						"maximumContributionPercent": 50,
						"minimumContributionPercent": 2,
						"minimumContributionAmount": 19,
						"maximumContributionAmount": 6000,
						"validContributionIncrementInPercent": 0.1,
						"validEscalationIncrementInPercent": 0.2,
						"validTargetIncrementInPercent": 1,
						"isEmployerMatchEligible": true,
						"contributionCompanyMatchText": "This contribution is eligible for company match.",
						"contributionDefinition": "<h5>After-Tax Contribution</h5><p>Contributions don't reduce the taxable income in your pay like before-tax contributions. However, these contributions aren't taxed when you withdraw them from the plan, but any associated earnings are taxable.</p>",
						"contributionDescriptionDisplayed": true,
						"isCtrbBonusAvlbl": false,
						"contributionPercent": 2,
						"contributionAmount": 0,
						"escalationPercent": 0,
						"targetPercent": 0,
						"contributionBeginDate": "2019-04-10",
						"contributionEndDate": "2299-12-31"
					}
				],
				"isBonusAvlbl": true,
				"isEscalationPageEligible": true,
				"nextEscalationDate": "January 6,2020",
				"nextEscalationDateFormatted": "2020-01-06",
				"isShowPayChkDedAtforChgCtrb": true,
				"isShowZeroPayChkDedAtforChgCtrb": true,
				"isShowPayChkTxt": true,
				"IsShowZeroMtchPerPayChk": true,
				"ShowCtrbWholePtForChgCtrb": 2,
				"IsShowDecimalForAt": true,
				"headerText": "Change Contributions",
				"currentText": "Current",
				"perPaycheckText": "per paycheck",
				"matchPerPaycheckText": "match per paycheck",
				"notFullMatchText": "Not Full Match",
				"fullMatchText": "Full Match",
				"currentCompanyMatchText": "Company Match",
				"createYourOwnText": "Create Your Own",
				"createYourOwnDescriptionText": "Your plan and the IRS impose contribution limits.",
				"enterHowMuchToContributeText": "Enter how much you want to contribute.",
				"currentContributionsText": "Current Contributions",
				"estimatedPerPaycheckText": "estimated",
				"percentSymbolText": "%",
				"currencySymbolText": "$",
				"yourContributionsText": "Your Contribution",
				"clientContributionsText": "Alight Company Contributions",
				"calculateImpactText": "Calculate Impact",
				"skipButtonText": "Skip",
				"automaticAnnualIncreaseText": "Automatic Annual Increase",
				"optionalText": "optional",
				"increaseYourcontributionText": "Increase your contributions over time on a schedule you can live with.",
				"automaticAnnualIncreaseOptionText": "Automatic Annual Increase Option",
				"startingRateText": "Starting Rate",
				"annualRateIncreaseText": "Annual Rate Increase",
				"endingRateText": "Ending Rate",
				"uptoText": "up to",
				"afterTaxSpillOverText": "After-Tax Spillover",
				"doYouWantAfterTaxSpillOverText": "Do you want After-Tax Spillover?",
				"yesAfterTaxSpillOverText": "<span class='outerSpanTextYes'><b>Yes,</b> <span class='innerspanText'>switch my Before-Tax contributions to </span> <b>After-Tax</b> <span class='innerspanText'> contributions if I reach the IRS limit.</span></span>",
				"changeContributionsBeforeTaxText": "Change my Before-Tax to After-Tax contributions if I reach the IRS limits.",
				"afterTaxDefinitionText": "<h5>After-Tax Spillover</h5><p>Spillover occurs if you keep contributing at the same rate, but on an after-tax basis, when you reach the IRS limit of <strong>${token:IRS_LMT}</strong> on Before-Tax contributions before the end of the year.</p>",
				"noAfterTaxSpillOverText": "<span class='outerSpanTextNo'><b>No,</b> <span class='innerspanText'> I don't want After-Tax Spillover.</span></span>",
				"reviewChoicesText": "Review Choices",
				"contributionsText": "Contributions",
				"nextAutomaticIncreaseText": "Next Automatic Increase",
				"paranthesisOpenText": "(",
				"paranthesisCloseText": ")",
				"moreText": "more",
				"periodText": ".",
				"howItWorksText": "How it Works",
				"resourcesText": "Resources",
				"contributionLmtText": "Contribution Limits",
				"cpmpareRothVsBeforeText": "Compare Roth 401(k) Versus Before-Tax",
				"commaText": ",",
				"annualRateBlankValText": "Annual Rate Increase field is blank. Enter information before continuing.",
				"EndingRateBlankValText": "Ending Rate field is blank. Enter information before continuing.",
				"annualIncEnteredText": "The annual increase rate you entered for",
				"enterLowerAnnualIncText": "equals or exceeds the ending rate. Enter an annual increase rate lower than the ending rate",
				"entryInlimitsValText": "Your entry must be within the limits",
				"inIncOfText": "in increments of",
				"andSoForthText": "and so forth",
				"forExampleText": "for example",
				"numericEntryValText": "Your entry is invalid. Enter a valid numeric value before continuing.",
				"footnoteNumericOneText": "1",
				"footnoteNumericTwoText": "2",
				"footnoteNumericThreeText": "3",
				"annualIncAndEndingRatePercntText": "If you wish to setup an annual increase for this rate, then you must enter both an annual increase percent and ending rate percent",
				"confirmChangesHeaderText": "Confirm Changes",
				"confirmChangesDescText": "Your new contributions will begin within 2 paychecks after submitting this request.",
				"howAutmtcAnlIncWorksText": "How Automatic Annual Increase Works",
				"descriptionText": "Description",
				"whyConsdrAutmtcAnlIncText": "Why Consider Automatic Annual Increase?",
				"howAutmtcAnlIncWorksDescPara1Text": "You can create a strategy to automatically increase your contributions each year until you reach your ending contribution rate. You’ll get where you want to be&mdash;but on a schedule you can live with. ",
				"howAutmtcAnlIncWorksDescPara2Text": "You can create a strategy to automatically increase your contributions each year until you reach your ending contribution rate. You’ll get where you want to be&mdash;but on a schedule you can live with. ",
				"whyConsdrAutmtcAnlIncDescText": "With the automatic annual increase option, you could gain more retirement savings by age 65 at a pace that works for you.",
				"projSavingText": "Projected Savings at Age 65",
				"projSavingDescText": "A 40-year-old making $40,000  who is enrolled in the plan at 6% and automatically increases his or her contribution rate annually until it reaches 10% may gain <span><large>$105,000 </large></span>in retirement savings (based upon the assumptions that follow).",
				"assummptionText": "Assumptions ",
				"assummptionList1Text": "Fees for this plan are assumed to be 25 basis points per year. ",
				"assummptionList2Text": "Salary is expected to increase at 2% per year. ",
				"assummptionList3Text": "The account is expected to earn a gross return of 7.25% each year. ",
				"exampleText": "Example",
				"eightPercentageText": "8%",
				"twoPercentageText": "2%",
				"fourteenPercentageText": "14%",
				"isChgCtrbYngExpl": false,
				"isChgCtrbMdlExpl": true,
				"isChgCtrbOldExpl": false,
				"contributionLimitLink": {
					"text": "Contribution Limits",
					"type": "sso",
					"url": "https://api.int.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_CTRB_LIMIT_LNK"
				},
				"rothVsBeforeTaxLink": {
					"text": "Compare Roth 401(k) Versus Before-Tax",
					"type": "sso",
					"url": "https://api.int.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_CMPR_TO_ROTH_VS_BT_LNK"
				},
				"noteText": "Note:",
				"planAndIrsText": "Plan and IRS limits",
				"imposedText": "are imposed.",
				"annualIncreaseImpactAlert": "The changes you made on the previous page impact this annual increase.",
				"annualIncreaseCancelAlert": "The changes you made on the previous page will cancel this annual increase.",
				"afterTaxDefinitionIRSLimitAmount": "0",
				"afterTaxAlertsAndTips": "Consider Choosing Yes if You Might Contribute More Than $0 (IRS Limit) This Year.",
				"definitionsTabHeader": "Definitions",
				"clntNameMatchHeaderText": "Contribution Information",
				"whyDoItText": "Why Do It?",
				"annualRateIncHoverText": "This is the percentage your contribution rate will increase each year.",
				"endRateHoverText": "This is the percent that your contribution rate will eventually reach (but not exceed).",
				"automaticAnlIncFootnoteTwoText": "Automatic annual increase is not applicable to this contribution type because you’re contributing the maximum allowed by the plan, so you can’t increase your contribution each year. ",
				"automaticAnlIncFootnoteOneText": "Automatic annual increase is not applicable to this contribution type because you didn’t make a choice for this contribution rate, so you can’t increase it. If you’d like to increase it, you must",
				"automaticAnlIncFootnoteOneLinkText": "choose a starting rate",
				"automaticAnlIncFootnoteThreeText": "Automatic annual increase is not applicable to this contribution type because you’ve chosen to contribute by dollar amount. To increase your contributions each year, return to",
				"automaticAnlIncFootnoteThreeLinkText": "enter a new contribution",
				"automaticAnlIncFootnoteThreeEndkText": "by percent.",
				"withAfterTaxText": "With After-Tax Spillover, you can keep contributing up to the plan limit if you reach the",
				"irsLimitText": "IRS Limit",
				"beforeEndOfYearText": "before the end of the year.",
				"perBonus": "per bonus",
				"atsHowOtWorksExampleDescText": "Susan decided to contribute 10% Before-Tax and 10% Roth. She recently received a raise. As a result, she’ll reach the IRS limit in October with her current contribution rates. She chooses to use After-Tax Spillover, which means that she'll continue contributing the entire year.",
				"atsHowOtWorksBeforeTaxAndRothCtrbText": "Before-Tax and Roth Contributions",
				"atsHowOtWorksAfterTaxCtrbText": "After-Tax Contributions",
				"atsHowOtWorksSVNWithoutText": "Without",
				"atsHowOtWorksSVNWithText": "With",
				"atsHowOtWorksSVNWAfterTaxText": "After-Tax",
				"atsHowOtWorksSVNWSpilloverText": "Spillover",
				"atsHowOtWorksSVNIRSLimitText": "IRS Limit Reached",
				"atsHowOtWorksHeadText": "About After-Tax Spillover",
				"atsHowOtWorksHeadDescText": "With After-Tax Spillover, you can automatically switch your Before-Tax contributions to After Tax if you reach the IRS limit before the end of the year.",
				"atsWhyYouWantCtrbAsMuchDescText": "Want to stop worrying about hitting the IRS limit and having your Before-Tax contributions automatically suspended before the end of the year? With After-Tax Spillover, any contributions that bring you over the IRS limit will be switched to the After-Tax portion of your plan, so you can contribute more to the plan.",
				"atsWhyYouWantKeepGettingCMDescText": "The company match is contributed to your savings each pay period. If you contribute too fast and reach the IRS limit for Before-Tax contributions, these contributions stop. You’ll also stop getting the company match (unless you’re already contributing to the After-Tax portion of your plan). With After-Tax Spillover, you don’t have to monitor how close you’re getting to the IRS limit. Any contributions that go over the limit will be switched to the After-Tax portion of your plan, so you’ll continue to get the company match.",
				"atsThingsToConsiderBulletThreeText": "At the beginning of next year, your After-Tax Spillover contributions switch back to Before Tax.",
				"atsWhyYouWantHeadText": "Why You Might Want to Take Advantage of After-Tax Spillover",
				"atsWhyYouWantCtrbAsMuchText": "You Can Contribute as Much as You Want, Up to the Plan Limit",
				"atsWhyYouWantKeepGettingCMText": "You’re More Likely to Keep Getting the Company Match",
				"atsThingsToConsiderText": "Some Things to Consider:",
				"atsThingsToConsiderBulletoneText": "Any money you put into the After-Tax portion of your plan is taxed and means less take-home pay.",
				"atsThingsToConsiderBulletTwoText": "The plan limit still applies.",
				"sameText": "same",
				"cyoFoorNoteText": "Any catch-up contributions are included.",
				"hyphenSymbolText": "-",
				"estimatedAmtFootnoteText": "This is an estimated amount based on your contribution choices and your current pay information. Any changes to your pay information or your contribution choices will impact this amount.",
				"cancelConfirmationText": "Are you sure you want to cancel this request?",
				"changedYourContributionsText": "You changed your contributions.",
				"bonusCtrbFootnoteText": "Your bonus contributions are not included in the total amount estimated per paycheck because the deduction is not taken from every paycheck.",
				"notGettingFullMatchText": "Not Getting Full Match",
				"gettingFullMatchText": "Getting Full Match",
				"annualIncreaseModelText": "This is the percent your contribution rate will increase each year.",
				"exampleModelText": "In this example, it will take 3 years to get from an 8% contribution rate to a 14% contribution rate, but this person <strong>will</strong> get there.",
				"ircText": "IRC",
				"irsText": "IRS",
				"irsIrcText": "IRS/IRC",
				"hasChgCtrbAtSplOvrExmpl": true,
				"isShowChgCtrbExmpl": true
		} 
	```

 - **Path Mapping**:  /api/channel/definedcontributionmobilewidgets/monthlyRetirementIncomeProjectionMobileWidget - GET Mapping <br> 
 - The **/monthlyRetirementIncomeProjectionMobileWidget** endpoint return monthly Retirement Income Projection Mobile Widget.
Obtain alightRequestHeader and alightPersonSessionToken from this API
https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location: 
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			NA
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
		{
			"isMonthlyRetirementProjectionElig": true,
			"qualifiedPlanId": 10,
			"projectionAccountId": "40819828::1",
			"onTrack": false,
			"goalGapAmount": 716,
			"retirementAgeAtProjection": 65,
			"pageTitleTxt": "Projected Monthly Retirement Income",
			"monthlyRetirementProjectionCardData": {
				"cardAgeText": "Projected Retirement Income at Age 65",
				"cardStatusMessage": "You may get <strong>$716.00 less</strong> than your retirement income goal",
				"retirementChartData": {
					"beginValue": "$0.00",
					"endValue": "$3,833.00",
					"projectionText": "per month",
					"projectionAmount": [
						"$3,117.00"
					],
					"goalText": "Goal",
					"poorMarketText": "Poor Market:",
					"poorMarketProjectionAmount": "$2,450.00",
					"updateProjectionText": "Update Projection",
					"resetText": "Reset",
					"startColor": "#f4b751",
					"endColor": "#cdcccb"
				},
				"isCanIDoBetterButtonElig": true,
				"canIDoBetterData": {
					"text": "Can I Do Better?",
					"type": "sso",
					"url": "https://api.int.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=DC_PRTL_RTRM_SMRY_LND"
				},
				"isSaveMoreButtonElig": false,
				"isChangeContributionElig": false,
				"isFootNoteElig": true,
				"footnoteText": "Your estimated retirement income goal is based on 70% of your estimated income at retirement age, unless you have specified a different goal within the advice site.",
				"footnoteSuperScriptText": "1",
				"isPhoneNumberElig": true,
				"callAdvisorText": "Call Financial Engines for help. <span class =\"ah-nowrap\">1-800-601-5957</span> "
			}
		} 
	```

 - **Path Mapping**: /api/channel/definedcontributionmobilewidgets/investmentChangeWidget/fundReallocationWidget/360?skipPreActivityCall=true - GET Mapping <br> 
 - The **/fundReallocationWidget/360?skipPreActivityCall=true** endpoint return Fund Reallocation data from Investment Change.
Obtain alightRequestHeader and alightPersonSessionToken from this API
https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			 **alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			 **alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			1) skipPreActivityCall ::: true
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
			"isFundReallocationOnMobileEnabled": true,
			"isDcTsfrPartParmElig": true,
			"hasPreActivityEdits": false,
			"businessProcessId": "360",
			"businessProcessDescription": "Fund Reallocation - Retirement Savings Plan",
			"planId": "10",
			"planDescription": "Retirement Savings Plan",
			"effectiveDate": "2020-01-28",
			"cutOffTime": "15.00.00.000000",
			"investmentGroupRules": [
				{
					"investmentGroupCategoryId": "1290",
					"isCategoryIdPartOfTransactionGroup": false,
					"categoryDescription": "Fund Reallocate-All Accounts",
					"isAllInvestmentGroupCategoryType": true,
					"validIncrementPercent": 4,
					"minimumAllocationPercent": 0,
					"maximumAllocationPercent": 100,
					"isAutoRebalanceEligibleForCategory": true,
					"defaultAutoRebalanceFrequency": "9",
					"isEligibleToAplyReallocationToFutureInvestments": true,
					"investmentGroupIncludeBalanceAmount": 34636.87,
					"investmentGroupExcludeBalanceAmount": 0,
					"fundListByAssetClass": [
						{
							"assetClassId": "5",
							"assetClassDescription": "Lifestyle/Pre-mix",
							"fundList": [
								{
									"fundId": "40",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 33579.71,
									"currentAllocationPercent": 97,
									"fundDescription": "Trust Portfolio 1",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMA",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "Document",
									"fundUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_40_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
								}
							]
						},
						{
							"assetClassId": "6",
							"assetClassDescription": "Large U.S. Equity",
							"fundList": [
								{
									"fundId": "50",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 1057.16,
									"currentAllocationPercent": 3,
									"fundDescription": "Trust Portfoli2",
									"isCoreFund": false,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMB",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0231600009"
								}
							]
						},
						{
							"assetClassId": "7",
							"assetClassDescription": "Mid U.S. Equity",
							"fundList": [
								{
									"fundId": "70",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfolio 4",
									"isCoreFund": false,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMD",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "CMSDocument",
									"fundUrl": "https://api.int.alight.com/api/channel/content/documentManagement/document?filepath=Documents/DC/ChangeFutureInvestments/F0080FDDTLPAGE"
								}
							]
						},
						{
							"assetClassId": "4",
							"assetClassDescription": "Balanced Funds",
							"fundList": [
								{
									"fundId": "80",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfolio 5",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREME",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0281400006"
								}
							]
						},
						{
							"assetClassId": "8",
							"assetClassDescription": "Small U.S. Equity",
							"fundList": [
								{
									"fundId": "90",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfoli6",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMF",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0281500006"
								}
							]
						},
						{
							"assetClassId": "12",
							"assetClassDescription": "Stock",
							"fundList": [
								{
									"fundId": "170",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Company Stock",
									"isCoreFund": true,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMS",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "Document",
									"fundUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_170_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
								}
							]
						}
					],
					"isThisCategoryFullExcluded": false,
					"categoryDescriptionText": "Asset testing value Category description for Mobile category Id 1290 "
				},
				{
					"investmentGroupCategoryId": "1350",
					"isCategoryIdPartOfTransactionGroup": false,
					"categoryDescription": "Employee money",
					"isAllInvestmentGroupCategoryType": false,
					"validIncrementPercent": 4,
					"minimumAllocationPercent": 0,
					"maximumAllocationPercent": 100,
					"isAutoRebalanceEligibleForCategory": false,
					"isEligibleToAplyReallocationToFutureInvestments": false,
					"investmentGroupIncludeBalanceAmount": 31750.47,
					"investmentGroupExcludeBalanceAmount": 0,
					"fundListByAssetClass": [
						{
							"assetClassId": "5",
							"assetClassDescription": "Lifestyle/Pre-mix",
							"fundList": [
								{
									"fundId": "40",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 30781.4,
									"currentAllocationPercent": 97,
									"fundDescription": "Trust Portfolio 1",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMA",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "Document",
									"fundUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_40_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
								}
							]
						},
						{
							"assetClassId": "6",
							"assetClassDescription": "Large U.S. Equity",
							"fundList": [
								{
									"fundId": "50",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 969.06,
									"currentAllocationPercent": 3,
									"fundDescription": "Trust Portfoli2",
									"isCoreFund": false,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMB",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0231600009"
								},
								{
									"fundId": "60",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfoli3",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMC",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0321200007"
								}
							]
						},
						{
							"assetClassId": "7",
							"assetClassDescription": "Mid U.S. Equity",
							"fundList": [
								{
									"fundId": "70",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfolio 4",
									"isCoreFund": false,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMD",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "CMSDocument",
									"fundUrl": "https://api.int.alight.com/api/channel/content/documentManagement/document?filepath=Documents/DC/ChangeFutureInvestments/F0080FDDTLPAGE"
								}
							]
						},
						{
							"assetClassId": "8",
							"assetClassDescription": "Small U.S. Equity",
							"fundList": [
								{
									"fundId": "90",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfoli6",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMF",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0281500006"
								}
							]
						},
						{
							"assetClassId": "12",
							"assetClassDescription": "Stock",
							"fundList": [
								{
									"fundId": "170",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Company Stock",
									"isCoreFund": true,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMS",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "Document",
									"fundUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_170_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
								}
							]
						}
					],
					"isThisCategoryFullExcluded": false,
					"categoryDescriptionText": "Money you contributed to your plan. "
				},
				{
					"investmentGroupCategoryId": "1340",
					"isCategoryIdPartOfTransactionGroup": false,
					"categoryDescription": "Employer money",
					"isAllInvestmentGroupCategoryType": false,
					"validIncrementPercent": 4,
					"minimumAllocationPercent": 0,
					"maximumAllocationPercent": 100,
					"isAutoRebalanceEligibleForCategory": false,
					"isEligibleToAplyReallocationToFutureInvestments": false,
					"investmentGroupIncludeBalanceAmount": 2886.41,
					"investmentGroupExcludeBalanceAmount": 0,
					"fundListByAssetClass": [
						{
							"assetClassId": "5",
							"assetClassDescription": "Lifestyle/Pre-mix",
							"fundList": [
								{
									"fundId": "40",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 2798.31,
									"currentAllocationPercent": 97,
									"fundDescription": "Trust Portfolio 1",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMA",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "Document",
									"fundUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_40_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
								}
							]
						},
						{
							"assetClassId": "6",
							"assetClassDescription": "Large U.S. Equity",
							"fundList": [
								{
									"fundId": "50",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 88.1,
									"currentAllocationPercent": 3,
									"fundDescription": "Trust Portfoli2",
									"isCoreFund": false,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMB",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0231600009"
								},
								{
									"fundId": "60",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfoli3",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREMC",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0321200007"
								}
							]
						},
						{
							"assetClassId": "7",
							"assetClassDescription": "Mid U.S. Equity",
							"fundList": [
								{
									"fundId": "70",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfolio 4",
									"isCoreFund": false,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMD",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "CMSDocument",
									"fundUrl": "https://api.int.alight.com/api/channel/content/documentManagement/document?filepath=Documents/DC/ChangeFutureInvestments/F0080FDDTLPAGE"
								}
							]
						},
						{
							"assetClassId": "4",
							"assetClassDescription": "Balanced Funds",
							"fundList": [
								{
									"fundId": "80",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Trust Portfolio 5",
									"isCoreFund": false,
									"isTargetDateFund": true,
									"fundPerformanceTicker": "PREME",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "public",
									"fundUrl": "https://hewitt.lipperweb.com/?Symbol=0281400006"
								}
							]
						},
						{
							"assetClassId": "12",
							"assetClassDescription": "Stock",
							"fundList": [
								{
									"fundId": "170",
									"fundUseLabel": "RECEIVE",
									"fundBalanceAmount": 0,
									"currentAllocationPercent": 0,
									"fundDescription": "Company Stock",
									"isCoreFund": true,
									"isTargetDateFund": false,
									"fundPerformanceTicker": "PREMS",
									"fundPerformanceTickerCode": "Y",
									"fundText": "Fund Name",
									"fundType": "Document",
									"fundUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=DC_FUND_170_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso"
								}
							]
						}
					],
					"isThisCategoryFullExcluded": false,
					"categoryDescriptionText": "Money your employer contributed to your plan. "
				},
				{
					"investmentGroupCategoryId": "955010",
					"isCategoryIdPartOfTransactionGroup": false,
					"categoryDescription": "Fund Reallocate-Temp Accts",
					"isAllInvestmentGroupCategoryType": false,
					"validIncrementPercent": 1,
					"minimumAllocationPercent": 0,
					"maximumAllocationPercent": 100,
					"isAutoRebalanceEligibleForCategory": false,
					"defaultAutoRebalanceFrequency": "N",
					"isEligibleToAplyReallocationToFutureInvestments": false,
					"investmentGroupIncludeBalanceAmount": 0,
					"investmentGroupExcludeBalanceAmount": 2886.41,
					"fundListByAssetClass": [
						{
							"assetClassId": "5",
							"assetClassDescription": "Lifestyle/Pre-mix",
							"fundList": []
						},
						{
							"assetClassId": "6",
							"assetClassDescription": "Large U.S. Equity",
							"fundList": []
						}
					],
					"isThisCategoryFullExcluded": true,
					"categoryDescriptionText": "Please setup the tool tip text item for this category."
				}
			],
			"autoRebalanceFrequencies": [
				{
					"autoRebalanceFrequency": "9",
					"autoRebalanceDescription": "Every 90 Days"
				},
				{
					"autoRebalanceFrequency": "8",
					"autoRebalanceDescription": "Every 180 Days"
				},
				{
					"autoRebalanceFrequency": "A",
					"autoRebalanceDescription": "Annually"
				}
			],
			"isAllSeparateCategoriesAreFullExcluded": false,
			"hasFullExcludedFunds": true,
			"isAllCategoryFullExcludedFunds": false,
			"isAllCategoryAvailable": true,
			"isPendingAutoRebalancingOnSameDate": false,
			"isPendingAutoRebalancingOnInFuture": false,
			"fundReallocationStaticData": {
				"pageTitle": "Create New Investment Mix",
				"effectiveDateText": "Effective Date <span class=\"ah-nowrap\">Jan 28, 2020</span>",
				"marketCloseNoteText": "(If you complete your changes by market close on <span class=\"ah-nowrap\">Jan 28, 2020</span>)",
				"pendingAutoRebalancingMessageHeaderText": "Auto Rebalance Pending",
				"pendingAutoRebalancingMessageText": "If you want to make a new investment request, you must either wait until the auto rebalance completes, or turn off auto rebalancing on the full site.",
				"onlyFundMessageHeaderText": "This Option Isn’t Available ",
				"onlyFundMessageText": "This option isn’t available to you because you’ve chosen to invest 100% in one fund.",
				"fullExcludeModelHeaderText": "This Option Isn’t Currently Available",
				"fullExcludeModelMessageText": "You’re currently invested in funds that are not available for this option. To make changes to this plan, return to the Change Investments page and choose a different option",
				"fullExcludeModelButtonText": "Return to Change Investments",
				"dallerSign": "$",
				"percentSign": "%",
				"submitLabel": "Submit",
				"fullStopText": ".",
				"clientParaOneText": "Client Para Text One",
				"clientParaTwoText": "Client Para Text Two",
				"clientParaThreeText": "Client Para Text Three",
				"showTargetDateEditMessage": true,
				"showClientParaTwoText": false,
				"showClientParaThreeText": false,
				"planDocumentsText": "Plan Documents",
				"planDocumentsLinkUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=MBL_DC_PLAN_DOC_YBR_LINK&srvcLng=&tokenmap=4A30012B6A1F0D1C0D823DB8E9D12C35AA7EF379E0D043527727318505B975EF5236BA3BF45588B3761F24669BE531DEF2DC5089705A7DD2B4BA59988BCD4AC75AAEDDD62CA23C5D24A5BDAC72B55CE1&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso",
				"planDocumentsLinkType": "sso",
				"howToApplyYourChange": {
					"chooseMixPageTitleText": "How to Apply Your Change",
					"chooseMixGuideText": "You can apply your changes to all your money, or to separate sources of money.",
					"allMoneyTogetherHeaderText": "All Money Together",
					"allMoneyTogetherText": "Make one change that will apply to all your money, whatever the source.",
					"separatelyHeaderText": "Separately",
					"separatelyText": "Make separate choices for the different sources of money (for example, you may be able to make investment choices just for the money coming from your employer)."
				},
				"chooseMoneySourcePage": {
					"chooseMoneySourcePageTitleText": "Choose the Money Source to Change",
					"chooseMoneySourcePageGuideText": "Choose one or more.",
					"chooseMoneySourcePageButtonText": "Where Are My Other Choices?",
					"modelPageTitleText": "Where are my other choices?",
					"modelPageGuideText": "The following options are not available:",
					"pageValidationText": "You must choose at least one checkbox."
				},
				"fundPerformanceText": "Fund Performance",
				"fundPerformanceLinkUrl": "https://api.int.alight.com/api/channel/personsinglesignonlink/getSSOTargetLink?partnerName=Portal&applicationName=uma&pageCode=MBL_DC_PRTL_INV_INQRY_PERF_LINK&srvcLng=&targetUrl=https://l8sita09.hewitt.com:9430/web/retirement4x/sso",
				"fundPerformanceLinkType": "sso",
				"chooseNewFundMixPage": {
					"chooseFundPageTitleText": "Choose Your New Fund Mix",
					"resourcesText": "Resources",
					"chooseFundNoteText": "<span class='boldFont'>Note:</span> Check plan documents for transfer restrictions or redemption fees.",
					"tableHaderFundText": "Fund",
					"footNoteOneSuperscript": "1",
					"tableHaderExistingMixText": "Existing Mix",
					"tableHaderNewMixText": "New Mix",
					"footNoteTwoSuperscript": "2",
					"footNoteOneText": "The fund amounts displayed reflect values at the close of the previous market. The actual amounts in this transaction may change due to market fluctuations. Any requests pending to process prior to this fund transfer are included in the estimated fund amounts.",
					"footNoteTwoText": "Your portfolio total reflects the values of your funds at the close of the previous market. The actual value of your portfolio in this transaction may change due to market fluctuations. Any requests pending to process prior to this fund transfer are included in the estimated fund amounts.",
					"validNumberText": "Your entry is invalid. Enter a valid numeric value before continuing.",
					"targetDateFundEditHeaderText": "You Put Less Than 100% in a Target Date Fund",
					"targetDateFundEditMessageText": "Your chosen mix places less than 100% of your money into a target date fund. Generally, one target date fund applies to your entire account balance. Choose Return if you want to adjust your mix.",
					"totalNotFullPercentValidationText": "Your entries must total 100%. Review and revise your entries before continuing. ",
					"hundredPercent": "100%"
				},
				"applyYourMixPage": {
					"applyMixTitleText": "Apply Your Mix",
					"decideMixNoteText": "Decide how you want to apply your new mix.",
					"whyRebalancingButtonText": "Why Rebalancing is Important",
					"modelDescriptionTextOne": "Current and Future Balances, with Rebalancing",
					"modelDescriptionTextTwo": "Current and Future Balances",
					"modelDescriptionTextThree": "Current Balance Only",
					"modelDescriptionTextFour": "Your portfolio will not be automatically rebalanced in the future.",
					"howToApplyMixText": "How To Apply Your Mix",
					"firstRadioButtonDescriptionText": "Your new mix will be applied to your current balance and future contributions, and your portfolio will be automatically rebalanced periodically to maintain your investment mix.",
					"secondRadioButtonDescriptionText": "Your new mix will be applied to your current balance and future contributions.",
					"thirdRadioButtonDescriptionText": "Your new mix will be applied to your current balance, but your future contribution choices will not change as a result of this request.",
					"advantagesOfRebalancingHeaderText": "Advantages of Rebalancing",
					"advantagesOfRebalancingBulletOneText": "Returns portfolio to your intended investment approach",
					"advantagesOfRebalancingBulletTwoText": "Keeps your portfolio diversified",
					"advantagesOfRebalancingBulletThreeText": "Avoids risk of some investments dominating your portfolio",
					"advantagesOfRebalancingBulletFourText": "Employs top rule of investing—selling high and buying low",
					"rebalancingHelpHeaderText": "Rebalancing Helps Maintain Your Portfolio Strategy",
					"rebalancingHelpParaOneText": "While you can't control the stock market, you can control your long-term investment strategy for your retirement portfolio.",
					"rebalancingHelpParaTwoText": "Today, you are choosing a particular mix of stocks, bonds, mutual funds, and/or other assets for your portfolio. Over time, your investments will naturally vary in their performance, which may cause your portfolio to become unbalanced. Higher-performing assets may take over a greater portion of your original mix of funds than you intended. If you do nothing, this can lead to unnecessary risk and less diversification.",
					"rebalancingHelpParaThreeText": "What you can do is rebalance your investments periodically to keep your long-term strategy on track. And, instead of manually rebalancing your portfolio periodically, you can choose to have it done for you automatically.",
					"rebalancingHelpParaFourText": "<span class='boldFont'>Note:</span>  If you're invested 100% in one fund, automatic rebalancing will never change your mix; you don't need to choose to automatically rebalance.",
					"rebalancingExampleHeaderText": "Example of How a Portfolio Gets Unbalanced",
					"rebalancingExampleParaOneText": "A moderate risk investor begins saving by creating a portfolio containing 50% in stocks, 25% in bonds, and 25% in a money market. After one year, the stock investment soared in value, to become 65% of the portfolio. Without rebalancing, the investor's portfolio shifted into a higher risk mix than was planned. The investor would have to move money manually from stocks to bonds and the money market to restore the original mix desired.",
					"rebalancingExampleParaTwoText": "These pie charts show a sample investment strategy, how the portfolio changed naturally after one year, and how rebalancing returned it to the original strategy:",
					"investmentStrategyText": "Investment Strategy",
					"afterOneYearText": "After One Year",
					"afterRebalancingText": "After Rebalancing",
					"signUpAutoRebalancingHeaderText": "Signing Up for Automatic Rebalancing",
					"signUpAutoRebalancingParaText": "Simply choose the option that includes \"rebalancing\". Your portfolio will be rebalanced at the next chosen interval, after this reallocation request is completed. You can turn off automatic rebalancing at any time from the Change Investments tab on the full site."
				},
				"rebalancingFrequencyPage": {
					"rebalancingFrequencyTitleText": "Rebalancing Frequency",
					"rebalancingFrequencyNoteText": "Decide how often your portfolio will be automatically rebalanced.",
					"singleRebalancingMessage": "Your new mix will be applied to your current balance and future contributions, and your portfolio will be automatically rebalanced  to maintain your investment mix."
				},
				"reviewPage": {
					"reviewPageTitleText": "Review Your Choices",
					"reviewPageNoteText": "Review your choices below to make sure they are correct before you submit your request.",
					"totalText": "Total",
					"applyMixReviewOneText": "Your portfolio will not be automatically rebalanced in the future.",
					"newFundMixText": "New Fund Mix"
				},
				"cancelMessageText": "Are you sure you want to cancel this request?"
			}
		}
 
	```

 - **Path Mapping**:  /api/channel/definedcontributionmobilewidgets/boostDCMobileWidget/contributionRateChange - POST Mapping <br> 
 - The **/boostDCMobileWidget/contributionRateChange** endpoint return Update Boost Retirement Mobile Widget. 
 Obtain alightRequestHeader and alightPersonSessionToken from this API
 https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md
 Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
 https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","clientId":"19943","roleId":"19943_1.0-E:@PPT@","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::b3e28c18-39f7-414c-a2ed-075aa92fb035_2020-08-27-01.59.16.406000::sessionCreatedTimestamp::2020-08-27-01.59.16.406000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			NA
	```
	- Request Body
	```
			{

			  "planId": "10",

			  "escalationDate": "2019-01-01",

			  "requestingBusinessProcess": "106881",

			  "newContributions": [

				{

				  "contributionRateId": "10",

				  "contributionBeginDate": "2019-01-01",

				  "contributionEndDate": "2019-12-31",

				  "electedContributionPercent": 10,

				  "electedContributionAmount": 10,

				  "escalationPercent": 10,

				  "targetPercent": 10

				}

			  ]

			}
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
				"statusCode": 201,
				"statusMessage": "Success",
				"thatsItText": "That’s it!",
				"boostedRetirementText": "You boosted your retirement.",
				"confirmationNumberText": "Confirmation number",
				"confirmationNumber": "115500039",
				"confirmationEmailedText": "Confirmation emailed to",
				"confirmationEmailId": "",
				"whatsNextText": "What’s next?",
				"whatsNextDescriptionText": "Your new {0} contributions will begin within 2 paychecks.",
				"okText": "OK"
			} 
	```
 
### Screen Shot:

 - This service returns contribution information for the user's enrolled plan to be displayed on balance chart, investment mix
   and contribution screen. The response of this service may contains the data depending on the participant : DC 401K balance total, ROR (Rate of Return), periodic RoR percentage, Gain & Loss, current plan balance, Fund details, fund amount, per paycheck, company match, BT, RT, Roth taxes etc. The service returns contribution details for a specific plan when plan id value is passed to it.
	![UPoint Mobile](balanceChart.png) </br>
	![UPoint Mobile](investmentMix.png) </br>
	![UPoint Mobile](contribution.png)
