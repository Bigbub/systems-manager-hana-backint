# systems-manager-hana-backint
This implements a simple AWS Systems Manager Command Document that may be used to run a backup on a SAP HANA database, which has the AWS Backint Agent installed.

The Command Document supports backing up a HANA Multitenant Database Containers based database server, with a single tenant database.

### The following parameters are expected
- BackupType : may be full, incremental, differential
- SystemID : the System ID of the main HANA database server
- TenantSID : the System ID of the tenant database

This code is licensed under the Apache 2.0 license.
