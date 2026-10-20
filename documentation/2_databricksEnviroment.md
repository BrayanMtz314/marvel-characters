# Databricks Environment

We'll be using Databricks Community Edition, which provides the necessary free-tier features we need.

We are using the `marvel-characters` repository as our main source code. [Repo link](https://github.com/marvelousmlops/marvel-characters)

You can view the project's configuration properties in the [`project_config_marvel.yml`](../project_config_marvel.yml) file.

Using the Databricks UI, we created the following Unity Catalog structure:

- **Catalogs**
    - `mlops_dev`
    - `mlops_prd`
    - `mlops_acc`

- **Schemas**
    - `mlops_dev.marvel_characters`
    - `mlops_prd.marvel_characters`

To use Databricks from the terminal, we need to install the Databricks CLI. You can follow the step-by-step guide in the [Databricks CLI documentation](https://docs.databricks.com/aws/en/dev-tools/cli/tutorial?language=Linux%2C%C2%A0macOS).

We updated the Databricks target host in [`databricks.yml`](../marvel-characters/databricks.yml) to match the actual host URL found in the Databricks interface.

During development, we'll use the Databricks VS Code extension, which can be found in the extensions marketplace. It uses the project configuration and the Databricks CLI to communicate with the workspace.

The [`pyproject.toml`](../marvel-characters/pyproject.toml) file contains the project's Python dependencies. Run `uv sync` to download all the necessary packages:

```bash
uv sync --extra dev
```

To use the code directly in Databricks, we can link a Git folder via the UI.

After adding the Git folder to our workspace, we can configure the environment variables. The only change required here is setting the environment version to `3`, which is the most recent version.

## The Project in Detail

The dataset is sourced from Kaggle and contains information about Marvel Characters.

![MarvelCharactersContent](../images/MarvelCharactersContent.png)

We are running the cells in the [lecture2](../notebooks/lecture2.marvel_data_preprocessing.py) notebook. This notebook utilizes the `DataProcessor` class located in the [data_processor.py](../src/marvel_characters/data_processor.py) file. This class helps us preprocess the data, rename columns, clean the dataset, drop null values, and upload the final tables to the Databricks catalog.