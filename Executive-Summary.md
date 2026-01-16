# Executive Summary

## Case Overview
This project documents a host-based forensic investigation performed on a live Windows system to assess running processes and active network connections for signs of suspicious or unauthorized activity. The investigation simulates a real-world SOC and incident response triage scenario, focusing on rapid identification, validation, and risk assessment of host-level activity.

## Scope of Investigation
The investigation focused on live system analysis, including:
- Enumeration of running processes
- Identification and review of active network connections
- Examination of executable file properties and metadata
- Validation of suspicious artifacts using cryptographic hash analysis and threat intelligence correlation

All analysis was conducted using native command-line tools and system utilities commonly leveraged during SOC and DFIR investigations.

## High-Level Findings
The analysis identified multiple running processes and network connections requiring contextual validation. Executable files associated with active processes were examined to determine legitimacy through file inspection and hash verification. Network connections were reviewed to assess whether communication patterns aligned with expected system behavior or indicated potential anomalies.

No immediate evidence of confirmed malware was identified during the initial triage; however, several artifacts warranted continued monitoring and follow-up validation.

## Risk and Impact Assessment
Unverified or unauthorized processes on an endpoint can introduce risk, including persistence mechanisms, data exfiltration, or lateral movement opportunities. Suspicious or unexplained network connections increase exposure to command-and-control activity or unauthorized external communication if left unaddressed.

Early detection and validation at the host level is critical to reducing dwell time and limiting potential operational impact.

## Recommended Actions
Based on investigative findings, the following actions were recommended:
- Continued monitoring of endpoint process activity
- Validation and reputation analysis of unknown executables
- Improved visibility into outbound network connections
- Escalation of confirmed suspicious activity for containment and remediation
- Strengthening endpoint hardening and user awareness controls to reduce future risk
