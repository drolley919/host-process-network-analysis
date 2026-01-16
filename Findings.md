# Investigation Findings

## Summary of Findings
The host-based forensic investigation did not identify evidence of malicious activity on the examined system. While multiple running processes and active network connections were observed, all activity aligned with expected behavior for a live Windows host under normal user operation.

Process activity, network communications, and executable artifacts were analyzed and validated using native system utilities and external threat intelligence sources. No indicators of compromise, unauthorized persistence mechanisms, or suspicious executable behavior were identified.

---

## Network Activity Findings
Analysis of active network connections identified multiple established TCP and UDP sessions, including outbound connections over standard service ports such as 80 and 443. These connections were consistent with legitimate web browsing activity and standard Windows operating system services.

No anomalous listening ports, suspicious destination IP addresses, or persistent outbound connections indicative of command-and-control communication were observed.

**Supporting Evidence – Active Network Connections (netstat):**  
![Active network connections identified with netstat](Assets/screenshots/host-network-connections-netstat.png)

---

## Process Analysis Findings
Process enumeration identified standard Windows system processes and user-initiated applications operating from expected directories. No unauthorized executables, suspicious execution paths, or abnormal parent-child process relationships were observed.

Processes associated with active network connections were reviewed and found to correspond with legitimate applications performing expected functions.

**Supporting Evidence – Process Enumeration and PID Correlation:**  
![Tasklist and netstat PID correlation](Assets/screenshots/tasklist-and-netstat-pid-correlation.png)

![Process and network correlation](Assets/screenshots/host-process-network-correlation.png)

---

## Executable Validation Findings
Executable validation was performed on selected binaries associated with active network connections. Cryptographic hash values were generated and correlated with external threat intelligence sources.

Reviewed executables, including `msedge.exe`, were confirmed as legitimate, digitally signed binaries with no malicious detections reported. These results support the conclusion that observed network activity originated from trusted applications.

**Supporting Evidence – Executable Validation (VirusTotal):**  
![VirusTotal analysis of msedge.exe](Assets/screenshots/virustotal-analysis-msedge.exe.png)

---

## Correlation Findings
Correlation of process activity, network connections, and executable validation results demonstrated consistent and expected system behavior. Active network communications were successfully attributed to legitimate running processes, and associated binaries were verified as trusted.

No inconsistencies or anomalies were identified that would suggest malicious execution, unauthorized persistence, or suspicious network behavior.

---

## Overall Assessment
Based on the evidence collected and analyzed, the system exhibited no indicators of compromise at the time of investigation. All observed activity was consistent with normal Windows host behavior during active use.

The investigation confirms the absence of malicious processes, unauthorized network communications, or suspicious executable execution. Continued monitoring and standard endpoint security controls are recommended to maintain system integrity.
