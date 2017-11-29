# NBI Data Visualization 

### Executive Summary

This application helps in visualizing the Bridge data which [National Bridge Inventory (NBI)](https://www.fhwa.dot.gov/bridge/nbi.cfm) annually submit to FHWA by the States, Federal agencies, and Tribal governments.

The purpose of this project is to provide a web application to visualize the NBI data and help users of this web application to analyze the NBI data in a fast and secure manner. Through this web application, a user will be able to create an account to get access to the application and can perform analysis using various forms of visualizations. The web application users may have access all or some of the features. It provides search options, Summaries, Tabular representations and various 2D charts based on the NBI data. different variants like Bridge Record Distribution by State, by Ownership, by Deck Area, Distribution of Bridges by Total Average Daily Traffic, Percentages of Bridges Identified as Scour Critical Bridges in the United States, etc. Main features of this web application are the secure and fast retrieval of the NBI data, Presenting the NBI data in the tabular form, 2 Dimensional Charts like Pie chart, Bar chart, Maps included Charts, etc. These features help users of this application to quickly understand and analyze the NBI data quickly and make further vital decisions for the actual maintenance teams by reporting their analysis.

The NBI Data Visualization application is developed using Django REST framework and EmberJS, which enables the test-driven development and achieves an acceptable level of web application security.

### Requirements
* Docker (https://www.docker.com/)

### Installation
The NBI Data Visualization application will run on docker. Thus you would require building the docker image from the provided DockerFile using Docker Compose.

#### Steps

```bash
git clone --recursive https://github.com/akhampariya/NBIDataVisualization.git
cd NBIDataVisualization
docker-compose build
```
The Docker-Compose command will create few docker containers with all of the requisite installed dependencies to run the development environment.

### Initial Setup
After installation, the basic setup is required.

#### Django
We need to initialize the Django database in Postgres

```bash
docker-compose run django bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser --username admin --email admin
exit
```
Specify a password for admin. In development, use for simplicity.

### Run the app
```bash
docker-compose up
```

### License
This repo is licensed under [GPL v3](/LICENSE).

Copyright (c) Ajay Khampariya, Shrikanth Vadla 2017

### Contribute

You can help this project in many ways, such as suggestions, reporting issues and contribute in coding.  
