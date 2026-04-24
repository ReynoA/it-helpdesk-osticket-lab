# 📁 Network File Shares & Permissions Lab

## 📌 Overview
This lab demonstrates how to configure file shares and manage access permissions in a Windows Server environment using Active Directory.

It simulates real-world IT support scenarios where users require specific access to shared resources based on roles and group membership.

---

## 🧰 Technologies Used
- Microsoft Azure (Virtual Machines)
- Windows Server (Domain Controller)
- Windows 10 (Client Machine)
- Active Directory (ADUC)
- File Explorer (NTFS Permissions & Sharing)

---

## 🧪 Lab Objectives
- Create and share folders with different permission levels
- Assign permissions to users and groups
- Test access from a client machine
- Use security groups to control access

---

## 🔹 Step 1: Create Shared Folders
On DC-1, created the following folders:

- read-access
- write-access
- no-access
- accounting

---

## 🔹 Step 2: Configure Permissions

Assigned permissions as follows:

- read-access → Domain Users → Read
- write-access → Domain Users → Read/Write
- no-access → Domain Admins → Read/Write

---

## 🔹 Step 3: Test Access as Normal User

From Client-1:
- Navigated to shared folders using:

\\dc-1

Observed:
- Read access works for read-access
- Write access works for write-access
- Access denied for no-access

---

## 🔹 Step 4: Create Security Group

In Active Directory:
- Created a group named:

ACCOUNTANTS

---

## 🔹 Step 5: Assign Group Permissions

On the “accounting” folder:
- Assigned:
  - Group: ACCOUNTANTS
  - Permission: Read/Write

---

## 🔹 Step 6: Test Access Before Group Membership

- Logged in as normal user
- Attempted to access accounting folder

❌ Result: Access denied

---

## 🔹 Step 7: Add User to Group

- Added user to ACCOUNTANTS group in Active Directory

---

## 🔹 Step 8: Test Access After Group Membership

- Logged back into Client-1
- Attempted access again

✅ Result: Access granted

---

## 🧠 Key Takeaways
- NTFS and share permissions control access to resources
- Security groups simplify permission management
- Access issues are often related to group membership
- Logging out and back in refreshes group policies
- Proper permission configuration is critical for security

---

## 🚀 Real-World Application
This lab simulates common IT support tasks:
- “User can’t access shared folder”
- “User needs access to department files”
- Managing permissions using groups instead of individuals
- Troubleshooting access denied errors

---

## 📁 Project Files
All screenshots for this lab are stored in the `screenshots/` folder.
