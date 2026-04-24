# 🌐 DNS Lab – Building Intuition for Name Resolution

## 📌 Overview
This lab demonstrates how DNS (Domain Name System) works in a Windows Server environment. It covers creating DNS records, understanding DNS caching behavior, and troubleshooting name resolution issues. This simulates real-world IT support scenarios where users cannot access systems due to DNS-related problems.

---

## 🧰 Technologies Used
- Microsoft Azure (Virtual Machines)
- Windows Server (Domain Controller)
- Windows 10 (Client Machine)
- DNS Manager
- Command Prompt

---

## 🧪 Lab Objectives
- Troubleshoot failed DNS resolution
- Create and modify DNS A records
- Understand DNS caching behavior
- Configure and test CNAME records

---

## 🔹 Step 1: Verify DNS Failure
From Client-1, attempt to resolve a hostname that does not exist:

ping mainframe  
nslookup mainframe  

❌ Result: Host not found (no DNS record exists)

---

## 🔹 Step 2: Create A Record
On DC-1 (Domain Controller):
- Open DNS Manager
- Create a new A Record  
  - Name: mainframe  
  - IP Address: DC-1 Private IP  

---

## 🔹 Step 3: Verify Resolution
From Client-1:

ping mainframe  

✅ Result: Host resolves successfully

---

## 🔹 Step 4: Modify DNS Record
On DC-1, change the `mainframe` A record IP address to:

8.8.8.8  

---

## 🔹 Step 5: Observe DNS Cache Behavior
From Client-1:

ping mainframe  

⚠️ Result: Still resolves to old IP address due to DNS cache

---

## 🔹 Step 6: View DNS Cache

ipconfig /displaydns  

This shows locally cached DNS entries.

---

## 🔹 Step 7: Flush DNS Cache

ipconfig /flushdns  

This clears the cached DNS records.

---

## 🔹 Step 8: Verify Updated Record

ping mainframe  

✅ Result: Now resolves to the updated IP (8.8.8.8)

---

## 🔹 Step 9: Create CNAME Record
On DC-1:
- Create a CNAME Record  
  - Alias: search  
  - Target: www.google.com  

---

## 🔹 Step 10: Test CNAME Record

ping search  
nslookup search  

✅ Result: Host resolves to Google via CNAME

---

## 🧠 Key Takeaways
- DNS translates human-readable names into IP addresses  
- A records map names → IP addresses  
- CNAME records map names → other domain names  
- DNS caching can cause outdated resolution results  
- Flushing the cache ensures updated DNS records are used  

---

## 🚀 Real-World Application
This lab reflects common IT support tasks:
- Troubleshooting “cannot reach server” issues  
- Fixing DNS misconfigurations  
- Understanding cached vs updated DNS records  
- Supporting users with connectivity problems  

---

## 📁 Project Files
All screenshots for this lab are stored in the `screenshots/` folder.
