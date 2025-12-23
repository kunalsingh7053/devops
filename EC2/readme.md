# 🚀 AWS EC2 Server Creation Guide (Step-by-Step)

This guide explains the complete flow of creating and setting up a server on **AWS EC2** for deploying applications.

---

## 🧠 What is EC2?

EC2 (Elastic Compute Cloud) is a virtual server provided by AWS that allows you to run applications on the cloud.

---

## 🪜 Step-by-Step Flow to Create an EC2 Server

---

## 1️⃣ Create an AWS Account
- Go to https://aws.amazon.com
- Sign up or log in to your AWS account
- Open **AWS Management Console**

---

## 2️⃣ Open EC2 Dashboard
- Search **EC2** in AWS Console
- Click **EC2 → Instances**
- Click **Launch Instance**

---

## 3️⃣ Choose an Amazon Machine Image (AMI)
Select an operating system:

✅ Recommended:
- **Ubuntu Server 22.04 LTS**

Click **Select**

---

## 4️⃣ Choose Instance Type
Choose server size based on need:

- **t2.micro** (Free Tier eligible) ✅
- t3.small / t3.medium (for higher load)

Click **Next**

---

## 5️⃣ Create or Select Key Pair (VERY IMPORTANT)
- Click **Create new key pair**
- Name it (example: `hallex-test-1`)
- Type: **RSA**
- Format: **.pem**
- Download and store it safely

⚠️ Never share or push this file to GitHub.

---

## 6️⃣ Configure Network & Security Group
Create a new security group and allow:

| Type | Port | Source |
|---|---|---|
| SSH | 22 | My IP |
| HTTP | 80 | Anywhere |
| HTTPS | 443 | Anywhere |
| Custom TCP | 3000 | Anywhere (for Node app) |

---

## 7️⃣ Configure Storage
- Default 8 GB is enough for beginners
- Increase if needed

Click **Launch Instance**

---

## 8️⃣ Get Public IP Address
- Go to **EC2 → Instances**
- Select your instance
- Copy **Public IPv4 Address**

Example:
```text
13.xxx.xxx.xxx
