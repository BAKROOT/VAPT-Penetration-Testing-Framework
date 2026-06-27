# Network & Infrastructure Testing Checklist

Aligned with NIST SP 800-115 and OSSTMM. For internal and external network assessments. Mark each item Pass / Fail / N/A / Review and log failures as findings.

## Discovery
- [ ] Perform host discovery across in-scope ranges
- [ ] Identify live hosts and operating systems
- [ ] Map network topology where authorized

## Port & Service Scanning
- [ ] Full TCP port scan of in-scope hosts
- [ ] UDP scan of common services
- [ ] Service and version enumeration
- [ ] Identify unexpected/unauthorized services

## Service Enumeration
- [ ] Enumerate SMB/NetBIOS shares and permissions
- [ ] Enumerate SNMP (default community strings)
- [ ] Enumerate DNS (zone transfer, records)
- [ ] Enumerate LDAP / directory services
- [ ] Enumerate SMTP (open relay, user enumeration)
- [ ] Enumerate database services exposure

## Vulnerability Identification
- [ ] Identify missing patches and outdated software
- [ ] Identify default or weak credentials on services
- [ ] Identify known CVEs on exposed services
- [ ] Validate scanner findings manually

## Authentication & Access
- [ ] Test for weak/default credentials on management interfaces
- [ ] Test remote access services (RDP, SSH, VPN) configuration
- [ ] Review exposed administrative interfaces

## Network Security Controls
- [ ] Assess firewall rule effectiveness / segmentation
- [ ] Test for VLAN hopping / segmentation bypass (where authorized)
- [ ] Review wireless security (if in scope)
- [ ] Check for cleartext protocols (Telnet, FTP, HTTP)

## Configuration Review
- [ ] Review TLS/SSL configuration on services
- [ ] Identify insecure service configurations
- [ ] Check for unnecessary exposed services

## Post-Exploitation (Authorized)
- [ ] Assess lateral movement potential
- [ ] Assess privilege escalation opportunities
- [ ] Document attack paths without disrupting production
