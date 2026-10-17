# MLOps Principles and tools

Welcome to the first sections! In this section we'll cover the principles in machine learning engineering. 

- **MLOPS:** is a set of practices that combines machine learning, software engineering (DevOps), and data engineering to automate, deploy, and manage machine learning models in production.


### Core Principles

- Traceability
- Reproducibility
- Code Quality
- Monitoring
- Documentation
- A/B testing and experimentation
- Feature stores
- Explainability

### MLOps Tooling

The tools could be categorized based on their functionality.

- Version Control: Git, Gitlab, Bitbucket, AWSCodeCommit
- CI/CD: Jenkings, Acure Devops, Github actions, etc.
- Orchestration: Airflow, Argo workflows, databricks workflow.
- Model Registry: MLflow, Amazon SageMaker.
- Compute: Databricks compute, Kubernetes, Azure, ML SageMaker
- Serving: Databricks, Kubernetes, Azure, ML SageMaker
- Monioring: There are many tools here, but they are generally customized based on the project model.
- Contianer Registry: Dockerhub
- Feature Store: Databrick, hopsworks, FEAST

### DEVOPS != MLOPS

DevOps automates and streamlines traditional software development, while MLOps extends these principles to manage the unique lifecycle of machine learning (ML) models.

In an ideal scenario, developers should be able to deploy their software, and machine learning engineers should be able to deploy machine learning models. However, this rarely happens. It is why the MLOps team exists.

### MLOPS with databricks

fortunately, databricks provide the complete tools necessary for mlops.

![Databricks Tools](../images/databricksTools.png)