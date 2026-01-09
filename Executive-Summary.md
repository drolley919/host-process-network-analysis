# Executive Summary

## Case Overview
This project documents a host-based forensic investigation conducted on a live system to identify potentially suspicious processes and network activity. The investigation focused on analyzing running processes, active network connections, and executable files to assess whether malicious activity was present and determine if escalation or remediation was required.

## Scope of Investigation
The scope of this investigation included live system analysis of running processes, identification of active network connections, examination of executable file properties, and validation of suspicious artifacts through hash analysis and threat intelligence correlation. The investigation was conducted using command-line tools and system utilities commonly leveraged during SOC and DFIR triage activities.

## High-Level Findings
Analysis identified multiple running processes and active network connections requiring further scrutiny. Several executables were reviewed for legitimacy through file inspection and hash validation. Threat intelligence correlation was used to assess potential malicious indicators, and network activity was evaluated to determine whether connections were expected or anomalous.

## Risk and Impact
Unauthorized or malicious processes running on an endpoint can enable persistence, data exfiltration, or lateral movement within an environment. Suspicious network connections increase the risk of command-and-control communication or unauthorized data transfer if not promptly identified and contained.

## Recommended Actions
Based on the investigation, recommendations included continued monitoring of endpoint processes, validation of unknown executables, enhanced network traffic visibility, and escalation of confirmed suspicious activity for containment and remediation. Additional endpoint hardening and user awareness measures were advised to reduce future risk.
