# Face Sentiment Analysis App (Python Flask)

## Technology Stack & Badges
[![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=flat&logo=google-cloud&logoColor=white)](https://cloud.google.com/)
[![AI-Gemini](https://img.shields.io/badge/AI-Gemini-orange?style=flat&logo=google-gemini&logoColor=white)](https://deepmind.google/technologies/gemini/)
[![Environment-Dev](https://img.shields.io/badge/Environment-Dev_UI-blueviolet?style=flat)](https://adk.dev)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A Python Flask web application that analyzes the sentiment (joy likelihood) of human faces in uploaded images. Built for deployment on Google App Engine, this app leverages Google Cloud's AI and data storage services to process and catalog facial expressions.

## App Interface Preview

![App Preview](app_images/Screenshot%202026-07-11%20112202.png)

---

## Architecture & Services

* **Frontend:** Responsive, modern UI built with HTML, Jinja2, and Bootstrap 5.
* **Compute:** Hosted on Google App Engine (Flexible Environment).
* **Storage:** Uploaded image files are securely stored in Google Cloud Storage.
* **Database:** Metadata (filename, upload timestamp, and sentiment analysis results) is logged in Google Cloud Datastore (NoSQL).
* **API:** Uses the Google Cloud Vision API for facial detection and sentiment analysis.

---

## Prerequisites

Before you begin, ensure you have the following:

* A Google Cloud Project with an active billing account.
* Google Cloud CLI (gcloud) installed and initialized.
* Python 3.12+ installed.
* The following APIs enabled in your Google Cloud Project:
  - Cloud Vision API
  - Cloud Datastore API

---

## Local Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/moonpy-a11y/sentimentAnalysis-with-Python-FlaskApp.git
   cd sentimentAnalysis-with-Python-FlaskApp
Install dependencies (virtual environment recommended):


```bash
pip install -r requirements.txt
Authenticate API Requests by setting your service account key:

```bash
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account-key.json"
Set up Cloud Storage Bucket variable:

```bash
export CLOUD_STORAGE_BUCKET="your-unique-bucket-name"
Run the application:

```bash
python main.py
Navigate to http://localhost:8080 in your web browser to test the application locally.

Google App Engine Deployment
To deploy this application to Google Cloud, you will use the provided app.yaml configuration file.

Open app.yaml and update the environment variables with your specific Cloud Storage bucket name.

Deploy the application using the Google Cloud CLI:

```bash
gcloud app deploy
Once the deployment finishes, view your live application:

```bash
gcloud app browse
---
```