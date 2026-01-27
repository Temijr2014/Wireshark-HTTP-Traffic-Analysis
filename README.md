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

### 2. Filtering Traffic
- http
- tcp.stream eq 
