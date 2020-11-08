# systems-manager-hana-backint
This implements a simple AWS Systems Manager Command Document that may be used to run a backup on a SAP HANA database, which has the AWS Backint Agent installed.

The Command Document supports backing up a HANA Multitenant Database Containers based database server, with a single tenant database.

### The following parameters are expected
- BackupType : may be full, incremental, differential
- SystemID : the System ID of the main HANA database server

The code may be modified for multitenant databases with more than one tenant container, by adding additional instances of the final "sudo..." line and modifying it to support the tenant's SID.  Note that command documents do not directly support looping, so this needs to be done based on one line added per tenant DB.

This code is licensed under the Apache 2.0 license.
