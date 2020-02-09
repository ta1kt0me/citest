[![CircleCI](https://circleci.com/gh/ta1kt0me/citest.svg?style=svg)](https://circleci.com/gh/ta1kt0me/citest)

## Project Overview

The project is flask API application to provide predict housing prices in Boston which model has been trained based on [the data source site](https://www.kaggle.com/c/boston-housing).

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

Then, Send post request `./make_prediction.sh` .

```command
# Upload a docker image
docker login
./upload_docker.sh
```

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

## Directory

```
.
├── app.py             # Flask app
├── Dockerfile
├── Makefile
├── make_prediction.sh # a script to send POST data
├── model_data         # a directory for a model
├── output_txt_files   # outputs of logging
├── README.md
├── requirements.txt
├── run_docker.sh      # a script to run flask app as docker container
├── run_kubernetes.sh  # a script to run flask app as kubernetes cluster
└── upload_docker.sh   # a script to push docker images to a repository
```
