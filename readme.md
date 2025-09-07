

# GCP-AirFlow-Project

This repository hosts a sample project integrating Apache Airflow with Google Cloud Platform (GCP) for orchestrating data workflows. It includes Python-based DAGs designed for tasks like data extraction, transformation, and loading (ETL) using GCP services such as BigQuery, Cloud Storage, and Composer.

## Features

- Custom Airflow DAGs for GCP-specific operations.
- Integration with GCP tools for scalable data processing.
- Example scripts for deployment and configuration.


## Prerequisites

- Python 3.8 or higher.
- Apache Airflow installed (version 2.0+).
- GCP account with access to Composer, BigQuery, and Cloud Storage.
- Google Cloud SDK (gcloud) configured.


## Installation

1. Clone the repository:

```
git clone https://github.com/Premkumar2005/GCP-AirFlow-project.git
cd GCP-AirFlow-project
```

2. Set up a virtual environment:

```
python -m venv venv
source venv/bin/activate
```

3. Install dependencies:

```
pip install -r requirements.txt
```

4. Configure Airflow with GCP connections (update `airflow.cfg` or use the UI).

## Usage

1. Initialize Airflow database:

```
airflow db init
```

2. Start the Airflow webserver and scheduler:

```
airflow webserver --port 8080
airflow scheduler
```

3. Deploy to GCP Composer:
    - Create a Composer environment in GCP.
    - Upload DAGs to the environment's Cloud Storage bucket.
    - Trigger DAGs via the Composer UI.

Example DAG: The `gcp_etl_dag.py` demonstrates loading data from Cloud Storage to BigQuery.
