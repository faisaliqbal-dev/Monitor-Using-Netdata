# 🖥️ Task 7: Monitor System Resources Using Netdata

## 📌 Objective
Set up **Netdata** using Docker on an EC2 instance to monitor system and application performance metrics in real-time.

---

## ⚙️ Tools Used
- [Netdata](https://www.netdata.cloud/) (Open-source monitoring tool)
- Docker
- stress (for CPU load testing)
- Amazon EC2 (Ubuntu)

---

## 🧠 What Was Done

### ✅ Step 1: Install Docker

sudo apt update -y
sudo apt install docker.io -y
sudo service docker start
sudo systemctl enable docker

✅ Step 2: Run Netdata Container

docker run -d --name=netdata -p 19999:19999 netdata/netdata

✅ Step 3: Access Netdata Dashboard

http://44.203.72.220:19999

Netdata shows real-time stats for:

CPU

Memory

Disk I/O

Network

Docker containers

📊 Charts and Alerts Panel
Charts: CPU, memory, disk, and more

Alerts: Built-in health checks with visual indicators (green/yellow/red)

🧪 Step 4: Stress Test the CPU

apt install stress -y
stress --cpu 4 --timeout 120

This created 4 CPU-intensive processes for 120 seconds, and the spike was clearly visible on Netdata’s dashboard.

🎯 Outcome
Successfully deployed a lightweight monitoring tool on a cloud server and generated CPU load to test real-time performance and alert visualization.



