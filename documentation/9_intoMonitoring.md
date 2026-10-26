# Section 9: Into Monitoring

### Things to monitor for ML Systems

- Generic Monitoring (software engineering)
    - System health
    - Errors
    - Latency

- ML-specific monitoring
    - Data quality checks
    - Data drift - questionable
    - Model drift

- Costs And Business value:
    - infrastructure costs
    - Business value
    - KPIs

- Fairness Adn bias (requirement for some ML systems like fraud detection)

### DevOps vs MLOps

Devops covers:

    - Code
    - data model
    - enviroment
    - infrastructure

MLOPs covers devops + statistical properties of the data.

### Data Drift

DAta drift occures when the distribution of the input data changes over time.

Example (housing prices):

There are a lot of new houses entering the market in the district. preferences of people buying houses didn't change, relationship between the inputs and the price didn't change.

This data drift may have resulted in the overall drop in model performance, just because the model in general doesn't prefict prices weel for new houses, and that group became larger.

Data drift may be a symptom of model drift.


# Lakehouse monitoring

Databricks offers "lakehouse monitoring," a tool used to monitor the statistical properties of data and machine learning models.

For different scenarios (inference, time series, snapshots), creates:
- Profile metrics table
- Drift metrics table
- Dashboard

For inference and time series scenarios, windows are creted ("5 minutes", "30 minutes", "1 hour", "1 day", "<n> week(s)", "1 month", or "1 year").


# Inference table=

An inference table in Databricks is an automated Unity Catalog-managed Delta Table that captures and logs live prediction requests and responses sent to model serving endpoints.

Key Features & Capabilities

- Automatic Logging: When enabled, Databricks automatically records incoming queries, model outputs, execution times, metadata, and MLflow traces without requiring custom logging code.
- Centralized Governance: Because they are stored as Delta tables in Unity Catalog, you can discover, share, and govern the prediction data using standard Databricks permissions.
- Querying & Monitoring: You can query the tables directly using Databricks SQL or notebooks to run data analysis, track model performance, and spot data drift.
- Feedback Loops & Training: By joining inference tables with ground truth labels, teams can build training corpora to fine-tune or retrain models
    
