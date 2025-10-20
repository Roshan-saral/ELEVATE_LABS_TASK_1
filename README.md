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



##  S3 Bucket Migration

![Alt text](https://miro.medium.com/v2/format:jpg/resize:fill:112:112/gravity:fp:0.50:0.50/1*ClAVK-vmBBqzex8eLmWkCw.gif)



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
  _or_  
- [Google Cloud Storage](https://cloud.google.com/storage) (Free Tier)

---

## 📚 Step-by-Step Guide

1. **Create a Free Cloud Account**  
   - [AWS Free Tier](https://aws.amazon.com/free/)  
   - [Google Cloud Free Tier](https://cloud.google.com/free)

2. **Create a Storage Bucket**  
   - Navigate to **Cloud Storage** → **Create Bucket**
   - Choose a **globally unique name** for your bucket
   - Select a region (e.g., `us-east1`)

3. **Configure Permissions**  
   - Leave default settings (private or public as needed)

4. **Upload a Sample File**  
   - Use a `.txt` or `.png` file for demonstration

5. **Copy the Public URL** (if public access is enabled)

6. **Test the Link in Your Browser**  
   - Confirm the file is accessible

---

## ✅ Deliverables

- 📸 **Screenshots** showing successful file uploads.
- 🔗 **Public URL** given in the files.

---



## CHALLENGES FACED:
 - WHEN OBJECTS WHERE PRIVATE HAD TO CHANGE SOME PERMISSONS OF THE S3 BUCKET TO MAKE IT PUBLIC.
 - EVEN AFTER THIS STILL THE URL WASNOT WORKING BECAUSE NOW THE CONCERN WAS BUCKET WAS PUBLIC BUT NOT THE OBJECT SO WE HAD TO MAKE THE OBJECT PUBLIC BY CHANGING THE ACL PERMISSIONS OF THE IMAGE .PNG OR .TXT FILE.
 - IN BETWEEN THERE WAS A SERVER OUTAGE FOR NORTH VIRGINIA AND IT WAS AN OPERATIONAL ISSUE AND HAD TO WAIT IN ORDER TO DELETE THE S3 BUCKET.
   

## 📁 Folder Structure

```bash
cloud-storage-task/
├── screenshots/           # Upload screenshots of successful file upload
├── sample-files/          # Sample text/image files used for upload
├── README.md              # Project documentation


