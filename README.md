#  Beginning MLOps

## Data

Get the data from Kaggle website [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download) and save it inside the `data` folder

# Prepare

Install the poetry environment from the project base folder

```
poetry install --no-root
```


## Run

This time we have two folders that have very similar scripts but with one particular difference. Run either one of them (finishing the other if started)

### beginning mlops

Here from one terminal run 

```Shell
cd beginningmlops
poetry run mlflow ui
```

and then from another terminal run

```Shell
cd beginningmlops
poetry run python practice1MLFlow.py
```

With that when you go to http://localhost:5000/ you will see the MLOps UI and can see the runs on the experiment `scikit_learn_experiment`

### servermlops

Here run from one terminal

```Shell
cd servermlops
poetry run mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 0.0.0.0 --port 5000
```
and then from another terminal run

```Shell
cd servermlops
poetry run python practice1MLFlow.py
```

Here to by going to http://localhost:5000/ you will see the MLOps UI and can see the runs on the experiment `scikit_learn_experiment`

In order to learn the difference go to the Medium article here