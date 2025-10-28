# 🧠 MongoDB SOC Data Lake — Day 1: Environment Setup & Architecture Planning
## ⚙️ My Goals
Prepare my lab environment for the SOC Data Lake.
Install and verify all necessary tools: MongoDB, Compass, mongosh, Python.
Plan the data flow and architecture of my SOC Data Lake before ingesting any logs.

## 💻 What I Did

### 🖥️ Installed MongoDB locally on Ubuntu and confirmed it was running.

### 📸 Screenshot: MongoDB service status — purpose: show database is operational

### 🪟 Installed MongoDB Compass to access the database via GUI.

### 📸 Screenshot: Compass connected to local database — purpose: verify GUI access

### 🧩 Installed mongosh CLI for command-line interaction.

### 📸 Screenshot: Mongosh shell open — purpose: confirm CLI connection works

### 🐍 Installed Python 3 and the pymongo library for future automation.

### 📸 Screenshot: Python version and pymongo installed — purpose: verify tools for scripting

### 🔍 Selected log sources I will simulate:

Windows Sysmon logs for system activity monitoring

Firewall logs to track allowed/denied traffic

Threat intelligence feeds for IP/domain reputation

### 🧠 Sketched out SOC Data Lake architecture:

Raw logs → Parsing/Normalization → MongoDB Collections → Queries & Dashboards

📸 Screenshot: Architecture sketch — purpose: document data flow plan

##💡 What I Learned

### 🏗️ Learned how to install and verify MongoDB and Python on Ubuntu.

### 🌐 Practiced using both Compass and mongosh for GUI and CLI database access.

### 🔄 Gained insight into SOC data flow and how logs are planned before ingestion.

### 🚀 Built a stable foundation for starting log ingestion and normalization in Day 2.


🏁 Summary

Today I set up my Ubuntu SOC lab, installed all necessary tools, selected log sources, and planned the architecture of my MongoDB SOC Data Lake. The screenshots provide proof of setup and planning, giving me a clear foundation to start log ingestion and normalization in Day 2.
