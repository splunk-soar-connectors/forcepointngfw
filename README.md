[comment]: # "Auto-generated SOAR connector documentation"
# Forcepoint

Publisher: Martin Ohl  
Connector Version: 1.0.6  
Product Vendor: Forcepoint  
Product Name: Forcepoint NGFW  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 5.5.0  

This app integrates with Forcepoint Firewall


# Forcepoint Firewall

This app integrates with Forcepoint Firewall

### Configuration Variables

The below configuration variables are required for this Connector to operate. These variables are
specified when configuring a NGFW asset in SOAR.

| VARIABLE               | REQUIRED | TYPE     | DESCRIPTION                |
|------------------------|----------|----------|----------------------------|
| **base_url**           | required | string   | SMC IP address or hostname |
| **verify_server_cert** | required | boolean  | Verify server certificate  |
| **base_port**          | required | string   | SMC API Port               |
| **auth_key**           | required | password | SMC API Auth Key           |
| **base_version**       | required | string   | SMC Version (e.g. 6.2)     |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity
using supplied configuration  
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

| PARAMETER | REQUIRED | DESCRIPTION              | TYPE   | CONTAINS            |
|-----------|----------|--------------------------|--------|---------------------|
| **ip**    | required | IP to block              | string | `        ip       ` |
| **group** | required | Group Name to add the IP | string |                     |

#### Action Output

| DATA PATH                        | TYPE    | CONTAINS            |
|----------------------------------|---------|---------------------|
| action_result.parameter.ip       | string  | `        ip       ` |
| action_result.status             | string  |                     |
| action_result.message            | string  |                     |
| summary.total_objects            | numeric |                     |
| summary.total_objects_successful | numeric |                     |


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Forcepoint NGFW asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base_url** |  required  | string | SMC IP address or hostname
**verify_server_cert** |  required  | boolean | Verify server certificate
**base_port** |  required  | string | SMC API Port
**auth_key** |  required  | password | SMC API Auth Key
**base_version** |  required  | string | SMC Version (e.g. 6.2)

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[block ip](#action-block-ip) - Block an IP  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

Tests api cpnnectivity by making a login/logout call to SMC api.

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'block ip'
Block an IP

Type: **contain**  
Read only: **False**

Updates Bad IP list.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP to block | string |  `ip` 
**group** |  required  | Group Name to add the IP | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip | string |  `ip`  |  
action_result.status | string |  |  
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |  
action_result.data | string |  |  
action_result.summary | string |  |  
action_result.parameter.group | string |  |  