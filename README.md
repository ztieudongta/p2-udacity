# Overview

In this project, we will build an flask application that can predict house price of Boston or California. This project is applied Continuous Integration (CI) by using Github Actions and we use Azure App Service to deploy app to website and create a Azure Pipeline to apply changes automatically from code in github to web app so that we can apply Continuos Delivery (CD).

## Project Plan

* [Link to a Trello board for the project](https://trello.com/b/sachbUu9/p2-udacity)
* [Link to a spreadsheet that includes the original and final project plan](https://docs.google.com/spreadsheets/d/1VS6FavzHqJ2QgfqKAtlMbNunuqqQ5wceTRKVGWMbJgI/edit?usp=sharing)


## Instructions

* Architectural Diagram

![image](https://user-images.githubusercontent.com/35824913/209517441-60ebe9d4-5afe-48b9-a083-18973af83139.png)


<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


