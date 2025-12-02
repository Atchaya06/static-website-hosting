# Static Website Hosting on AWS S3

## 📌 Project Overview
This project demonstrates how to host a static website using **Amazon S3**. It covers bucket creation, file uploads, permission configuration, and enabling website hosting. This is a beginner-friendly cloud computing project.

---

## 🎯 Objective
To deploy a static website (HTML, CSS, JS) using Amazon S3 and make it publicly accessible.

---

## ☁️ AWS Service Used
- Amazon S3 (Simple Storage Service)

---

## 📁 Files Used
- index.html
- style.css
- (Optional) error.html

---

## 🛠️ Steps to Host Website

### Step 1: Create an S3 Bucket
- Login to AWS Console
- Go to **S3**
- Click **Create Bucket**
- Enter unique bucket name
- Choose region
- Disable "Block all public access"
- Create bucket

---

### Step 2: Upload Website Files
- Open your bucket
- Click **Upload**
- Add `index.html`, `style.css`, etc.
- Make sure `index.html` is in the root directory

---

### Step 3: Set Bucket Permissions
Go to **Permissions > Bucket Policy** and add:

```json
{
  "Version": "2012-10-17",
  "Statement": [{
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
  }]
}
