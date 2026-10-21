# Model Logging and Registration

**MLflow Model**

- An Mlflow Model is a standard format for packaging machine learning models

- MLflow provides "flavors" as wrappers for specific machine learning libraries.

- Flavors ensure consistent saving, loading, and inference deployment from diverse libraries.

- Custom pyfuncs through the PythonModel base class, which offers flexibility for embedding any library's model into MLflow's structured system

**Main supported model flavors**

- H2O (h2o)
- Keras (keras)
- MLeap (mleap)
- PyTorch (pytorch)
- Scikit-learn (sklearn)
- Spark MLlib (spark)
- TensorFlow (tensorflow)
- ONNX (onnx)
- XGBoost (xgboost)
- LightGBM
- OpenAI
- LangChain
- Transoformers
- etc..

You can find more about the avairable flavors in [mlflow flavors documentation](https://mlflow.org/docs/latest/api_reference/python_api/mlflow.models.html)

Continue in 52:54
