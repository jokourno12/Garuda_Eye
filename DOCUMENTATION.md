# 🦅 GARUDA EYE - Security Observation Tool

**Version:** v1.0  
**Year:** 2026 - 2027

---

## 📖 SYNOPSIS

This is a script to scan ports on machines to try and identify running services.

---

## 📝 DESCRIPTION

This script will scan a range of ports on a target machine to try and identify running services.

---

## ⚙️ PARAMETERS

### `-help`
Displays this help message.

### `-pMin`
**Default:** `1`  
Minimum port number to scan.

### `-pMax`
**Default:** `65535`  
Maximum port number to scan.

### `-quickScan`
**Mutually exclusive** with selecting port numbers manually.  
Scans the top 1000 most common ports.

### `-verbose`
Will display each port's status (open or closed).

### `-targets`
Target machines to scan. Can be multiple comma-separated servers.

### `-ports`
Comma-separated ports to be scanned.

### `-discover`
Checks if a host or subnet is alive and reachable.

---

## 📚 EXAMPLES

### Example 1: Full Port Scan
```powershell
.\portScan.ps1 -targets 10.34.56.66, 10.34.56.67
```
**Description:** Full port scan of both targets.

---

### Example 2: Quick Scan
```powershell
.\portScan.ps1 -targets 10.34.56.66 -quickScan
```
**Description:** Scans the most common 1000 ports of the target.

---

### Example 3: Port Range
```powershell
.\portScan.ps1 -targets 10.34.56.66 -pMin 1024 -pMax 2000
```
**Description:** Scans ports 1024 to 2000 of the target.

---

### Example 4: Specific Ports
```powershell
.\portScan.ps1 -targets 10.34.56.66 -ports 21,22,23,25,80,443,8080,8443
```
**Description:** Scans the selected ports of the target.

---

### Example 5: Discover Single Target
```powershell
.\portScan.ps1 -targets 10.34.56.66 -discover
```
**Description:** Checks if the target is reachable.

---

### Example 6: Discover Subnet
```powershell
.\portScan.ps1 -targets 192.168.1.1/24 -discover
```
**Description:** Checks what hosts in the subnet are reachable.

---

### Example 7: With Verbose Output
```powershell
.\portsScan.ps1 -targets 10.34.56.66 -verbose *> test.txt
```
**Description:** Will include the output of each port scanned verbosely indicating open or closed. Also redirects output to `test.txt`.

---

## 📁 FILES

| File | Description |
|------|-------------|
| `garuda-eye.ps1` | Main script |
| `ports.txt` | Database of ports and services |
| `garuda-eye-functions.psm1` | Module functions |

---

## ⚠️ DISCLAIMER

Use this tool only on systems you own or have explicit permission to scan. Unauthorized port scanning may be illegal in some jurisdictions.

---

## 📞 SUPPORT

For issues or questions, please open an issue on GitHub.
