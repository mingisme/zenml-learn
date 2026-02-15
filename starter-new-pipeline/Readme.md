# Starter New Pipeline

A ZenML machine learning pipeline project that trains a Support Vector Classifier (SVC) on the Iris dataset.

## Project Setup

### 1. Create the Project

```bash
mkdir starter-new-pipeline
cd starter-new-pipeline
poetry init
```

### 2. Install Dependencies

```bash
poetry add "setuptools<70.0.0"
poetry add "zenml[server]==0.74.0"
poetry add matplotlib
poetry add scikit-learn
poetry add pandas
```

## Project Structure

```
starter-new-pipeline/
├── Readme.md
├── poetry.lock
├── pyproject.toml
└── run.py
```

## Pipeline Overview

The `run.py` file contains a ZenML pipeline with the following components:

- **training_data_loader**: Loads the Iris dataset and splits it into training and test sets
- **svc_trainer**: Trains a Support Vector Classifier with configurable gamma parameter
- **training_pipeline**: Orchestrates the data loading and model training steps

## Running the Pipeline

Execute the pipeline with:

```bash
poetry run python run.py
```

## Features

- Uses ZenML for ML pipeline orchestration
- Trains an SVC model on the classic Iris dataset
- Configurable gamma parameter for the SVC model
- Returns training accuracy metrics
- Type-annotated pipeline steps for better code clarity

## Requirements

- Python >=3.11 <3.13
- Poetry for dependency management

## Viewing the Dashboard

To monitor and inspect your pipeline runs, start the ZenML dashboard:

```bash
poetry run zenml login --local
```

This will launch the local ZenML dashboard where you can:
- View executed pipeline runs
- Inspect step outputs and artifacts
- Monitor pipeline performance
- Debug failed runs
- Visualize the pipeline DAG

Open the provided URL in your browser to access the dashboard and check your executed pipeline.
