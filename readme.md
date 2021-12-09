[comment]: # "Auto-generated SOAR connector documentation"
# Cisco Meraki Dashboard

Publisher: World Wide Technology  
Connector Version: 1\.9  
Product Vendor: Cisco Meraki  
Product Name: Cisco Meraki  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 1\.0\.240  

This app interfaces with the Cisco Meraki cloud managed devices\. The search string specified is used to match a value in the client MAC address or description field\. The default dashboard URL is dashboard\.meraki\.com\. The API Key is generated in your account profile\. An account with read only privileges is acceptable\.

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Cisco Meraki asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**Meraki\-API\-Key** |  required  | string | Meraki API key
**dashboard** |  optional  | string | Dashboard URL

### Supported Actions  
[locate device](#action-locate-device) - Locates a specific device in your cloud managed Meraki network  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity  

## action: 'locate device'
Locates a specific device in your cloud managed Meraki network

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**timespan** |  required  | Timespan \(seconds\) | numeric | 
**search\_string** |  required  | Match in MAC or description\. Asterisk \* returns all\. | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.data\.\*\.client\.mac | string |  `mac address` 
action\_result\.data\.\*\.client\.description | string | 
action\_result\.data\.\*\.device | string | 
action\_result\.data\.\*\.network | string | 
action\_result\.data\.\*\.organization | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.parameter\.timespan | string | 
action\_result\.parameter\.search\_string | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'test connectivity'
Validate the asset configuration for connectivity

Type: **test**  
Read only: **True**

This action logs into the Cisco Meraki Cloud Service using a REST API call to validate the API key

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output