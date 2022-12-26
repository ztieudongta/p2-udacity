# Overview

In this project, we will build an flask application that can predict house price of Boston or California. This project is applied Continuous Integration (CI) by using Github Actions and we use Azure App Service to deploy app to website and create a Azure Pipeline to apply changes automatically from code in github to web app so that we can apply Continuos Delivery (CD).

## Project Plan

* [Link to a Trello board for the project](https://trello.com/b/sachbUu9/p2-udacity)
* [Link to a spreadsheet that includes the original and final project plan](https://docs.google.com/spreadsheets/d/1VS6FavzHqJ2QgfqKAtlMbNunuqqQ5wceTRKVGWMbJgI/edit?usp=sharing)


## Instructions

## Architectural Diagram

![image](https://user-images.githubusercontent.com/35824913/209519200-e645e3e5-09ad-40bb-b229-aa78278479d9.png)


## Instructions for running this project

### Prerequisites:

* [Github account](https://github.com/)

* [Azure account](https://azure.microsoft.com/en-us/)

* [Azure devops account](https://dev.azure.com/f)

### Create a new fork of this project

* You need to create a new fork of this project so that you can work on it easily

![image](https://user-images.githubusercontent.com/35824913/209524110-d0a5882a-fd6b-474a-916f-ca0acf1d9931.png)

* Delete two yml files on the repo: azure-pipelines.yml and .github/workflows/python-app.yml so that you create your own yml files.

### Create and configure ssh key to github account

* Go to Azure portal and create a new shell or bash command

* Create your ssh key and add to your github setting

```
ssh-keygen -t rsa
cat <your-keyfile-path>
```
* Go to [Github key setting](https://github.com/settings/keys) and add created key

### Clone project into Azure Cloud Shell

* Copy SSH path to clone your project into Azure Cloud Shell

![image](https://user-images.githubusercontent.com/35824913/209527012-240c94d8-5fc1-4ba2-aa25-5cac589e9fa6.png)

```
git clone <your-SSH-path>
```

### Create and active the python virtual environment and run project

* You need to create python virtual environment inside your project folder

```
python3 -m venv ~/.myrepo
source ~/.myrepo/bin/activate
```

* Run this project following to Makefile

```
make all
```
After running this command, your bash/shell cmd should be like blow:

![image](https://user-images.githubusercontent.com/35824913/209558658-7ccfa8d0-a441-4f3d-a87b-0b44db6ad2f3.png)

* Host web app by using Azure App Service

```
az webapp up --name <yourwebappname> --resource-group <yourresourcegroup> --runtime "PYTHON:3.9" --location <yourlocation> --sku B1
```
After hosting web app, you can open website by direct url

![image](https://user-images.githubusercontent.com/35824913/209559186-ef3496cb-f52f-4123-8a64-68123f90ec1d.png)

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


