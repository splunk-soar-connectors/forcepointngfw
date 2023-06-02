[comment]: # "Auto-generated SOAR connector documentation"
# Forcepoint Firewall

Publisher: Martin Ohl  
Connector Version: 1\.0\.6  
Product Vendor: Forcepoint  
Product Name: NGFW  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.0\.1068  

This app integrates with Forcepoint Firewall





### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a NGFW asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base\_url** |  required  | string | SMC IP address or hostname
**verify\_server\_cert** |  required  | boolean | Verify server certificate
**base\_port** |  required  | string | SMC API Port
**auth\_key** |  required  | password | SMC API Auth Key
**base\_version** |  required  | string | SMC Version \(e\.g\. 6\.2\)

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[block ip](#action-block-ip) - Block an IP  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'block ip'
Block an IP

Type: **contain**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP to block | string |  `ip` 
**group** |  required  | Group Name to add the IP | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip | string |  `ip` 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 