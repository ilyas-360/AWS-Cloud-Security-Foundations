# AWS Cloud Security Foundations
## Hybrid Networking & Security Architecture
### CCNA → AWS Cloud Security Engineering

This repository documents my enterprise networking foundation as I transition from CCNA-level infrastructure engineering toward AWS Cloud Security Engineering. It demonstrates how on-prem enterprise network security principles translate directly into AWS hybrid cloud architectures.

---

## 🎯 Project Objective

Design and implement a secure, highly available enterprise network architecture that provides:

- Traffic segmentation and isolation (VLAN-based)
- Redundant routing and failover (HSRP, OSPF)
- Hardened management and control planes
- A solid foundation for AWS hybrid connectivity (VPN / Direct Connect)

This project establishes the networking and security fundamentals required to secure AWS hybrid cloud environments.

---

## 🛡️ Security Architecture

### Zero Trust Network Foundation

- Port Security & DHCP Snooping (hardware trust layer)
- VLAN-based segmentation (conceptually mapped to AWS Security Groups & NACLs)
- Management plane hardening (SSHv2, ACL restrictions)
- Least privilege access enforcement

### AWS Conceptual Translation

These principles directly map to:

- AWS VPC and subnet architecture
- Security Group and Network ACL design
- AWS Site-to-Site VPN security posture
- Direct Connect private virtual interfaces

---

## 🛠️ Technical Implementation

### High Availability
- HSRP for default gateway redundancy
- EtherChannel with LACP for link aggregation
- Redundant core / distribution layer design

### Routing & Connectivity
- OSPF for dynamic routing
- Multi-area OSPF (scalability foundation)
- Prepared for future BGP integration with AWS

### Traffic Control
- NAT / PAT with logging
- ACL-based traffic filtering
- VLAN-based segmentation and isolation

---

## 📁 Repository Structure

```
AWS-Cloud-Security-Foundations/
├─ configs/                   # Device configurations (Core, Distribution, Access, Edge)
├─ design-docs/               # Topology diagrams, addressing plans, segmentation logic
├─ security-controls/         # Management hardening, port security, DHCP snooping
├─ verification/              # Connectivity tests, security validation + screenshots
├─ enterprise-hybrid-security-lab.pka   # Full interactive Packet Tracer lab (100% completed)
└─ future-aws-integration/    # Bridge to active Zero Trust AWS project

---

🚀 Next Phase: AWS Integration — In Active Development
This on-prem foundation is now being extended into production-grade cloud security.

👉 **[zero-trust-aws](https://github.com/ilyas-360/zero-trust-aws)**  
Zero Trust Multi-Account AWS Security Architecture (Terraform IaC, SCPs, IAM permission boundaries, hybrid VPN, GuardDuty + Security Hub, etc.)

See `future-aws-integration/` for the conceptual mapping (VLAN segmentation → Security Groups/NACLs, ACL hardening → AWS guardrails, etc.).

## 📚 Skills Demonstrated

- Enterprise network design and implementation
- VLAN segmentation and traffic isolation
- High-availability protocols (HSRP, EtherChannel)
- Dynamic routing (OSPF)
- Network security hardening
- Technical documentation and verification

Foundation for: AWS VPC architecture, hybrid cloud security, infrastructure-as-code

---

## 👤 Author

**Ilyas Benkhadra**
Cloud Security Engineering | AWS SAA-C03 ✅ March 2026 | CCNA ✅

🔗 LinkedIn: https://www.linkedin.com/in/ilyas-benkhadra-a118582b4/
💻 GitHub: https://github.com/ilyas-360
📧 Email: ilyasbenkhadra10@gmail.com
📍 Morocco
