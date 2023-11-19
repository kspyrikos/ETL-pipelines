# ETL pipelines
ETL pipelines using best practices in Python and Data Engineering.

## Dataset
This repository is using data from the German marketplace organizer for trading shares, Deutsche Boerse.

There are two datasets available, but the `xetra` dataset is being used for the implementation of the ETL pipelines. 

Xetra stands for exchange electronic trading and is the trading platform of the Deutsche Boerse Group.

The xetra dataset is saved in a `aws s3 bucket` and available to the public for free: [ Deutsche Börse Public Dataset](https://registry.opendata.aws/deutsche-boerse-pds/)


## Task
This repository produced a report of the ISINs on a daily basis. The report provides insights regarding `opening` and `closing` price, `minimum` and `maximum` price, the `daily_traded_volume`, and the change of the current day's closing price compared to the previous day's closing price. 

The task is to create a production ready python data job that is extracting the  `xetra` dataset from a `source aws s3 bucket`, since the last run of the job, and saves the report to a `target aws s3 bucket`.
The format of the target file should be `parquet`.

Both `functional` and `OOP` approaches are explored.


## Steps
1. Set up virtual environment for a Python environment.
2. Set up a AWS user account.
3. Juputer notebook for functional approach.
4. OOP design principles and further requirements - Configuration, Logging, Meta Data.
5. OOP code desing.
6. Implement Logging.
7. Set up dependency management with pipenv.
8. Performance tuning with profiling and timing.
9. Create Dockerfile and push docker image to Docker Hub.
10. Run application in production using a Minikube and Argo Workflows.

## Requirements
A `pipenv` virtual environment was used for this project.

Use `pip install -r requirements.txt` in order to install the required depedencies. 
