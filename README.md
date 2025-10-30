# 🧠 MongoDB SOC Data Lake — 5-Phase Lab with Wazuh

## 🎯 Lab Overview

For this lab, I built a mini SOC data lake using **MongoDB Atlas** to simulate how security analysts collect, store, correlate, and visualize log data. The goal was to create a functional system capable of ingesting and enriching logs from multiple sources, including Windows Sysmon, firewall logs, threat intelligence feeds, and Wazuh alerts.

<img width="649" height="547" alt="LB1FSFf" src="https://github.com/user-attachments/assets/efee6dbe-531d-4c92-b741-5a687414faff" />

## 🛠️ Technologies Used

- **MongoDB Atlas** — Cloud database platform used to host the SOC data lake and store log collections.
- **MongoDB Compass** — GUI tool for exploring, querying, and verifying database contents.
- **Python 3 + pymongo** — Scripting environment for automating log ingestion, enrichment, and queries.
- **Wazuh Manager & Agent** — Security monitoring platform used to collect host and network logs in real time.
- **MongoDB Charts** — Visualization tool to create dashboards and present SOC metrics and trends.

---

## ⚙️ Phase 1 — Environment Setup & Planning

**Goal:** Prepare my MongoDB Atlas environment, install Compass, Python, and plan the SOC data flow.

**What I Did:**  
I signed up for MongoDB Atlas and created a free-tier cluster, added my IP to the network whitelist, and created a database user with read/write access. I installed MongoDB Compass for GUI access and Python 3 with the pymongo package. I also installed the Wazuh manager on my local machine to collect security events and set up a Wazuh agent to simulate log collection from a host. I decided on my log sources including Sysmon logs, firewall logs, threat intelligence feeds, and Wazuh alerts. Finally, I sketched the architecture of the data lake showing the flow from raw logs to parsing, normalization, MongoDB collections, queries, and dashboards.

**Deliverables / Documentation:**  

🟢 Cluster overview

   <img width="1377" height="295" alt="yZHVD65" src="https://github.com/user-attachments/assets/7fd04342-6aff-4b2c-b3e7-1b4c480017b5" />

🟢 Network & user setup

 <img width="529" height="222" alt="ESwDJOI" src="https://github.com/user-attachments/assets/98bfecd6-8dae-4dfe-9852-f9854c03948e" />
   
🟢 Compass connected

   <img width="660" height="336" alt="rQohfES" src="https://github.com/user-attachments/assets/9950127d-756d-4cf4-8458-bf4dca6ddf51" />

🟢 Python connection

<img width="358" height="199" alt="8EeKZTC" src="https://github.com/user-attachments/assets/17f00bb5-8c11-458d-803d-c03a9fe0f23e" />

---

## 📥 Phase 2 — Collect & Prepare Sample Data

**Goal:** Gather sample logs, including Wazuh alerts, and normalize them for MongoDB ingestion.

**What I Did:**  
I downloaded sample datasets including Sysmon logs, firewall logs in CSV or JSON format, and threat intelligence feeds. I collected Wazuh alerts from my Wazuh agent. I standardized the key fields across all logs including IP addresses, timestamps, and action codes. I converted CSV and text files to JSON for MongoDB ingestion and organized all files into structured folders for each log source.

**Deliverables / Documentation:**  
- Folder structure screenshot showing all logs  
- Example JSON file of normalized data  
- Screenshot of Wazuh alerts exported or visible in the dashboard

---

## 🗄️ Phase 3 — Create Collections & Ingest Data

**Goal:** Create collections in MongoDB Atlas and load all sample logs including Wazuh alerts.

**What I Did:**  
I connected to MongoDB Atlas using Compass and mongosh, then created a database called `soc_data`. I created the collections for Sysmon logs, firewall logs, threat intelligence, and Wazuh alerts. I imported all JSON files into their respective collections and verified the imports by checking document counts and confirming field types for each collection.

**Deliverables / Documentation:**  
- Screenshot of Compass showing collections and document counts  
- Screenshot of Wazuh alerts visible in MongoDB after ingestion

---

## 🔍 Phase 4 — Explore, Correlate & Enrich Data

**Goal:** Query logs, identify patterns, correlate data, and enrich with threat intelligence context.

**What I Did:**  
I queried Sysmon logs to find failed logins, suspicious processes, and file modifications. I analyzed firewall logs to find blocked traffic, unusual ports, and repeated source IPs. I also reviewed Wazuh alerts for critical events and malware detections. I cross-referenced firewall IPs and Sysmon activity with threat intelligence using aggregation pipelines and tagged matching events with enrichment fields like malicious, suspicious, and benign. I used Compass filters to visually explore correlations and identify anomalies across all log sources.

**Deliverables / Documentation:**  
- Screenshot of enriched data in Compass  
- Screenshot of correlation query results including Wazuh alerts

---

## 📊 Phase 5 — Visualization, Automation & Reflection

**Goal:** Visualize insights, automate log ingestion, and reflect on SOC workflow.

**What I Did:**  
I created dashboards using MongoDB Charts and Python visualization libraries to highlight top blocked IPs, most frequent event types, and alerts correlated with threat intelligence and Wazuh events. I wrote a Python script to automatically ingest new logs into MongoDB collections and configured MongoDB Change Streams to detect and alert on new malicious entries. I reflected on the workflow, noting lessons learned and potential improvements for scaling this into a production-style SOC setup.

**Deliverables / Documentation:**  
- Screenshot of dashboards summarizing SOC metrics  
- Screenshot of Python automation script processing logs  
- Screenshot of MongoDB Change Streams detecting new malicious events  
- Summary notes on lessons learned and improvements

---

## ✅ Lab Completed — Key Learnings

- I learned how to set up a **MongoDB Atlas cluster** and connect it with MongoDB Compass for GUI exploration.  
- I learned how to install and configure **Wazuh manager and agent** to collect security events and integrate them into a SOC data lake.  
- I learned to **normalize and convert multiple log formats** (Sysmon, firewall, threat intelligence, Wazuh) into JSON for MongoDB ingestion.  
- I learned to **create collections, ingest data, and verify document structure** in MongoDB Atlas.  
- I practiced **querying, correlating, and enriching data** using MongoDB aggregation pipelines and Compass visual filters.  
- I learned how to **visualize SOC data** using MongoDB Charts and Python visualization libraries.  
- I learned to **automate log ingestion and alerting** using Python scripts and MongoDB Change Streams.  
- I reflected on SOC workflows and identified potential improvements for a scalable, production-style SOC environment.  

