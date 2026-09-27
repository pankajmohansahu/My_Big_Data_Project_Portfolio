<div align="center">

# 📊 Big Data & Data Engineering Portfolio

### *Data that doesn't move at scale is just a very large file.*

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache_Spark-PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-Streaming-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-Dataproc-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Pub/Sub](https://img.shields.io/badge/Pub%2FSub-Event_Driven-669DF6?style=for-the-badge&logo=googlecloud&logoColor=white)
![Cloud Functions](https://img.shields.io/badge/Cloud_Functions-Serverless-FBBC04?style=for-the-badge&logo=googlecloud&logoColor=black)

</div>

---

## 👋 About This Portfolio

I'm a data science student at **IIT Madras (BSc, Data Science & Applications)** who likes building systems that keep working after the data stops fitting in memory.

This portfolio collects my hands-on work in distributed data processing: batch jobs on a single VM, then Spark clusters on Dataproc, event-driven serverless triggers, real-time Kafka streams, and finally distributed ML inference. Each project answers a practical question: *how does this pipeline behave when the data gets bigger, arrives faster, or shows up without warning?*

> **Philosophy:** *If it only runs on a laptop with a sample CSV, it isn't a data pipeline yet.*

---

## 🗺️ Data Engineering Stack I Work With

```
  Sources  ──►  GCS / Kafka / Pub/Sub  (ingestion)
                          │
            Cloud Functions  (event-driven triggers)
                          │
           Spark on GCP Dataproc  (RDD · DataFrame · SparkSQL)
                          │
         Spark Structured Streaming  (windowed real-time aggregation)
                          │
          MLlib / Pandas UDF + PyTorch  (distributed ML)
                          │
            GCS / Cloud Logging  (storage & observability)
```

---

## 🚀 Core Projects

> 🟢 Complete &nbsp;|&nbsp; 🟡 In Progress &nbsp;|&nbsp; 🔵 Planned &nbsp;|&nbsp; ⭐ Featured

| Status | Project | What Problem It Solves | Stack |
|:---:|---|---|---|
| 🟢 ⭐ | [**Spark DL Image Classification**](https://github.com/pankajmohansahu/spark-dl-image-classification-iitm) | Scales deep-learning inference across a Spark cluster: a pretrained MobileNetV2 is broadcast to workers and applied via Pandas UDFs, so images are classified in parallel instead of one at a time on one machine. | PySpark · Pandas UDF · MobileNetV2 · PyTorch/TensorFlow · GCP Dataproc |
| 🟢 ⭐ | [**MNIST PySpark GCP Dataproc Pipeline**](https://github.com/pankajmohansahu/mnist-pyspark-gcp-dataproc-pipeline) | End-to-end ML on big data: trains a Decision Tree with CrossValidator in Spark MLlib on Dataproc, then runs inference automatically whenever a new file lands in GCS, triggered by a Gen2 Cloud Function. | PySpark MLlib · GCP Dataproc · Cloud Functions Gen2 · GCS |
| 🟢 ⭐ | [**Kafka + Spark Structured Streaming**](https://github.com/pankajmohansahu/iitm-bigdata-week8-kafka-spark-streaming) | Real-time pipeline with dual Kafka producers (GCE VM + Cloud Functions) feeding Spark Structured Streaming on Dataproc, with sliding-window aggregations that update continuously as events arrive. | Apache Kafka · Spark Structured Streaming · GCP Dataproc · Compute Engine |
| 🟢 | [**GCP Pub/Sub Event-Driven Pipeline**](https://github.com/pankajmohansahu/gcp-pubsub-event-driven-pipeline-iitm) | Decouples producers from consumers: Cloud Storage upload events fan out through Pub/Sub to Cloud Functions (Gen1 & Gen2) and a Compute Engine subscriber, so processing reacts to data with no polling. | Pub/Sub · Cloud Functions Gen1/Gen2 · Cloud Storage · Compute Engine |
| 🟢 | [**SparkSQL Analytics & SCD Type I/II**](https://github.com/pankajmohansahu/iitm-bsds-bigdata-week6-sparksql-scd) | Warehouse-style dimension handling at scale: runs aggregation analytics and implements Slowly Changing Dimensions (Type I overwrite and Type II history-tracking) on customer tables with Spark SQL. | Spark SQL · PySpark · GCP Dataproc |

---

## 🧪 Practice & Exploration

| Project | Focus |
|---|---|
| [PySpark Data Cleaning on Dataproc — Week 5](https://github.com/pankajmohansahu/iitm-bsds-intro-big-data-week5-pyspark-dataproc) | First cluster job: data cleaning and aggregation with PySpark submitted to Google Cloud Dataproc. |
| [PySpark ClickCount — RDD vs DataFrame](https://github.com/pankajmohansahu/PySpark-ClickCount-RDD-DataFrame) | The same click-count analysis written with both the RDD and DataFrame APIs, to compare the low-level and optimized abstractions directly. |
| [Longest Line — GCS-Triggered Cloud Function — Week 3](https://github.com/pankajmohansahu/iitm-ibd-w3-longest-line-gcs-function) | First serverless trigger: a Gen1 Cloud Function (Python 3.11) that analyses uploaded text files, logs to Cloud Logging, and writes results back to the bucket. |
| [Longest Line in GCS — Week 2](https://github.com/pankajmohansahu/iitm-ibd-week2-longest-line-gcs) | Where it started: a Python script reading a GCS-hosted file from Cloud Shell with `gsutil`, before any distributed tooling. |

---

## 🧰 Tech Stack

<div align="center">

| Layer | Tools |
|:---:|:---:|
| **Distributed Processing** | Apache Spark · PySpark · RDD · DataFrames |
| **Querying & Modelling** | Spark SQL · SCD Type I / II |
| **Streaming** | Apache Kafka · Spark Structured Streaming |
| **Event-Driven / Serverless** | Google Pub/Sub · Cloud Functions (Gen1 & Gen2) |
| **Compute** | GCP Dataproc · Compute Engine |
| **Storage & Observability** | Google Cloud Storage · Cloud Logging |
| **ML on Big Data** | Spark MLlib · Pandas UDF · PyTorch · MobileNetV2 |
| **Language** | Python 3.10+ |

</div>

---

## 🗂️ My Other Portfolios

| Portfolio | Focus |
|---|---|
| [⚙️ MLOps Project Portfolio](https://github.com/pankajmohansahu/My_MLOps_Project_Portfolio) | End-to-end ML pipelines using MLflow, DVC, Docker, Kubernetes, and GCP |
| [🧠 ML & Deep Learning Portfolio](https://github.com/pankajmohansahu/My-ML-Deep-Learning-Project-Portfolio) | NLP, Speech, LLM fine-tuning and Agentic AI with PyTorch, HuggingFace, Gemma and LangGraph |
| [👁️ Computer Vision Portfolio](https://github.com/pankajmohansahu/My_Computer_Vision_Portfolio) | Image classification, object detection, and restoration with PyTorch and EfficientNet |
| [🌐 Full Stack App Development Portfolio](https://github.com/pankajmohansahu/My_Full_Stack_Application_Development_Portfolio) | Web apps using Flask, SQLite, Vue.js and REST APIs |

---

## 📬 Let's Connect

I'm always open to discussing data engineering, project feedback, or collaboration opportunities.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pankaj-mohan-sahu-3b8662205/)
[![Email](https://img.shields.io/badge/Email-Reach_Out-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sahumpankaj1994@gmail.com)

</div>

---

<div align="center">
<sub>⭐ If any of these projects helped you, a star goes a long way!</sub>
</div>
