# Project Front-End Notes App for Menjadi Google Cloud Engineer
Running a project in production:

1. ``npm install``
2. ``npm run build``
3. ``npm run start``

---
#### Create repo

gcloud artifacts repositories create frontend --repository-format=docker --location=asia-southeast2 --async

#### Make container image

gcloud builds submit --tag asia-southeast2-docker.pkg.dev/${GOOGLE_CLOUD_PROJECT}/frontend/notes-app:1.0.0

#### Deploy to Cloud Run

gcloud run deploy --image asia-southeast2-docker.pkg.dev/${GOOGLE_CLOUD_PROJECT}/frontend/notes-app:1.0.0
