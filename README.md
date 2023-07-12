# Google Cloud Functions Course 
## Starting a project
To start a new project in Google Cloud, we can go to the GCP console
## Creating a virtual environment
First we have to install `python3-venv` with the following command:
```
python -m venv venv
```
To activate the virtual environment we do:
```buildoutcfg
.\venv\Script\activate
```
In order to add new packages to our new virtual environment, we create a file called `requirements.txt` and execute the following command:
```
pip install -r requirements.txt
```

The code can be tested by:
```
functions-framework --target hello_world --debug

```

## Deploy our functions
First, we have to set our project ID with the following command:
```
gcloud init
gcloud config set project [YOUR_PROJECT_ID] 
```
Then we deploy our function with this command:
```
gcloud functions deploy [FUNCTION_NAME] --runtime python311 --triger-http
```
