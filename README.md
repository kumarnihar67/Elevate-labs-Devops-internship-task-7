# 🚀 Task 7: Monitor System Resources Using Netdata

## 🎯 Objective
Install Netdata and visualize system and application performance metrics using Docker.

## 🛠️ Tools Used
- **Netdata** – Free, open-source monitoring tool 🖥️  
- **Docker** – To run Netdata as a container 🐳  
- **Windows PowerShell** – To execute Docker commands 💻  

## 📝 Steps Performed

1️⃣ Install & Verify Docker
- Installed Docker Desktop for Windows ✅  
- Verified installation:
  
2️⃣ Run Netdata Container
Ran Netdata in Docker:

powershell:
docker run -d --name=netdata -p 19999:19999 netdata/netdata

🌐 Maps dashboard to localhost
Verified the container is running:
docker ps

<img width="1920" height="1080" alt="1 Netdata-runing" src="https://github.com/user-attachments/assets/25429dac-5537-4587-a85e-b3c765111d73" />


3️⃣ Access Dashboard
Opened browser at: http://localhost:19999 🌟

<img width="1920" height="1080" alt="2 Netdata-dashboard" src="https://github.com/user-attachments/assets/49c51f26-48c7-4e8d-987b-3b6498a41848" />


Monitored live charts for:

CPU usage ⚡

<img width="1920" height="1049" alt="3 cpu-monitoring" src="https://github.com/user-attachments/assets/2ea90365-25bc-4bac-8bcd-b33ef09ff8cd" />


Memory usage 🧠

<img width="1920" height="1043" alt="4 Memory" src="https://github.com/user-attachments/assets/1d814d37-e9c3-4aa1-9f8a-f2e49f98342f" />


Disk I/O 💾

<img width="1920" height="1046" alt="5 Disk" src="https://github.com/user-attachments/assets/48cbafc3-ec5f-4f43-8c7e-a3ec6c5d0c3d" />


Docker containers 🐳 (Windows not show all containers)

<img width="1920" height="1080" alt="7 Docker-image" src="https://github.com/user-attachments/assets/995db42b-0326-4538-9d49-3100d36ef031" />


4️⃣ Explore Charts and Alerts
Charts panel shows real-time metrics 📊

Alert panel indicates high usage or abnormal behavior ⚠️

<img width="1920" height="1050" alt="6 Alerts" src="https://github.com/user-attachments/assets/285b646c-59b0-4474-9df0-e987a232f55e" />


Screenshots captured for CPU, memory, and disk charts with active alerts 📸


5️⃣ Access Logs 
Logs are stored inside the container at /var/log/netdata.
To view logs:
powershell
docker exec -it netdata bash
cd /var/log/netdata
ls
cat error.log
Logs show system metrics, errors, and alert events 📝

<img width="1920" height="1080" alt="1 Netdata-runing" src="https://github.com/user-attachments/assets/9073d91c-00eb-4b61-a17f-fcb2e06ce4f6" />


6️⃣ Stop and Remove Container
powershell
docker stop netdata
docker rm netdata
Cleans up resources 🧹


💡Observations
On Windows, some Docker container metrics may not appear due to platform limitations ⚠️

Netdata provides real-time monitoring without requiring login or configuration ⏱️

Dashboard is interactive and updates metrics live 🔄
