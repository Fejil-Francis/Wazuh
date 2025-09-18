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
Install docker-compose,if not installed
```bash
sudo apt install docker-compose
```
<img width="816" height="403" alt="docker" src="https://github.com/user-attachments/assets/c565b3ec-780e-4b8c-943d-32f9b03445f9" />

We will start the wazuh in background using command,
```bash
sudo docker-compose up -d
```
<img width="808" height="486" alt="upp" src="https://github.com/user-attachments/assets/c6936b70-a96c-4c4d-bdaa-9b75f94674b6" />

<img width="800" height="333" alt="up -d" src="https://github.com/user-attachments/assets/4286c298-3f6e-4360-9125-e975c3382174" />

We can also start wazuh as foreground
```bash
sudo docker-compose up 
```
For stopping we can use,

```bash
sudo docker-compose down 
```
When we use foreground,if terminal is closed the wazuh will automatically closed so its better to use background.If there arise such cases where background doesnt works use foreground


## The wazuh is now ready.
Now open the browser and move to the following web address
```bash
https://<ip address>
```
Sometime a warning will come
<img width="1059" height="429" alt="advance" src="https://github.com/user-attachments/assets/01b3cbf4-88f8-4fcd-b178-153c061bd5ca" />

Click on advanced and click accept the risk
 and continue
 <img width="977" height="533" alt="accept" src="https://github.com/user-attachments/assets/9254ae70-4a2d-4b1c-9737-b2699790103a" />

The wazuh login page will open like following
<img width="773" height="493" alt="login" src="https://github.com/user-attachments/assets/29cdea51-317e-42fe-a3ba-a274aab78d76" />

The username and password are
```bash
username:admin
password:SecretPassword
```

The wazuh page will take some time to load after login.

The page similar to the following will arise
<img width="1268" height="521" alt="wazu" src="https://github.com/user-attachments/assets/2117fe3f-e8e7-4483-9f7e-afca65e420ea" />

Now the wazuh is implemented now and can check statuse of machine through wazuh.By deploying new agent new machine can be added. 


