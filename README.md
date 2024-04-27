# MLOps_Exercise

This is Git Repo For Showcasing the integration of MLFlow and Airflow in ML Pipelines. 
Follow Below Steps to set up the infra:

**Step 1: Install Dependencies**
Make sure you have Python installed on your system. Then, install the required libraries:
Run on terminal: pip install apache-airflow pandas scikit-learn mlflow

**Step 2: Initialize Airflow Database**
Airflow uses a database to store metadata about the tasks, DAGs, and executions. Initialize the database by running:
Run on terminal: airflow db init

**Step 3: Start Airflow Scheduler and Webserver**
Start the Airflow scheduler and webserver:
Run on terminal: airflow scheduler

Open a new terminal and run:
Run on terminal: airflow webserver

**Step 4: Define the DAG**
Create a Python file (e.g., housing_prediction.py) and paste the provided code for the DAG into it.

**Step 5: Prepare Data**
Prepare your dataset for housing prediction and save it as housing.csv in the same directory as your Python file.

**Step 6: Run the Pipeline**
Now, you can run the DAG by turning it on in the Airflow UI or using the following command:
Run on terminal: airflow dags trigger housing_prediction_pipeline

**Step 7: Monitor the Pipeline**
You can monitor the execution of the pipeline in the Airflow UI by navigating to **http://localhost:8080** in your web browser.

**Step 8: View Experiments in MLflow**
You can view the experiments, hyperparameters, metrics, and registered models in MLflow's UI by navigating to **http://localhost:5000** in your web browser.

**Additional Notes:**
Make sure to adjust any file paths or configurations in the code according to your setup.
Ensure that your Python environment has all the necessary libraries installed.
You may need to configure Airflow's airflow.cfg file for advanced settings, such as changing the executor or specifying a different database backend.
By following these steps, you can successfully run the machine learning pipeline using MLflow and Apache Airflow and monitor the execution and experiment results using their respective UIs.
