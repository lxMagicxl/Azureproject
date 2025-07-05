# Step-by-Step Azure Infrastructure Deployment Guide

This document details the exact steps I followed to deploy the secure Azure infrastructure.

---

## 1️⃣ Network Architecture Design:
- Created **3 Virtual Networks (VNets)**:
  - VNet1: For main workloads
  - VNet2: For database layer
  - VNet3: For backup & monitoring

- Subnet segmentation per VNet (e.g., Web, App, DB subnets).

---

## 2️⃣ Secure Access Configuration:
- Deployed **Azure Bastion** in VNet1 for secure RDP/SSH access to VMs.
- Configured **Network Security Groups (NSGs)** to allow only required inbound/outbound traffic.

---

## 3️⃣ Connectivity Setup:
- Configured **VNet Peering** to enable communication between VNets.
- Established **Point-to-Site (P2S)** VPN for admin remote access.
- Configured **Site-to-Site (S2S)** VPN for on-premises connectivity (lab simulated).

---

## 4️⃣ Firewall & Routing:
- Deployed **Azure Firewall** in a dedicated subnet.
- Created custom **route tables** for Forced Tunneling via Firewall.
- Applied routing rules to route all outbound traffic through Firewall.

---

## 5️⃣ Identity & Secrets Management:
- Assigned **RBAC roles** to limit permissions following the principle of least privilege.
- Integrated **Azure Key Vault** to securely store and retrieve secrets (e.g., connection strings, passwords).

---

## 6️⃣ Monitoring & Alerts:
- Enabled **Azure Monitor** and **Log Analytics** for system monitoring and centralized log collection.
- Configured alerts for performance thresholds, unauthorized access attempts, and firewall events.

---

## ✅ Tools Used:
- Azure Portal
- Azure Resource Manager (ARM)
- PowerShell

---

## 💡 Notes:
- All resources were tagged for cost management and resource organization.
- Security best practices were followed according to Microsoft’s Azure Well-Architected Framework.

---

