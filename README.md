# NCSC Scanning Made Easy Script Developer Guidelines

## Introduction
Scanning Made Easy (SME) is a joint project between the i100 and the NCSC to build a collection of NMAP Scripting Engine scripts, designed to help system owners and administrators find systems with specific vulnerabilities.
When a software vulnerability is disclosed, it is often easier to find proof-of-concept code to exploit it, than it is to find tools that will help defend your network. To make matters worse, even when there is a scanning script available, it can be difficult to know if it is safe to run, let alone whether it returns valid scan results.  Scanning Made Easy (SME) was born out of our frustration with this problem and our desire to help network defenders find vulnerable systems, so they can protect them.
Should you be interested in developing a script for SME, more detail can be found below on how scripts should be produced, how the NCSC will approve, publication and through life management. 


## Contributing

When considering whether a script meets the standard required to be part of Scanning Made Easy, the NCSC will determine whether the mandatory requirements are met. For more details including the developer guidelines please refer to the following page. 

- [Developer Guidelines](ncsc-scanning-made-easy-script-developer-guidelines.md)


## Approved NMAP Scripts

We would encourage you to review any scripts before running across your networks. Each script will contain information regarding:

- How it checks for the presence of the vulnerability
- Why the check is not intrusive
- Why there may be False Positives
- Why there may be False Negatives

The NMAP scripts below are pinned to the release that was validated by NCSC, it is possible additional updates are availiable, however these may not have been vetted as part of the Scanning Made Easy Process. 

####  Exim message transfer agent

*Exim remote code execution via CVE-2020-28017 through CVE-2020-28026 also known as 21Nails*

https://github.com/nccgroup/nmap-nse-vulnerability-scripts/tree/04d5c186b784f3880c033faec102b3a480268608