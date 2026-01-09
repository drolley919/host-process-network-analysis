# Host-Based Forensic Analysis

## Analysis Overview
The host-based forensic analysis focused on identifying suspicious activity through examination of running processes, active network connections, and associated executable files. The goal was to triage the live system, determine whether indicators of malicious activity were present, and assess whether escalation or remediation was necessary.

## Process Enumeration and Review
Running processes were enumerated to establish a baseline of system activity. Processes were reviewed based on name, execution path, and behavior to identify anomalies such as unexpected executables, unusual parent-child relationships, or processes running from non-standard directories.

## Network Connection Analysis
Active network connections were examined to identify external communications and listening services. Connections were reviewed for unusual destination addresses, unexpected ports, or persistent outbound activity that could indicate command-and-control behavior or unauthorized data transfer.

## Executable Validation
Executable files associated with suspicious or unknown processes were identified for further review. File properties were examined, and cryptographic hash values were generated to support validation efforts. Hashes were prepared for correlation with threat intelligence sources to assess potential malicious indicators.

## Correlation and Contextual Analysis
Findings from process and network analysis were correlated to provide context and reduce false positives. Legitimate system activity was differentiated from potentially suspicious behavior by reviewing execution context, expected system services, and known application behavior.

## Validation and Accuracy Checks
Analysis steps were documented and conducted in a repeatable manner to ensure accuracy. Observations were cross-referenced across multiple data points, including process information and network activity, to support reliable conclusions.
