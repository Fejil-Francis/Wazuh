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

## 📦 Installation (Docker)

Clone the Wazuh Docker repository:

```bash
git clone https://github.com/wazuh/wazuh-docker.git -b v4.12.0
```
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
