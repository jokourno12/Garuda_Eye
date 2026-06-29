# GARUDA EYE
![image](https://img.shields.io/badge/powershell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)

![demo](demos/demo-garuda-eye.gif)

Garuda Sense is a PowerShell-based, multithreaded platform for probing remote hosts and identifying open TCP ports without requiring elevated privileges.

## Features

- **Multithreaded Scanning**: Fast parallel host and port scanning.
- **Host Discovery**: Detects reachable hosts, including CIDR subnet support.
- **Flexible Targeting**: Scan single, multiple, or subnet targets.
- **Multiple Scan Modes**: Quick, full, or custom port scanning.
- **Service Detection**: Identifies services using the IANA port database.
- **PowerShell Native**: Runs without administrative privileges or external dependencies.

## Requirements

- **PowerShell 7.6.3 or later**
- **Currently does not rely on additional dependencies**

## Color Indicators

- **Yellow**: Blockchain.
- **Red**: Vulnerability Assessment and Penetration Testing.
- **Magenta**: Incident Handling and Response.
- **Blue**: Network Defense.
- **Green**: Application Security.

## Installation

Clone the repository or download the scripts directly:

```bash
git clone https://github.com/jokourno12/Garuda_Eye.git
```
## Examples

### Full port scan of multiple targets
`.\garuda-eye.ps1 -targets 10.34.56.66,10.34.56.67`

### Quick scan using the predefined common port list
`.\garuda-eye.ps1 -targets 10.34.56.66 -quickScan`

### Scan a custom port range (1024 to 2000) on a single target
`.\garuda-eye.ps1 -targets 10.34.56.66 -pMin 1024 -pMax 2000`

### Scan specific ports on a single target
`.\garuda-eye.ps1 -targets 10.34.56.66 -ports 21,22,23,25,80,443,8080,8443`

### Check whether a host is reachable
`.\garuda-eye.ps1 -targets 10.34.56.66 -discover`

### Discover live hosts in a subnet
`.\garuda-eye.ps1 -targets 192.168.1.0/24 -discover`

### Generate verbose output and redirect it to a text file
`.\garuda-eye.ps1 -targets 10.34.56.66 -Verbose *> test.txt`

### Display debugging information with scan results
`.\garuda-eye.ps1 -targets 8.8.8.8 -quickScan -InformationAction Continue`
