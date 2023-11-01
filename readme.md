# Leveraging Clear Scape Analytics Experience in Data CI/CD Pipelines

Continuous Integration (CI) and Continuous Delivery (CD) are both crucial components of modern software development practices, aimed at automating and improving the development lifecycle.

The goal of Continuous Integration (CI) is to integrate the work of different developers frequently, ensuring that the software is always in a releasable state. CI includes processes such as automated builds, automated testing, repository management, version control, etc.

The goal of Continuous Delivery (CD) is to ensure that software can be reliably deployed to production. CD includes processes such as automated deployment, configuration management, logs and monitoring, rollback procedures, etc.

Both CI and CD processes might need access to data to either run integration tests or build development and staging environments that more closely resemble the data context in production.

CI/CD practices can be implemented as part of the development of dbt pipelines, migration scripts, or apps.

ClearScape Analytics Experience offers a lightweight Teradata environment that can be used for learning purposes but also to build a data environment for your CI/CD processes.

This repository contains an illustration of using ClearScape Analytics Experience in this fashion.

## This Repository

The workflows subdirectory of the .github contains a sample workflow that:

- Starts a ClearScape Analytics Experience Environment
- Creates a Database
- Loads data into the database
- Makes a testing query
- Errors if the query returns an unexpected result
- Cleans the testing data
- Stops the ClearScape Analytics Experience Environment

## Prerequisites
- A ClearScape Analytics Experience Environment can be done at [Teradata.com/experience.](https://www.teradata.com/Getting-Started/Demos/ClearScape-Analytics?utm_source=github&utm_medium=referral&utm_campaign=gbl-devrel-internal&utm_content=demo)
- A github repository

## Running the Example
### Clone this repository to your local environment
### Set a remote repository in github and point your local copy to that remote
- Explanation on how to do this can be found [here.](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories)
### Set the following secrets on your github repository
- API_KEY (Your ClearScape Analytics Experience API Key)
- ENV_NAME (Your Environment Name)
- ENV_HOST (Your Environment Host URL)
- ENV_AUTH (The base64 encoding of the following string "demo_user:<your environment password>")
![Example of setting the environment secrets](/etc/ENV_Setting.PNG)

### Push code to main

- The action will start to execute.
    - Will start the ClearScape Analtyics Environment
    - Will create a database
    - Will create a table
    - Will load data to a table
    - Will make a query to the table
    - Will validate the result of the query
    - Will clean the data
    - Will stop the environment
- After the action completes successfully you'll see the following results. 
![Example of successful run](/etc/Completed.PNG)