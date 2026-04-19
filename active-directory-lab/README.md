# Active Directory Lab (Azure)

## 📌 Overview
This lab demonstrates building a complete Active Directory environment in Microsoft Azure.  
It includes virtual network setup, domain controller deployment, DNS configuration, user management, and domain joining a client machine.

---

## 🧱 Environment
- Microsoft Azure
- Windows Server (Domain Controller)
- Windows 10/11 (Client Machine)
- Active Directory Domain Services (AD DS)

---

## ⚙️ Deployment & Configuration

### 🔹 1. Resource Group & Networking

Created a resource group and virtual network to host the lab environment.

![Resource Group](./screenshots/ad-01-resource-group-created.png)
![Virtual Network](./screenshots/ad-02-virtual-network-created.png)

---

### 🔹 2. Domain Controller Setup

Provisioned a Windows Server VM and configured networking and security rules.

![DC VM Creation](./screenshots/ad-03-dc1-vm-creation.png)
![DC Network Config](./screenshots/ad-04-dc1-network-config.png)
![NSG Rules](./screenshots/ad-05-dc1-nsg-rules.png)
![Static IP](./screenshots/ad-06-dc1-private-ip-static.png)

---

### 🔹 3. Client Machine Setup

Created a client VM and configured DNS to point to the domain controller.

![Client VM](./screenshots/ad-07-client1-vm-creation.png)
![Client Network](./screenshots/ad-08-client1-network-config.png)
![Default DNS](./screenshots/ad-09-client1-dns-default.png)
![Custom DNS](./screenshots/ad-10-client1-dns-custom-dc.png)

---

### 🔹 4. Connectivity Verification

Verified connectivity between client and domain controller.

![Ping Success](./screenshots/ad-12-ping-dc1-success.png)
![DNS Verification](./screenshots/ad-13-ipconfig-dns-verification.png)

---

### 🔹 5. Active Directory Installation

Installed Active Directory Domain Services on the domain controller.

![Add Roles](./screenshots/ad-14-add-roles-start.png)
![Installation Type](./screenshots/ad-15-installation-type.png)
![Server Selection](./screenshots/ad-16-server-selection.png)
![AD DS Installed](./screenshots/ad-17-ad-ds-role-added.png)
![Installation Complete](./screenshots/ad-18-ad-ds-installation-complete.png)

---

### 🔹 6. Domain Configuration

Promoted the server to a domain controller and created a new forest.

![Create Forest](./screenshots/ad-19-create-new-forest.png)
![DNS Options](./screenshots/ad-20-dns-options.png)
![Prerequisites Check](./screenshots/ad-21-prerequisites-check.png)

---

### 🔹 7. Active Directory Structure

Configured organizational units (OUs) and directory structure.

![AD Overview](./screenshots/ad-22-active-directory-overview.png)
![Employees OU](./screenshots/ad-23-create-employees-ou.png)
![Admins OU](./screenshots/ad-24-create-admins-ou.png)

---

### 🔹 8. User & Permissions Management

Created administrative users and assigned appropriate permissions.

![Create Admin User](./screenshots/ad-25-create-admin-user.png)
![Admin Created](./screenshots/ad-26-admin-user-created.png)
![Add to Domain Admins](./screenshots/ad-27-add-user-to-domain-admins.png)

---

### 🔹 9. Domain Join & Organization

Joined the client machine to the domain and organized it within Active Directory.

![Join Domain](./screenshots/ad-28-client-join-domain.png)
![Client in AD](./screenshots/ad-29-client-in-ad-computers.png)
![Move to OU](./screenshots/ad-30-move-client-to-clients-ou.png)

---

## ✅ Key Skills Demonstrated
- Azure resource deployment and networking
- Active Directory Domain Services (AD DS)
- DNS configuration and troubleshooting
- User and group management
- Organizational Unit (OU) design
- Domain joining and endpoint management

---

## 📎 Summary
This lab simulates a real-world enterprise environment where a domain controller is deployed, users are managed, and client machines are integrated into the domain.

It demonstrates foundational system administration and help desk skills relevant to IT support roles.
