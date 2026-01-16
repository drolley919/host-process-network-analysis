# Evidence and Data Collection

## Evidence Overview
This investigation relied on live-response data collected from an active Windows host during a host-based forensic triage. The evidence set was designed to capture volatile system state, including running processes and active network connections, to support rapid assessment of potential security risk.

## Evidence Sources
| Evidence Type | Description |
|--------------|-------------|
| Process Listings | Enumeration of active processes executing on the host system |
| Network Connections | Active TCP/UDP connections and listening services |
| Executable Artifacts | Executables associated with identified processes |
| Command Output | Output generated from native system and network diagnostic commands |

## Data Collection Methodology
Live-response data was collected using native operating system utilities and command-line tools to minimize system impact while preserving volatile information. Commands were executed in a controlled and documented sequence to capture an accurate snapshot of system and network activity at the time of investigation.

All collection actions were performed with a focus on rapid triage, consistent with SOC and DFIR operational practices.

## Validation and Corroboration
Executable files associated with suspicious or unknown processes were validated through cryptographic hash generation and threat intelligence correlation. Where applicable, multiple data sources were cross-referenced to confirm process legitimacy and network behavior.

This approach enabled differentiation between expected system activity and artifacts requiring additional scrutiny.

## Integrity and Reliability Considerations
Because live system analysis involves inherently volatile data, integrity was maintained through:
- Immediate capture and documentation of command output
- Consistent use of trusted, native system utilities
- Minimal system interaction beyond required investigative actions
- Correlation of findings across independent evidence sources

While live-response analysis does not provide the immutability of offline forensic imaging, these measures support reliable and defensible investigative conclusions.

## Host Network Configuration
The `ipconfig` command was executed to document the system’s active network interfaces, assigned IPv4 addresses, subnet masks, and default gateways at the time of analysis.

![Host network configuration using ipconfig](Assets/screenshots/host-network-configuration-ipconfig.png)

## Active Network Connections
The `netstat -ano` command was used to enumerate active TCP and UDP connections, listening ports, and associated process identifiers (PIDs). This information supported identification of network activity requiring contextual validation.

![Active network connections identified with netstat](Assets/screenshots/host-network-connections-netstat.png)

## Process Enumeration and PID Correlation
The `tasklist` command output was reviewed and correlated with network connection PIDs to associate active network activity with specific running processes.

This correlation was used to identify executables responsible for network communication and prioritize further analysis.

![Tasklist and netstat PID correlation](Assets/screenshots/tasklist-and-netstat-pid-correlation.png)
