Assignment Documentation:

Name: Muhammad Usman

Roll no: 20i-0416

Section: DS-N


Setup:

Install Apache Airflow:

Install the Python package manager, and virtual environment.

$ sudo apt-get install -y python3-pip python3-venv

Create a new directory.

 $ mkdir airflow-project

switch to the directory.

 $ cd airflow-project

Create a new virtual environment.

 $ python3 -m venv airflow-env

Activate the virtual environment.

 $ source airflow-env/bin/activate


Using pip, install Airflow.

 $ pip install apache-airflow

Initialize a new SQLite database to create the Airflow meta-store that Airflow needs to run.

 $ airflow db init

Create the administrative user and password used to access Airflow.

 $ airflow users create --role Admin --username admin --email admin --firstname admin --lastname admin --password my-password

 $ nohup airflow scheduler > scheduler.log 2>&1 &

The Scheduler command starts the Airflow scheduler, queues, and runs the workflows defined in the DAG code.

Start the Airflow web server on port 8080.

$ nohup airflow webserver -p 8080 > webserver.log 2>&1 &




