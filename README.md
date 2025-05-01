# 🚀 Launching an EC2 Instance Using AWS Management Console

This guide provides step-by-step instructions to launch an Amazon EC2 (Elastic Compute Cloud) instance using the AWS Management Console.


## ✅ Prerequisites

Before you begin, make sure:

- You have an **active AWS account**.
- You are signed into the **AWS Management Console**.
- You are familiar with basic AWS terminology (like instance types, key pairs, security groups).



## 🧭 Steps to Launch an EC2 Instance via Console

### 🥇 Step 1: Sign in to AWS Console

1. Visit: [https://console.aws.amazon.com](https://console.aws.amazon.com)
2. Sign in with your **IAM user** or **root account** credentials.



### 🥈 Step 2: Navigate to EC2 Dashboard

1. In the AWS Console, search for **EC2** in the search bar.
2. Click on **EC2** to go to the EC2 Dashboard.



### 🥉 Step 3: Launch a New Instance

1. Click on **Launch Instance**.
2. Fill in the following details:


#### 🔹 Name and Tags
- Enter a name for your instance (e.g., `MyFirstEC2`).


#### 🔹 Application and OS Image (AMI)
- Select an Amazon Machine Image (AMI), e.g., **Amazon Linux 2023 AMI**.


#### 🔹 Instance Type
- Choose an instance type (e.g., `t2.micro` for Free Tier eligibility).


#### 🔹 Key Pair (Login)
- Select an existing key pair or create a new one.
- Download the `.pem` file if you create a new key pair (save it securely).


#### 🔹 Network Settings
- Choose an existing **VPC and subnet** or keep the defaults.
- Allow SSH traffic from **your IP** or **Anywhere (0.0.0.0/0)** for testing (not recommended for production).


#### 🔹 Configure Storage
- Accept the default (usually 8 GB for Amazon Linux).



### 🏁 Step 4: Launch Instance

1. Click **Launch Instance** at the bottom of the page.
2. Wait for the instance to be initialized.
3. Go to **View Instances** to see your instance running.



### 🧪 Step 5: Connect to EC2 Instance

1. Select your instance from the list.
2. Click **Connect** at the top.
3. Choose the **SSH client** tab.
4. Follow the provided SSH command:

```bash
ssh -i "your-key.pem" ec2-user@<your-public-ip>
```

✅ Make sure your key file has correct permissions:

```bash
chmod 400 your-key.pem
```



## 🧹 Step 6: Terminate the Instance (To Avoid Charges)

1. In the EC2 dashboard, select the instance.
2. Click **Instance State > Terminate Instance**.
3. Confirm the termination.



## 📌 Note:

- `t2.micro` is Free Tier eligible (750 hours/month).
- Open ports (like SSH) only to trusted IPs.
- Store `.pem` files securely; you can’t download them again.



## 📎 Resources

- [EC2 Documentation](https://docs.aws.amazon.com/ec2/index.html)
- [Free Tier Info](https://aws.amazon.com/free/)
- [Amazon Linux Guide](https://docs.aws.amazon.com/linux/)


🟢 You’ve successfully launched an EC2 instance using the AWS Console!
