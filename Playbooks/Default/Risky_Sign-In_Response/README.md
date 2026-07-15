# Risky_Sign-In_Response
Automated investigation and response for risky authentication attempts



**Enabled:** False

**Version:** 0

**Type:** Playbook

**Priority:** 2

**Playbook Simulator:** False


### Playbook Trigger
**Trigger Type:** Custom Trigger

**Conditions Operator:** Or

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
|alert_name|Contains|Risky_Sign-In_Response|
|alert_name|Contains|Remote Login from High Risk Country|
|alert_name|Contains|Azure Successful Service Login from Tor|
|product|Equals|RULE|
|event_type|Equals|USER_LOGIN|


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Siemplify_Change Priority_2|Automatically change case priority to the given input|Siemplify|Change Priority|
|Siemplify_Change Priority_3|Automatically change case priority to the given input|Siemplify|Change Priority|
|Siemplify_Change Priority_1|Automatically change case priority to the given input|Siemplify|Change Priority|
|Insights_Create Entity Insight From Enrichment_1|The action creates an entity insight from an Enrichment action|Insights|Create Entity Insight From Enrichment|
|MandiantThreatIntelligence_Enrich Entities_1|Enrich entities using information from Mandiant. Supported entities: Hostname, IP Address, URL, Domain, File Hash, Threat Actor, Vulnerability. Note: only MD5, SHA-1 and SHA-256 are supported.|MandiantThreatIntelligence|Enrich Entities|
|Siemplify_Assign Case_2|Assign case to specific user or usergroup|Siemplify|Assign Case|
|Siemplify_Assign Case_1|Assign case to specific user or usergroup|Siemplify|Assign Case|

### Involved Blocks
|Name|Description|
|----|-----------|
|Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|High Risk Users Check|This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.|
test