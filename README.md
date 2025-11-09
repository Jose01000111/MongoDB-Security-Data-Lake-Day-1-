# 🧠 My MongoDB Data Federation Lab for Splunk Integration & Threat Modeling

## Overview

In this lab, I set up a **MongoDB Atlas Data Federation environment** to simulate a SOC workflow. My goal was to create a foundation where I could collect, store, and analyze security log data from multiple sources. Later, I plan to pull logs from **Splunk** or other sources, enrich them, and explore the data using **Compass, Charts, and advanced queries** like vector search and NLP for threat detection.

---

## Technologies I Used

- **MongoDB Atlas** — to host the SOC data and Data Federation  
- **MongoDB Compass** — to explore, query, and validate collections  
- **Python 3 + pymongo** — for automating log ingestion, enrichment, and queries  
- **MongoDB Charts** — for visualizing trends and SOC metrics  
- **Atlas Data Federation** — to unify data across clusters and external sources  
- **Vector search / NLP queries** — optional advanced queries for threat detection

---

## Setting Up My Environment

**Goal:** I wanted to prepare MongoDB Atlas for SOC use, verify connectivity, and lay the groundwork for pulling data from Splunk later.

### MongoDB Atlas Cluster

- I created a free-tier cluster.  
- Added my IP to the **network access whitelist**.  
- Created a **database user** with read/write permissions.  
- Saved my **connection string** for Compass and Python.

**Cluster Overview:**  

![Cluster Overview](https://github.com/user-attachments/assets/7fd04342-6aff-4b2c-b741-5a687414017b5)

## Network & User Setup

For my MongoDB Atlas cluster, I configured the **IP Access List** to allow connections only from my current IP address.  

<img width="529" height="222" alt="ESwDJOI" src="https://github.com/user-attachments/assets/98bfecd6-8dae-4dfe-9852-f9854c03948e" />

- **Allowed IP Address:** 108.195.24.228/32 (this includes my current IP).  
- This ensures secure access to the cluster by restricting it to known addresses.  
- I also created a **database user** with read/write permissions to manage the collections and enable Python and Compass connections.

This setup forms the foundation for securely accessing and managing the cluster from my local environment and scripts.


---

### MongoDB Compass

- I downloaded Compass and connected to my Atlas cluster.  
- Verified that I could see collections and explore the database.

**Compass Connected:**  

![Compass Connected](https://github.com/user-attachments/assets/9950127d-756d-4cf4-8458-bf4dca6ddf51)

---

### Python Setup

- Installed Python 3 and the `pymongo` package.  
- Verified connection to Atlas with this test script:
## Python Connection Test

**Python Connection Screenshot:**  
![Python Connection](https://github.com/user-attachments/assets/17f00bb5-8c11-458d-803d-c03a9fe0f23e)


```python
from pymongo import MongoClient

client = MongoClient("YOUR_ATLAS_CONNECTION_STRING")
db = client.test_database
print(db.list_collection_names())

