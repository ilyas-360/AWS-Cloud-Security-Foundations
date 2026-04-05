# Future AWS Integration — In Active Development

This folder is the bridge from the on-premises enterprise networking foundation in this repository to production-grade cloud security engineering.

The CCNA lab established the fundamentals: VLAN segmentation, OSPF routing, HSRP failover, ACL hardening, management plane hardening. These are not background knowledge — they are direct prerequisites for designing secure AWS hybrid architectures.

## Active Project

I am currently building a **Zero Trust Multi-Account AWS Security Architecture** that implements these exact concepts at the cloud layer.

👉 **[github.com/ilyas-360/zero-trust-aws](https://github.com/ilyas-360/zero-trust-aws)**

## How This Repo Maps to That One

| On-Prem (this repo) | AWS Implementation (zero-trust-aws) |
|---|---|
| VLAN segmentation | VPC subnets + Security Groups + NACLs |
| ACL-based traffic filtering | Security Groups + Transit Gateway route tables |
| Management plane hardening | SCPs + IAM permission boundaries |
| HSRP / redundant routing | Transit Gateway + multi-AZ design |
| OSPF dynamic routing | BGP over Site-to-Site VPN to Transit Gateway |
| SSHv2 + least privilege | IAM role assumption chains + no persistent credentials |

## What Is Being Built There

- AWS Organizations with 5 dedicated accounts (Management, Security, Logging, Network, Workload)
- Service Control Policies enforced at the organization level
- IAM permission boundaries closing privilege escalation paths
- Site-to-Site VPN connecting simulated on-prem to AWS Transit Gateway
- Centralized GuardDuty, Security Hub, and CloudTrail across all accounts
- Full Terraform IaC — modular, documented, reproducible

**Status:** Architecture and SCP policies complete. Terraform modules in active development (April 2026).
