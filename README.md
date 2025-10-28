# 🧠 MongoDB SOC Data Lake — 5-Phase Lab Project 

#### I want to build a functional SOC data lake in MongoDB on Ubuntu that simulates how security analysts collect, store, correlate, and enrich log data. The goal is to design a professional data model demonstrating SOC workflows, threat intelligence, and data enrichment. This is meant to impress MongoDB leadership with Python-driven ingestion, enrichment, and correlation in a self-contained Ubuntu environment.

#### Tools I’m Using:

#### 🟢 MongoDB Community Edition on Ubuntu

#### 🟢 MongoDB Compass

#### 🐍 Python 3 with pymongo

#### 📊 Sample security data from Wazuh, Sysmon, firewall logs, and threat intelligence feeds

#### 💻 Optional: VS Code or Jupyter Notebook

## Phase 1 — Environment Setup & Planning ⚙️

## What I Did:
I installed MongoDB Community Edition on Ubuntu using apt commands, set up MongoDB to run as a service, and verified the connection with mongosh. I installed MongoDB Compass for GUI exploration and Python with pymongo for automation. I decided on my log sources: Sysmon logs for system activity, firewall logs for traffic, and Wazuh alerts for IDS data.

## Why:
Setting up MongoDB locally ensures I understand installation, configuration, and connectivity on Ubuntu — critical for real-world deployments. Planning my architecture ensures that my data model will handle multiple security sources efficiently.

### 📸 Deliverables :

#### 🍃Terminal showing MongoDB installed and running (sudo systemctl status mongod)

#### 🍃Compass connected to local MongoDB instance

#### 🍃Python pymongo setup confirmation

## Phase 2 — Collect & Prepare Security Data 📥

## What I Did:
I downloaded sample datasets: Sysmon logs, firewall logs, Wazuh IDS alerts, and threat intel feeds. I cleaned and normalized the data (standardizing IP addresses, timestamps, and actions) and converted any CSV or text files into JSON. I organized the files into /data/sysmon/, /data/firewall/, /data/wazuh/, and /data/threat_intel/.

## Why:
Clean, standardized data is essential for proper ingestion and analysis. Normalization ensures queries and correlation pipelines work without errors, just like in a production SOC.

### 📸 Deliverables :

#### 🍃Folder structure on Ubuntu showing organized JSON files

#### 🍃Sample JSON file open in VS Code or Jupyter Notebook

#### 🍃Example of cleaned and normalized log data

## Phase 3 — Design MongoDB Data Model & Ingest Logs 🗄️

## What I Did:
I created a database soc_data with collections: sysmon_logs, firewall_logs, wazuh_alerts, and threat_intel. Using Python and pymongo, I wrote scripts to insert JSON logs into MongoDB. I verified that timestamps, IPs, and event types were correctly interpreted.

## Why:
I focused on data modeling, making sure each collection supports SOC-style queries and enrichment. This is key for demonstrating that I can structure data intelligently for analysis.

### 📸 Deliverables :

#### 🍃Compass view of soc_data collections with documents

#### 🍃Python script inserting JSON data into MongoDB

#### 🍃Sample document showing correct fields and data types

## Phase 4 — Query, Correlate & Enrich 🔍

## What I Did:
I wrote queries to find suspicious activity: failed logins, blocked IPs, and repeated alerts. Using $lookup, I correlated firewall IPs with threat intel feeds and enriched alerts with tags like malicious, suspicious, or benign. I also linked Wazuh alerts with Sysmon events for deeper analysis.

## Why:
This phase simulates real SOC analysis, showing that my MongoDB model is ready for analytics and threat detection, not just storage.

### 📸 Deliverables :

#### 🍃Example MongoDB queries in mongosh

#### 🍃Compass showing correlated and enriched data

#### 🍃Sample enriched documents with added fields

## Phase 5 — Visualization & GitHub Documentation 📊

## What I Did:
I created visualizations using MongoDB Charts and Python (matplotlib/pandas) showing trends: top blocked IPs, frequent alert types, and correlated threats. I wrote a GitHub README explaining architecture, goals, and instructions to reproduce the data model.

## Why:
This phase demonstrates end-to-end capability: ingestion, enrichment, and actionable insights. Documenting everything professionally shows technical skill and communication — exactly what impresses executives.

### 📸 Deliverables :

#### 🍃MongoDB Charts dashboard of alerts or IPs

#### 🍃Python-generated plots showing trends

#### 🍃README snippet with project structure and workflow


🏁 Summary

Today I set up my Ubuntu SOC lab, installed all necessary tools, selected log sources, and planned the architecture of my MongoDB SOC Data Lake. The screenshots provide proof of setup and planning, giving me a clear foundation to start log ingestion and normalization in Day 2.
