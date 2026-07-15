# Chronicle_Alerts _Mail




**Enabled:** False

**Version:** 0

**Type:** Playbook

**Priority:** 2

**Playbook Simulator:** False


### Playbook Trigger
**Trigger Type:** All

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
||Equals||


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Tools_Change Case Name_1|The action changes the case's name (title)|Tools|Change Case Name|
|MicrosoftGraphMail_Send Email_1|Send email from a specific mailbox to an arbitrary list of recipients. Action can send either plain text or html emails. If permissions allow, action can send an email from a mailbox different that is specified in the integration configuration. Note: Action is not running on Chronicle entities.|MicrosoftGraphMail|Send Email|
|Siemplify_Create Gemini Case Summary_1|Create a summary of the case using Gemini AI.|Siemplify|Create Gemini Case Summary|

### Involved Blocks
|Name|Description|
|----|-----------|
|Auto close of email exceed|An embedded workflow that can receive inputs and return an output.|
test