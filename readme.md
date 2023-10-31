# Leveraging Clear Scape Analytics Experience in Data CI/CD Pipelines

Applying Continuos Integration and Development principles to data specific tasks is a very relevant topic.

Whether executing integration testing, changes of a dbt project, or even migration scripts, it is valuable to check those changes againts a test database.

Clear Scape Analytics Experience offer this kind of lightweight support for Teradata Users.

In the workflows subdirectory of the .github contains a sample workflow that:

- Starts a ClearScape Analytics Experience Environment
- Creates a Database
- Loads data into the database
- Makes a testing query
- Errors if the query returns an unexpected result
- Cleans the testing data
- Stops the ClearScape Analytics Experience Environment

## Prerequisites
- A ClearScape Analytics Experience Environment
- A github repository

## Process
### Clone this repository to your local environment
### Set a remote repository in github and point your local copy to that remote
### Set the following secrets on your github repository
- API_KEY (Your ClearScape Analytics Experience API Key)
- ENV_NAME (Your Environment Name)
- ENV_HOST (Your Environment Host URL)
- ENV_AUTH (The base64 encoding of the following string "demo_user:<your environment password>")
- Push code to main

