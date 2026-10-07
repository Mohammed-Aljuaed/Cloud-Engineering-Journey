# Lab 01: Explore the Google Cloud Console and Cloud Shell

## 🎯 Lab Objectives
- Get access to Google Cloud and navigate the Console.
- Create a Cloud Storage bucket using the Cloud Console GUI.
- Create a Cloud Storage bucket using the Cloud Shell CLI.
- Explore Cloud Shell features and manage files.

---

## 🛠️ Key Commands Used

1. Create a bucket via CLI:
```bash
gcloud storage buckets create gs://[BUCKET_NAME]
⚠️ Errors Encountered & Troubleshooting
Error: HTTPError 400: Invalid bucket name
Cause: Using uppercase letters or invalid characters (like underscores _) in the bucket name.
Solution: Bucket names must consist exclusively of lowercase letters, numbers, and dashes.
