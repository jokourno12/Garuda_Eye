# Garuda Eye - Security Observation Tool

## SYNOPSIS
This is a script to scan ports on machines to try and identify running services.

## DESCRIPTION
This script will scan a range of ports on a target machine to try and identify running services.

## PARAMETERS

### `-help`
Displays this help message.

### `-pMin`
Default = 1  
Minimum port number to scan

### `-pMax`
Default = 65535  
Maximum port number to scan

### `-quickScan`
Mutually exclusive with selecting port numbers manually.  
Scans the top 1000 most common ports.

### `-verbose`
Will display each port's status (open or closed).

### `-targets`
Target machines to scan. Can be multiple comma separated servers.

### `-ports`
Comma separated ports to be scanned.

### `-discover`
Checks if a host or subnet is alive and reachable.

## EXAMPLES

### Example 1: Full Port Scan
```powershell
.\portScan.ps1 -targets 10.34.56.66, 10.34.56.67