# Cloud Security Testing Checklist

Aligned with CIS Benchmarks and cloud provider best practices (AWS, Azure, GCP). Cloud testing must comply with the provider's penetration testing policy and the engagement ROE. Mark each item Pass / Fail / N/A / Review and log failures as findings.

> **Note:** Confirm the cloud provider's rules of engagement and any required notifications before testing managed services.

## Identity & Access Management
- [ ] Review IAM users, roles, and policies for least privilege
- [ ] Identify overly permissive policies (wildcards on actions/resources)
- [ ] Check for unused credentials and stale access keys
- [ ] Verify MFA enforced for privileged accounts
- [ ] Review root/global-admin account usage and protection
- [ ] Check for privilege escalation paths in IAM

## Storage
- [ ] Identify public buckets/blobs and object ACLs
- [ ] Verify encryption at rest for storage
- [ ] Review storage access logging
- [ ] Check for sensitive data in publicly accessible storage

## Compute
- [ ] Review instance/VM security groups and firewall rules
- [ ] Identify instances with public IPs and exposed services
- [ ] Check instance metadata service exposure (IMDSv2 / SSRF risk)
- [ ] Review patching and image hardening

## Networking
- [ ] Review VPC/VNet segmentation and peering
- [ ] Identify overly permissive security group / NSG rules
- [ ] Review exposed load balancers and endpoints
- [ ] Verify private endpoints for sensitive services

## Logging & Monitoring
- [ ] Verify audit logging enabled (CloudTrail / Activity Log / Audit Logs)
- [ ] Verify logs protected from tampering
- [ ] Review alerting on suspicious activity

## Data Protection & Keys
- [ ] Review key management (KMS) configuration and rotation
- [ ] Verify encryption for databases and managed services
- [ ] Check for secrets in environment variables / code / metadata

## Serverless & Managed Services
- [ ] Review function permissions and triggers
- [ ] Review managed database exposure and authentication
- [ ] Review container registry and orchestration (K8s) security

## Configuration Baseline
- [ ] Run against CIS Benchmark for the provider
- [ ] Identify drift from secure baseline
