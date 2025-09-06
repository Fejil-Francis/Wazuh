# 🛡️ Wazuh

**Wazuh** is a free and open-source **security platform** that provides unified protection for endpoints, cloud workloads, and on-premises systems.  
It acts as a **SIEM (Security Information and Event Management)** and **XDR (Extended Detection and Response)** solution, helping organizations detect threats, monitor activity, and maintain compliance.

---

## 🚀 Features
- 📊 **Log Data Analysis** – Collect and analyze security events from multiple sources  
- 🕵️ **Intrusion Detection** – Detect malware, anomalies, and unauthorized activity  
- 🔒 **File Integrity Monitoring (FIM)** – Watch for changes in sensitive files  
- 👮 **Compliance Management** – Meet standards like PCI DSS, GDPR, HIPAA, etc.  
- 🌐 **Cloud Security** – Monitor AWS, Azure, GCP environments  
- 📡 **Centralized Dashboard** – Web-based interface for real-time visibility  

---

## 🖥️ Components
- **Wazuh Manager** – Analyzes data and generates alerts  
- **Wazuh Agent** – Installed on endpoints to collect logs and security events  
- **Wazuh Indexer** – Stores and indexes security data  
- **Wazuh Dashboard** – Web UI for visualization and monitoring  

---


## 📦 Installation 

Clone the Wazuh Docker repository:

```bash
git clone https://github.com/wazuh/wazuh-docker.git -b v4.12.0
```
<img width="811" height="404" alt="git" src="https://github.com/user-attachments/assets/01caeabb-9116-48aa-9065-275c274fe832" />


Move to the **single-node** directory
```bash
cd wazuh-docker/single-node
```
We can also move to the **multi-node** directory
```bash
cd wazuh-docker/multi-node
```
We must provide certificates for each node to secure communication between them in the Wazuh stack.For certificate generations,
```bash
sudo docker-compose -f generate-indexer-certs.yml run --rm generator
```
<img width="816" height="403" alt="docker" src="https://github.com/user-attachments/assets/c565b3ec-780e-4b8c-943d-32f9b03445f9" />

We will start the wazuh in background using command,
```bash
sudo docker-compose up -d
```
<img width="800" height="333" alt="up -d" src="https://github.com/user-attachments/assets/4286c298-3f6e-4360-9125-e975c3382174" />
