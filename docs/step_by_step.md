[Azure Project Documentation Guide](/docs/azure_project_documentation)

# Azure Infrastructure Deployment — Step-by-Step Guide

This document outlines the process followed to deploy a secure, production-ready Azure environment.

---

## 1. Network Design
- Created three Virtual Networks:
  - **VNet1**: Main workloads
  - **VNet2**: Database layer
  - **VNet3**: Monitoring & backup

- Defined subnets within each VNet (e.g., web, app, database tiers).

---

## 2. Secure Access Setup
- Deployed Azure Bastion in VNet1 for secure, agentless RDP/SSH access.
- Configured Network Security Groups (NSGs) to control traffic at subnet and NIC levels.

---

## 3. Connectivity Configuration
- Established Virtual Network Peering between VNets for seamless communication.
- Configured Point-to-Site (P2S) VPN for admin access.
- Set up Site-to-Site (S2S) VPN to connect simulated on-premises resources.

---

## 4. Firewall & Routing
- Deployed Azure Firewall in a dedicated subnet.
- Configured User-Defined Routes (UDRs) to enable Forced Tunneling via the Firewall.
- Applied routing to direct outbound traffic through the Firewall for centralized control.

---

## 5. Identity & Secrets Management
- Applied Role-Based Access Control (RBAC) roles based on the principle of least privilege.
- Integrated Azure Key Vault to store sensitive data such as connection strings and secrets.

---

## 6. Monitoring & Logging
- Enabled Azure Monitor and Log Analytics to collect performance data and security logs.
- Configured alerts for key metrics including resource performance and security events.

---

## Notes
- All resources were tagged for effective cost management and organization.
- Deployment followed Microsoft’s Azure Well-Architected Framework best practices.

---

## Tools & Services Used
- Azure Portal
- ARM Templates
- PowerShell
###[Azure_Project_Documentation Guide](docs/azure_project_documentation)
