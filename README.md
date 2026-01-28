# Wireshark HTTP Traffic Analysis – Credential Exposure

## 📌 Project Overview
This project demonstrates how insecure **HTTP traffic** can expose sensitive information such as login credentials. Using **Wireshark**, I captured and analyzed network traffic to identify a login request sent over HTTP and extracted the credentials transmitted in clear text.

This project was conducted in a **controlled lab environment** using intentionally vulnerable test websites for educational purposes only.

---

## 🎯 Objectives
- Capture network traffic using Wireshark
- Identify HTTP login requests
- Analyze packet contents
- Demonstrate how credentials are exposed over HTTP
- Understand why HTTPS is critical for secure communication

---

## 🛠 Tools Used
- Wireshark
- Web browser
- HTTP test login page (intentionally vulnerable)
- Ubuntu / Kali Linux (lab environment)

---

## 🔍 Methodology

### 1. Traffic Capture
- Started packet capture on the active network interface
- Accessed an HTTP login page (testphp.vulnweb.com)
- Entered test credentials (user:admin password:1234password)
<img width="2560" height="1440" alt="screen shot 2" src="https://github.com/user-attachments/assets/076eb69e-8f57-4fd2-95e1-6037dcf1542a" />

### 2. Filtering Traffic
- http
- tcp.stream eq 

---

### 3. Packet Analysis
- Located HTTP POST request containing login data
- Inspected packet details and payload
- Identified username and password transmitted in plain text
<img width="2560" height="1440" alt="screen shot 3" src="https://github.com/user-attachments/assets/04c837d4-f67f-4287-8ec8-83dee39e2750" />
<img width="2560" height="1440" alt="screen shot 1" src="https://github.com/user-attachments/assets/6df3e962-9b84-4b63-920a-b7fb09907a98" />

---

## ⚠️ Findings
- Login credentials were transmitted **unencrypted**
- Username and password were visible in the packet payload
- Demonstrates a major security risk of using HTTP for authentication

---

## 🛡 Security Implications
- Attackers on the same network can intercept credentials
- HTTP should never be used for login forms
- HTTPS encrypts data and prevents credential sniffing

---

## 📚 Lessons Learned
- Importance of HTTPS and TLS encryption
- How attackers sniff credentials
- How SOC analysts identify insecure traffic
- Practical experience using Wireshark filters and packet inspection

---

## ⚖️ Disclaimer
This project was performed in a **legal, controlled lab environment** using test credentials and vulnerable applications for educational purposes only.
