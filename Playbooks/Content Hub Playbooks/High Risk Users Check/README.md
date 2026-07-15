# High Risk Users Check
This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False


##### Input Parameters
|Name|Default Value|
|----|-------------|


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Retrieve Relevant Users|Search a specified string within the records of an environment's custom list. (If no values are provided will return all custom lists records)|Lists|Search Environment Custom Lists|
|Add High Severity Record|This action will add an entry to the alert scoring database.  Alert score is based off the ratio: 5 Low = 1 Medium.  3 Medium = 1 High.  2 High = 1 Critical.  Optional tag added to case.|Tools|Add Alert Scoring Information|
|Find Matches|This action will render a Jinja2 template using a JSON input.  |TemplateEngine|Render Template|

