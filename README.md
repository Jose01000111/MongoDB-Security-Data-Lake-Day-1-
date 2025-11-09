# 💾 MongoDB Data Federation-setup  ➡️ 📈 Splunk Integration  ➡️ Threat Modeling 🔐 

## In this lab, I set up a **MongoDB Atlas Data Federation environment** to simulate a SOC workflow. My goal was to create a foundation where I could collect, store, and analyze security log data from multiple sources. Later, I plan to pull logs from **Splunk** or other sources, enrich them, and explore the data using **Compass, Charts, and advanced queries** like vector search and NLP for threat detection.

<img width="649" height="547" alt="Yd25KtT" src="https://github.com/user-attachments/assets/1906a4ef-7e1f-4864-9b0d-e65f34ebe037" />

---

## Technologies I Used

- **MongoDB Atlas** — to host the SOC data and Data Federation  
- **MongoDB Compass** — to explore, query, and validate collections  
- **Python 3 + pymongo** — for automating log ingestion, enrichment, and queries  
- **MongoDB Charts** — for visualizing trends and SOC metrics  
- **Atlas Data Federation** — to unify data across clusters and external sources  
- **Vector search / NLP queries** — for advanced queries for threat detection

---

## Setting Up My Environment

**Goal:** I wanted to prepare MongoDB Atlas for SOC use, verify connectivity, and lay the groundwork for pulling data from Splunk later.

### MongoDB Atlas Cluster

- I created a free-tier cluster.  
- Added my IP to the **network access whitelist**.  
- Created a **database user** with read/write permissions.  
- Saved my **connection string** for Compass and Python.

<img width="1377" height="295" alt="Sx5yn9Y" src="https://github.com/user-attachments/assets/adf99a73-34bb-497f-8e21-7390224491f5" />

## Network & User Setup

For my MongoDB Atlas cluster, I configured the **IP Access List** to allow connections only from my current IP address.  

<img width="529" height="222" alt="ESwDJOI" src="https://github.com/user-attachments/assets/98bfecd6-8dae-4dfe-9852-f9854c03948e" />

- **Allowed IP Address:** 108.195.24.228/32 (this includes my current IP).  
- This ensures secure access to the cluster by restricting it to known addresses.  
- I also created a **database user** with read/write permissions to manage the collections and enable Python and Compass connections.


<img width="529" height="222" alt="C7BNrTV" src="https://github.com/user-attachments/assets/fb6f8413-cd1e-467e-9e97-2a8fb51ea85b" />

This setup forms the foundation for securely accessing and managing the cluster from my local environment and scripts.


---

### MongoDB Compass

- I downloaded Compass and connected to my Atlas cluster.  
- Verified that I could see collections and explore the database.

<img width="660" height="336" alt="goKPy6F" src="https://github.com/user-attachments/assets/ab76e23d-777d-4bbd-add0-9378214ce17e" />


**Compass Connected:**  

![Compass Connected](https://github.com/user-attachments/assets/9950127d-756d-4cf4-8458-bf4dca6ddf51)

---

### Python Setup

- Installed Python 3 and the `pymongo` package.  
- Verified connection to Atlas with this test script:
## Python Connection Test

**Python Connection Screenshot:**  
![Python Connection](https://github.com/user-attachments/assets/17f00bb5-8c11-458d-803d-c03a9fe0f23e)

---

## 🚀 Next Steps

After setting up the MongoDB Data Federation lab and verifying connectivity with Compass and Python, here’s what I plan to do next:

1. **Ingest Logs from Splunk**
   - Connect to Splunk or other log sources via Python or Atlas connectors.
   - Pull SOC-relevant logs such as Windows Sysmon events, firewall logs, and IDS alerts.
   - Normalize and store them in MongoDB collections.

2. **Data Enrichment**
   - Add metadata such as timestamps, source IP, geolocation, and threat intelligence tags.
   - Prepare the data for advanced queries and analytics.

3. **Advanced Querying**
   - Explore **Vector Search** and **NLP queries** to detect anomalous or suspicious patterns.
   - Experiment with aggregation pipelines to summarize activity.

4. **Visualization and Dashboards**
   - Use **MongoDB Charts** to create dashboards for SOC metrics.
   - Identify trends, spikes, and potential incidents visually.

5. **Threat Modeling & Analysis**
   - Simulate attack scenarios using the enriched dataset.
   - Evaluate alerting strategies and log correlation for SOC exercises.

6. **Automation & Scaling**
   - Automate ingestion and enrichment using Python scripts.
   - Consider adding multiple clusters or external sources for Data Federation testing.

7. **Documentation & Sharing**
   - Keep clear documentation of architecture, queries, and dashboards.
   - Share insights and lessons learned for future SOC labs or portfolio projects.



