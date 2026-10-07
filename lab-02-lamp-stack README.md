# Lab 02: Deploying a LAMP Stack on GCP

## 🎯 Lab Objectives
- Deploy a pre-configured LAMP stack (Linux, Apache, MySQL, PHP) on Google Cloud.
- Utilize Google Cloud Deployment Manager for automated infrastructure provisioning.
- Verify web server accessibility and database connectivity.

---

## 🛠️ Instructions & Steps
1. **Tool Activation & Setup:**
   - Access the Google Cloud Console and open Cloud Shell.
   - Prepare the deployment configuration file for the LAMP stack.
2. **Deployment Execution:**
   - Execute the deployment command in the console:
     ```bash
     gcloud deployment-manager deployments create <deployment-name> --config <config-file>.yaml
     ```
3. **Verification & Access:**
   - Navigate to the VM Instances page to copy the `External IP` address.
   - Access the address via browser to verify the Apache default page, or connect via SSH for internal checking:
     ```bash
     gcloud compute ssh <instance-name>
     ```

---

## ⚠️ Errors & Troubleshooting
* **Error 1:** Deployment Manager error regarding resource or bucket naming conventions.
  - **Cause:** Using uppercase letters, spaces, or invalid special characters in the deployment name.
  - **Correction:** Modify the deployment name to strictly use lower-case letters, numbers, and dashes.

---

## 💡 Key Takeaways
- Understanding how Infrastructure as Code (IaC) via Deployment Manager accelerates multi-tier application deployment.
- Recognizing the importance of firewall rules for permitting HTTP (Port 80) web traffic.
