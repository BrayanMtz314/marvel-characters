# Experiment Tracking with MLflow

In this chapter we'll see the basic components in the using of MLflow.

**Key component:**
- MLflow Tracking: A centralized repository that logs machine learning models parameters, metrics, artifacts, and reference to data used for model training. Experiment tracking gives insights into changes in models over time, and helps with model evaluation. 

- Model Registry: a centralized model store that allows to manage model's lifecycle, add tags, aliases and new model versions.

- Model Evaluation: a set of tools to facilitate model evaluation (GenAI and standard ML). 

- MLflow Tracing: enhances LLM observability in your generative AI  (GenAI) applications by capturing detailed information about execution of your application's services. (part of mlflow tracking)

Even though all these features are avairable both in the open-source version of MLflow and Databricks-managed MLflow, there are quite a lot of differences between managed and open-source versions.

**Differences between experiment Tracking vs registry**

- Experiment and registry have a different backend 

- Experiment can be found in a workspace

- Models are registered in Unity Catalog

**MLflow Experiment**

- Experiments in MLflow are the main unit of organization for ML model training runs 

- All MLflow runs belong to an experiment. Each MLflow run corresponds to a single execution of model code.

- All MLflow runs are logged to active experiment. MLflow Experiment can be created by using `mlflow.create_experiment` or `mlflow.set_experiment` commands

The notebook that implements this mlflow logic can be found in the [lecture3](../notebooks/lecture3.mlflow_experiment_tracking.py) file.

In order to use the notebook locally we need to fill in the `.env` with our PROFILE account.
Example:
```bash
PROFILE=adsfasdfg-adsfsadf-sadfas
```