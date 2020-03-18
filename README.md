# Kinesis Data Firehose Helper
## Splunk App to help troubleshoot AWS Kinesis Data Firehose HEC issues

### Overview

This app was developed to help users troubleshoot common issues with connecting to Kinesis Data Firehose from Splunk. It's divided into three secions.

#### Section 1 - HEC URL Tests
This section creates a HEC URL to test the health of the HEC endpoint. If you click on the link and do not get this code, then the endpoint is unlhealthy.

`{"text":"HEC is healthy","code":17}`

### Section 2 - Nslookup Hosts
This section validates that the HEC Endpoints resolve to a load balancer. Typically, there should be three IP's listed.

### Section 3 - cURL testing
You can copy and paste the commands in a terminal and run it to test to see if the data comes back properly. There are two cURL commands, one for standard HEC and the other for Firehose HEC which requires indexer ACK enabled, sticky sessions enabled on the ELB and a valid SSL Cert.


