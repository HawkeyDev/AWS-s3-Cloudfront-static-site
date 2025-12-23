# AWS S3 + CloudFront Static Website – Setup Steps

This document describes the complete process followed to deploy a secure,
serverless static website using Amazon S3 and Amazon CloudFront.

---

## Step 1: Create S3 Bucket
- Created a General Purpose S3 bucket
- Selected default AWS region
- Enabled default encryption (SSE-S3)

---

## Step 2: Upload Website Files
- Uploaded `index.html` and `style.css`
- Verified files exist at the root of the bucket

---

## Step 3: Disable Public Access
- Enabled **Block all public access** on the S3 bucket
- Ensured the bucket is not publicly accessible

---

## Step 4: Disable Static Website Hosting
- Disabled S3 static website hosting
- Prepared bucket for private access through CloudFront (REST endpoint)

---

## Step 5: Create CloudFront Distribution
- Created a CloudFront distribution
- Configured S3 REST endpoint as the origin
- Enabled HTTPS using CloudFront default certificate

---

## Step 6: Configure Origin Access Control (OAC)
- Created and attached an Origin Access Control (OAC)
- Enabled signed requests from CloudFront to S3
- Restricted S3 access to CloudFront only

---

## Step 7: Update S3 Bucket Policy
- Allowed access to `cloudfront.amazonaws.com` service principal
- Restricted access using CloudFront distribution ARN
- Ensured least-privilege permissions

---

## Step 8: Set Default Root Object
- Configured CloudFront default root object as:

index.html
---

## Step 9: Cache Invalidation
- Created CloudFront invalidation:

invalidation-/*
- Forced CloudFront to fetch updated content from S3

---

## Step 10: Verification
- Accessed the website using CloudFront HTTPS URL
- Confirmed successful website loading
- Verified S3 bucket remained private

---

## Step 11: Cost Management
- Disabled or deleted CloudFront distribution after testing
- Kept S3 Block Public Access enabled
- Ensured zero or minimal AWS cost

---

## Outcome
Successfully deployed a secure, serverless static website using Amazon S3
and CloudFront following industry-standard security and cost best practices.