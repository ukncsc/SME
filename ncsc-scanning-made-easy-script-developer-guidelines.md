# NCSC Scanning Made Easy Script Developer Guidelines

## Introduction
Scanning Made Easy (SME) is a joint project between the i100 and the NCSC to build a collection of NMAP Scripting Engine scripts, designed to help system owners and administrators find systems with specific vulnerabilities.
When a software vulnerability is disclosed, it is often easier to find proof-of-concept code to exploit it, than it is to find tools that will help defend your network. To make matters worse, even when there is a scanning script available, it can be difficult to know if it is safe to run, let alone whether it returns valid scan results.  Scanning Made Easy (SME) was born out of our frustration with this problem and our desire to help network defenders find vulnerable systems, so they can protect them.
Should you be interested in developing a script for SME, more detail can be found below on how scripts should be produced, how the NCSC will approve, publication and through life management. 

## Testing
We ask that you thoroughly test any scripts developed and, where possible, keep testing artifacts so they can be reviewed by the NCSC if required.

## NCSC Approval of a Script
When considering whether a script meets the standard required to be part of Scanning Made Easy, the NCSC will determine whether the following mandatory requirements are met:

1.	written for NMAP using the NMAP Script Engine (.nse).
2.	relate to one of the high priority vulnerabilities impacting the UK;
3.	conform to the metadata template (see annex);
4.	run in isolation, i.e. no dependencies and does not connect to other servers;
5.	be as close to 100% reliable in detection of vulnerable instances as is practicable, i.e. low false-positive rate;
6.	be as unintrusive (i.e. not transmit excessive network traffic) and safe as possible in the detection mechanism;
7.	be hosted on a publicly available repository or website;
8.	be made freely available under a permissive open source licence;
9.	not to capture sensitive data, e.g., exposure of cyber security risk or personal;
10.	not to send data off the system upon which the script is run; and
11.	ability to write the output from the script to a file.

## Publishing
Once the script has been uploaded to a publicly available repository or website, contact the NCSC at https://www.ncsc.gov.uk/section/about-this-website/general-enquiries. We will check the script, and once assessed notify the community and link to it. NCSC will share a link to the specific version of the script checked.  You may also wish to contribute the script to NMAP. 
Subsequent Updates
Script authors should inform the NCSC at https://www.ncsc.gov.uk/section/about-this-website/general-enquiries of subsequent updates to the script. The NCSC will check the script and update the published link.  

Please also inform the NCSC if the script will no longer be supported.

## Association with NCSC
NCSC welcomes authors referring to their script being part of the NCSC's Scanning Made Easy programme by stating:
```
“Our scripts are published in accordance with the NCSC's guidelines for the Scanning Made Easy programme to provide organisations trusted scanning tools to identify their vulnerable systems. More information can be found here: https://github.com/ukncsc/sme”.
```
The NCSC does not approve the use of its logo by script authors.
 
# Annex - Required Metadata
Each script requires the following standard metadata at the top of the file:

```
--
-- Description
--
description = [[
VULNERABILITY DESCRIPTION AND CVE
We check for the presence of the vulnerability via:
  - ACTION A
  - ACTION B
This check is not intrusive, because:
 - REASON A
 - REASON B
This check may have False Positives if:
 - REASON A
 - REASON B
This check may have False Negatives if:
  - REASON A
  - REASON B
References:
* https://EXAMPLE/URL
]]

--
-- Author
--
author = "NAME at COMPANY"

--
-- License
---
license = "TYPE – HTTPS LINK"

--
-- Categories
--
categories = {"safe", "vuln"}
```

An example of a completed metadata entry is available here:

https://github.com/nccgroup/nmap-nse-vulnerability-scripts/blob/master/smtp-vuln-cve2020-28017-through-28026-21nails.nse
