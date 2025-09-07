#  End-to-End Big Data Pipeline:  NiFi, MongoDB, Spark, Delta Lake on Hadoop, Power BI  

##  Architecture 
<img width="2071" height="901" alt="last_arch drawio" src="https://github.com/user-attachments/assets/d8d1d3db-d39d-4e3e-a6a9-15e5c15974bd" />



---

##  Description   

This project demonstrates an end-to-end big data pipeline built on top of Docker containers, covering the full data lifecycle:  

| Layer          | Technology          | Purpose                                                                 |
|--------------------------|---------------------------|-------------------------------------------------------------------------|
| **Data Source**          | JSON file (movies data)   | Provides raw movie dataset                                              |
| **Ingestion Layer**      | Apache NiFi → MongoDB     | Ingests JSON data and stores it in MongoDB                              |
| **Processing Layer**     | Apache Spark              | Transforms and prepares data for storage                                |
| **Storage Layer**        | Delta Lake on Hadoop HDFS | Implements Medallion architecture:<br>• Bronze = raw<br>• Silver = cleaned<br>• Gold = aggregated |
| **Visualization Layer**  | Power BI                  | Builds interactive dashboard                 |

---

##  NiFi Flow    
  <img width="1095" height="899" alt="NIFI" src="https://github.com/user-attachments/assets/8368b0f9-bc26-4539-b3fc-b4e0fc599948" />


---

## Robo 3t ( mongodb client )
<img width="1893" height="925" alt="robo 3t mongodb client" src="https://github.com/user-attachments/assets/baf7881b-bc35-46bb-944a-e47264153588" />

---
##  Dashboard 
<img width="1423" height="797" alt="dashboard" src="https://github.com/user-attachments/assets/3fd78ce0-71d1-4c54-8705-5f789e90a3da" />

---
##  Access Ports

| Service                  | Port / URL                                       |
|---------------------------|--------------------------------------------------|
| **Hadoop NameNode**       | [http://localhost:9870](http://localhost:9870)   |
| **Hadoop ResourceManager**| [http://localhost:8088](http://localhost:8088)   |
| **Hadoop HistoryServer**  | [http://localhost:19888](http://localhost:19888) |
| **DataNodes**             | 9864, 9865, 9866                                |
| **NodeManagers**          | 8042, 8043, 8044                                |
| **Spark Master (UI)**     | [http://localhost:8080](http://localhost:8080)   |
| **Spark Workers**         | 8081, 8082, 8083                                |
| **Spark History Server**  | [http://localhost:18080](http://localhost:18080) |
| **Spark Master URL**      | `spark://172.28.1.2:7077`                        |

---

