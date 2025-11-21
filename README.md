# Dockernf

This tool helps ease working with Docker for setting up Nextflow jobs.


## Setup

A parameter file or runtime parameters can be passed which must include the following

```yaml
DOCKERFILE: ./filepath/Dockerfile
ECR_REPO: repo_name
IMAGE_URI: 12345678.dkr.ecr.awsregion.amazonaws.com/repo_name:latest

```

## Usage

To create ecr repo:

```bash
nextflow run prteek/dockernf -ops create_ecr_repo -params-file params.yml
```


To build the Docker image:

```bash
nextflow run prteek/dockernf -ops build -params-file params.yml
```


To push the Docker image to ECR:

```bash
nextflow run prteek/dockernf -ops push -params-file params.yml
```
