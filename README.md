[![CircleCI](https://circleci.com/gh/ta1kt0me/citest.svg?style=svg)](https://circleci.com/gh/ta1kt0me/citest)

## Project Overview

The project is flask API application to provide predict housing prices in Boston which model has been trained based on [the data source site](https://www.kaggle.com/c/boston-housing).

### Setup

#### Development


#### Docker

```command
# build an image and start up flask app
./run_docker.sh

# Open another teminal, post predict
./make_prediction.sh
```

```command
# push a docker image to a image registory
docker login
./upload_docker.sh
```

#### Kubernetes

```command
# start up flask app as kubernetes cluster
./run_kubernetes.sh

# Open another teminal, post predict
./make_prediction.sh
```

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

```command
# Setup virtualenv
make setup
source ~/.devops/activate

# Install dependencies
make install

# Execute Lint
make lint
```

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
