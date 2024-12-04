# Menjadi Google Cloud Engineer

Notes API (backend) untuk materi Cloud Run di kelas Menjadi Google Cloud Engineer

### Enable Google Cloud services

gcloud services enable artifactregistry.googleapis.com cloudbuild.googleapis.com run.googleapis.com

### Make Artifact Registry repository

gcloud artifacts repositories create backend --repository-format=docker --location=asia-southeast2 --async

### Make container image

gcloud builds submit --tag asia-southeast2-docker.pkg.dev/${GOOGLE_CLOUD_PROJECT}/backend/notes-api:1.0.0

### Deploy Notes API to CLoud Run

gcloud run deploy --image asia-southeast2-docker.pkg.dev/${GOOGLE_CLOUD_PROJECT}/backend/notes-api:1.0.0
