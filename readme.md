# AWS S3 Static Website with CloudFront CDN

This project demonstrates how to host a static website using **Amazon S3** and deliver it globally using **Amazon CloudFront** with secure access controls.

---

## 🚀 Architecture Overview

User → CloudFront (CDN) → S3 Bucket (Static Website)

CloudFront caches content at edge locations and securely fetches files from S3 using **Origin Access Control (OAC)**.

---

## 🛠️ AWS Services Used

- Amazon S3 (Static Website Hosting)
- Amazon CloudFront (Content Delivery Network)
- Origin Access Control (OAC)
- IAM (implicit via CloudFront access policy)

---

## 🔐 Security Features

- S3 **Block Public Access** enabled
- Bucket accessible **only via CloudFront**
- CloudFront signed requests using OAC
- No public S3 access

---

## 📂 Files

- `index.html` – Main website page  
- `style.css` – Styling for the website  

---

## 📸 Screenshots

Screenshots of:
- S3 bucket creation
- Static website hosting configuration
- CloudFront distribution
- Final website output via CloudFront

(See `/screenshots` folder)

---

## 🌐 Live Demo (During Testing)

- CloudFront URL: `https://d2s09pcz1qqc96.cloudfront.net/'

*(Distribution disabled after testing to avoid costs)*

---

## 🧠 What I Learned

- Hosting static websites on Amazon S3
- Configuring CloudFront distributions
- Understanding Origin Access Control (OAC)
- Securing S3 buckets from public access
- CDN caching and global content delivery

---

## 👤 Author

**Vetrivel**  
Final Year IT Student  
Aspiring Cloud Engineer
