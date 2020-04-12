# My First GCP Cloud Run in Python
This is a demo project from https://cloud.google.com/run/docs/quickstarts/build-and-deploy.
Demo: https://myfirstcloudrun-ow4mjcgp7a-de.a.run.app/

# CI/CD
## Build
1. Find _PROJECT-ID_
    ```
    gcloud config get-value project
    ```

2. Build container image using Cloud Build 
    ```
    gcloud builds submit --tag gcr.io/PROJECT-ID/myfirstcloudrun
    ```

## Deploy
1. Deploy using the following command 
    ```
    gcloud run deploy --image gcr.io/PROJECT-ID/myfirstcloudrun --platform managed
    ```
