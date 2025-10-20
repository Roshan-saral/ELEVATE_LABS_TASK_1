# ELEVATE_LABS_TASK_1
TASK 1: Create a Cloud Storage Bucket and Upload Files

## 📘 WHAT I DID FOR THE PROJECT:-

1. 🪣 **Created S3 Bucket**  
   - Set up a new Amazon S3 bucket to host files.

2. 📤 **Deployed Image & Text File**  
   - 🖼️ Uploaded both an image and a text file to the bucket  
   - 🔗 Object URLs Generated 

   - 🌐 AWS automatically provided public URLs for each object  
   - 🌍 Accessed via Browser  
   - ✅ Successfully viewed both the image and text file using their respective URLs in a web browser
  

## 🗺️ Static Website Architecture (S3)

 ![static-website-s3-architecture-jpg](https://github.com/user-attachments/assets/e3e6dad8-ac2e-4d00-8ae7-0c879e18627b)



##  S3 Bucket Migration

![Alt text](https://miro.medium.com/v2/format:jpg/resize:fill:112:112/gravity:fp:0.50:0.50/1*ClAVK-vmBBqzex8eLmWkCw.gif)

### 📦 What This Diagram Represents

The image above illustrates a typical **S3 Bucket Migration** between two AWS accounts. This is a common scenario in cloud operations where data needs to be transferred securely across environments — such as during team handovers, mergers, or infrastructure upgrades.

- **AWS Account - 1** contains the source S3 bucket with existing data.
- **AWS Account - 2** is the destination where the data is migrated.
- The arrows represent the transfer of objects (files, folders, metadata) using AWS CLI, SDKs, or automated services like **AWS DataSync**.

---

### 🔐 Why S3 Migration Matters

- Ensures **data continuity** across teams and projects
- Enables **centralized storage** for analytics, backups, or compliance
- Supports **multi-account architecture** for better security and cost control
- Prepares infrastructure for **automation, versioning, and lifecycle policies**

---

### 🛠️ Tools Commonly Used

- `aws s3 cp` / `sync` — for manual transfers
- **AWS DataSync** — for automated, large-scale migrations
- **Cross-account IAM roles** — for secure access between accounts
- **S3 Replication** — for continuous sync across buckets

---

This migration workflow is a foundational skill for cloud engineers and DevOps professionals. Understanding it helps you manage real-world infrastructure with confidence and precision.




# ☁️ Cloud Storage Bucket & File Upload Task

This project demonstrates the basics of cloud object storage using **AWS S3** or **Google Cloud Storage** (Free Tier). It walks through creating a bucket, uploading files, and accessing them via public URLs — a foundational skill for cloud engineers and developers.

---

## 🎯 Objective

Understand how cloud object storage works by:

- Creating a storage bucket
- Uploading a sample file
- Accessing the file via aan object or public URL

---

## 🛠️ Tools Used

- [AWS S3](https://aws.amazon.com/s3/) (Free Tier)  

---

## 📚 Step-by-Step Guide

1. **Create a Free Cloud Account**  
   - [AWS Free Tier](https://aws.amazon.com/free/)  

2. **Create a Storage Bucket**  
   - Navigate to **Cloud Storage** → **Create Bucket**
   - Choose a **globally unique name** for your bucket
   - Select a region (e.g., `us-east1`)

3. **Configure Permissions**  
   - Leave default settings (private or public as needed)

4. **Upload a Sample File**  
   - Use a `.txt` or `.png` file for demonstration

5. **Copy the Public URL** (MAKING public access as enabled for objects that is for image and text file)

6. **Test the Link in Your Browser**  
   - Confirm the file is accessible

---

## ✅ Deliverables

- 📸 **Screenshots** showing successful file uploads.
- 🔗 **Public URL** given in the files.

---



## CHALLENGES FACED:
 - WHEN OBJECTS WHERE PRIVATE HAD TO CHANGE SOME PERMISSONS OF THE S3 BUCKET TO MAKE IT PUBLIC.
 - EVEN AFTER THIS STILL THE URL WAS NOT WORKING BECAUSE NOW THE CONCERN WAS BUCKET WAS PUBLIC BUT NOT THE OBJECT SO WE HAD TO MAKE THE OBJECT PUBLIC BY CHANGING THE ACL PERMISSIONS OF THE IMAGE .PNG OR .TXT FILE.
 - IN BETWEEN THERE WAS A SERVER OUTAGE FOR NORTH VIRGINIA AND IT WAS AN OPERATIONAL ISSUE AND HAD TO WAIT IN ORDER TO DELETE THE S3 BUCKET.BUT AFTER SOMETIME THE SERVICES HAD COMEBACK IN THE REGION AND I WAS ABLE TO DELETE MY S3 BUCKET FROM THE MANAGEMENT CONSOLE.

## 🚀 Daily AWS S3 CLI Commands for Corporate Operations

Mastering these commands is essential for cloud engineers, DevOps teams, and automation workflows in enterprise environments. Here's your go-to cheat sheet 🧠:

---

### 🪣 Bucket Management

| 🔧 Command | 📝 Description |
|-----------|----------------|
| `aws s3 ls` | List all S3 buckets |
| `aws s3 mb s3://bucket-name` | Create a new bucket |
| `aws s3 rb s3://bucket-name` | Remove an empty bucket |
| `aws s3 rb s3://bucket-name --force` | Delete bucket and all contents |

---

### 📁 Object Operations

| 📦 Command | 📝 Description |
|-----------|----------------|
| `aws s3 cp file.txt s3://bucket-name/` | Upload a file to S3 |
| `aws s3 cp s3://bucket-name/file.txt .` | Download a file from S3 |
| `aws s3 mv file.txt s3://bucket-name/` | Move a file to S3 |
| `aws s3 rm s3://bucket-name/file.txt` | Delete a file from S3 |
| `aws s3 sync ./local-folder s3://bucket-name/` | Sync local folder to S3 |
| `aws s3 sync s3://bucket-name/ ./local-folder` | Sync S3 bucket to local folder |

---

### 🔐 Access & Permissions

| 🛡️ Command | 📝 Description |
|-----------|----------------|
| `aws s3api get-bucket-policy --bucket bucket-name` | View bucket policy |
| `aws s3api put-bucket-policy --bucket bucket-name --policy file://policy.json` | Apply bucket policy |
| `aws s3api get-object-acl --bucket bucket-name --key file.txt` | View object ACL |
| `aws s3api put-object-acl --bucket bucket-name --key file.txt --acl public-read` | Make object public |

---

### 🌐 Static Website Hosting

| 🌍 Command | 📝 Description |
|-----------|----------------|
| `aws s3 website s3://bucket-name/ --index-document index.html --error-document error.html` | Enable static website hosting |
| `aws s3api put-bucket-policy --bucket bucket-name --policy file://website-policy.json` | Set public access for website |

---

### 🧪 Troubleshooting & Metadata

| 🧭 Command | 📝 Description |
|-----------|----------------|
| `aws s3api list-objects --bucket bucket-name` | List all objects with metadata |
| `aws s3api head-object --bucket bucket-name --key file.txt` | View object metadata |
| `aws s3api get-bucket-location --bucket bucket-name` | Check bucket region |

---

## 🧠 Pro Tip

Before using any of these commands, make sure your AWS CLI is configured:
```bash
aws configure

```
## 📁 Folder Structure
```
cloud-storage-task/
├── FILE/                 # Upload screenshots of successful file upload
├── screenshots/          # Sample text/image files used for upload
├── README.md             # Project documentation





