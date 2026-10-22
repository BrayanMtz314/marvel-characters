# Section 6: Deploying Model Serving Endpoint

### Databricks Serverless Endpoints for ML Models

A fully managed, serverless solution for deploying MLflow models as RESTful APIs in Databricks-no infrastructure setup or management required. 

- **Key Features:**
    - Easy deployment of registered MLflow models
    - Automatic scaling, including optional scale-to-zero
    - Built-in monitoring via Databricks UI (latency, throughput, error rates)
    - Supports batch and real-time inference. 

- **Why use it?**
    - Simplifies deployment from experimentation to production
    - Ideal for teams that want to focus on ML, not infrastructure
    - Works out-of the box with the databricks MLflow Model Registry.

- **Databricks serving is serverless:**
    - No ability to choose runtime
    - No control over cluster size (4gb RAM limit)

- Can choose the workload size:
    - Small: 4 units
    - Medium: 8-16 units
    - Large: 16-64 units
    - On request, XL, 2XL, 3XL (512 units) sizes are available
    - if scale-to-zero is enabled, the lower bound for each workload size is 0.

### Compute Units, QPS, and Performance Limits

- Each unit can process one request at a time
- Autoscaling is based on the number of required units (even if a single unit is not optimally utilized, for example, only using 5% CPU)

Number of required units = (queries per second)*(model processing time)

Example: 
    QPS = 1000
    Model processing time (MPT) = 0.02 s (20 ms)
    Number of required units = 20

Maximum QPS (if MPT=0.02): 512/0.02=25600 - this is a limit per endpoint

### Notebook Notes

For this practice we need to add this variables to the `.env` file.

- PROFILE=adsf-adfasd-asdf
- DBR_TOKEN=
- DBR_HOST=