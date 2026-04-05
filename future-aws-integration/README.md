# Future AWS Integration — In Active Development

This folder serves as the **bridge** from the on-premises enterprise networking foundation in this repository to production-grade AWS Cloud Security Engineering.

The CCNA lab here established core fundamentals (VLAN segmentation, OSPF routing, HSRP failover, ACL hardening, management plane security). These are direct prerequisites for secure hybrid cloud architectures.

## Active Project

I am currently building a **Zero Trust Multi-Account AWS Security Architecture** that applies these same principles at cloud scale.

👉 **[zero-trust-aws Repository](https://github.com/ilyas-360/zero-trust-aws)**

## Concept Mapping

| On-Prem (this repo)              | AWS Implementation (zero-trust-aws)                  |
|----------------------------------|-----------------------------------------------------|
| VLAN segmentation                | VPC subnets + Security Groups + NACLs               |
| ACL-based traffic filtering      | Security Groups + Transit Gateway route tables      |
| Management plane hardening       | SCPs + IAM permission boundaries                    |
| HSRP / redundant routing         | Transit Gateway + multi-AZ design                   |
| OSPF dynamic routing             | BGP over Site-to-Site VPN                           |
| SSHv2 + least privilege          | IAM role assumption chains + no persistent keys     |

## What Is Being Built in the New Project

- AWS Organizations with 5 dedicated accounts (Management, Security, Logging, Network, Workload)
- Organization-level Service Control Policies (SCPs)
- IAM permission boundaries to prevent privilege escalation
- Site-to-Site VPN for hybrid connectivity (on-prem simulation ↔ AWS Transit Gateway)
- Centralized observability (GuardDuty, Security Hub, Organization Trail CloudTrail)
- Full modular Terraform IaC

**Status (April 2026):** Architecture design and SCP policies complete. Terraform modules actively in development with daily commits. Verification screenshots and deployment outputs coming this week.

---

This foundation repo established the networking & security base.  
The new repo takes it to production-grade Zero Trust cloud security.

**Status:** Architecture and SCP policies complete. Terraform modules in active development (April 2026).
