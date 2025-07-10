# 🚗 ETL Toll Data Pipeline with Apache Airflow

This project demonstrates a complete **ETL (Extract, Transform, Load)** pipeline using **Apache Airflow**, designed to process toll data from multiple source formats into a consolidated, transformed CSV file.

It showcases your ability to handle orchestration workflows, data extraction from multiple formats, transformation logic, and modular code structure — a valuable skillset for Data Engineering and ETL roles.

---

## ✨ Features

- ✅ Download dataset from a cloud source (`.tgz` archive)
- ✅ Extract from multiple file formats:
  - **CSV** (Comma Separated)
  - **TSV** (Tab Separated)
  - **Fixed-width text**
- ✅ Consolidate all data sources into a single table
- ✅ Transform vehicle type data to standardized format (uppercase)
- ✅ Automate task sequencing with Airflow DAG
- ✅ Clear and modular Python code using `PythonOperator`

---

## 🛠️ Prerequisites

Before running this project, make sure you have the following installed:

- **Python 3.7+**
- **pip** (Python package manager)
- **Apache Airflow 2.x**

### ✅ Install Airflow

You can install Airflow using the official method:

```
pip install apache-airflow==2.8.1
```
💡 For full setup, follow Airflow's official installation guide: https://airflow.apache.org/docs/apache-airflow/stable/installation/index.html

# ✅ Required directory  
Ensure this directory exists before running the DAG:  
/home/project/airflow/dags/python_etl/staging.  

Open a terminal and create a directory structure:  
```sudo mkdir -p /home/project/airflow/dags/python_etl/staging  ```

Execute the following commands to avoid any permission issues in writing to the directories:  
```sudo chmod -R 777 /home/project/airflow/dags/python_etl  ```

# 🚀 How to Run
1. Clone this repo:
```git clone https://github.com/hungnguyen820/etl-airflow-project.git```
```
cd etl-airflow-project
```
3. Install dependencies:
```pip install -r requirements.txt```

4. Initialize Airflow database:
```airflow db init```

5. Create Airflow user (first-time only):
airflow users create \  
  --username admin \  
  --firstname Firstname \  
  --lastname Lastname \  
  --role Admin \  
  --email hungnguyen29820@gmail.com
  
6. Start Airflow services:
airflow webserver --port 8080
In another terminal:
airflow scheduler

7. Place the DAG file:
Make sure etl_toll_data.ipynb is inside the dags/ folder or the folder specified in your AIRFLOW_HOME.

8. Access the Airflow UI:
Open http://localhost:8080 in your browser, activate the DAG named ETL_toll_data, and trigger it manually.

  
# 📁 Folder Structure
etl-airflow-project/    
├── dags/    
│   └── etl_toll_data.ipynb           # Main DAG definition 	

├── requirements.txt               # Python dependencies	 

├── README.md                      # Project documentation	 


  
# 📦 Python Dependencies (requirements.txt)
```
apache-airflow==2.8.1
requests
```


