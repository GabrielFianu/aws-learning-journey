# How to Launch an EC2 Instance in AWS

## Introduction
Amazon Elastic Compute Cloud (EC2) provides scalable virtual servers in the cloud. This guide walks you through the steps to launch an EC2 instance.

---

## Steps to Launch an EC2 Instance

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Open the EC2 Dashboard
1. Search for **EC2** in the AWS search bar.
2. Click on **EC2** to access the EC2 dashboard.

---

### 3. Launch an Instance
1. On the EC2 dashboard, click **Launch Instance**.
![launch1 jpeg](https://github.com/user-attachments/assets/6c7da83a-575e-4941-94c3-f9d3f67d9b60)
2. Provide a name for your instance in the **Name and Tags** section (e.g., `MyFirstInstance`).

---

### 4. Choose an Amazon Machine Image (AMI)
1. Select an AMI, which is a template for your instance:
   - Use the default **Amazon Linux 2 AMI (Free Tier eligible)** for testing purposes.
   - You can also choose other AMIs based on your requirements.
![ami-first jpeg](https://github.com/user-attachments/assets/352eb810-eaf1-437b-a530-926482883c6d)
![choose amazon linux 2 jpeg](https://github.com/user-attachments/assets/adfcca02-6ca4-4120-985a-fbc5ff2af82a)

---

### 5. Choose an Instance Type
1. Select an instance type based on your needs:
   - For Free Tier, choose **t2.micro**.
   ![choose t2 micro jpeg](https://github.com/user-attachments/assets/5438b102-822c-4993-bb93-d2a802f1e1b9)

---

### 6. Create a **key pair (log in)** to securely connect to your instance.
1. Under **key pair (log in)**, enter your key pair name and choose **create new key pair**.
[key pair name jpeg](https://github.com/user-attachments/assets/995c1d2b-9e4a-43cc-b5cb-ef97bf9c3c52)
2. Check the **RSA** under **key pair type** and **.pem** under **Private key file format**.
![RSA-jpeg](https://github.com/user-attachments/assets/0b4c30e8-4d70-4fa1-9114-115f1ba3c75b)
3. Choose  **create key pair**. The key pair is downloaded for you.


### 7. Network settings
1. For Firewall (security groups), choose **Create security group**.
2. Check **Allow SSH traffic from** and choose **Anywhere** box.
3. Check **Allow HTTP traffic from the internet** box.
![network settings jpeg](https://github.com/user-attachments/assets/5be6ac23-1f8c-4398-8cf5-0c0085370cea)


### 8. Configure Storage
1. Maintain the default (default is 8 GiB gp2 for Free Tier).
![configure storage-jpeg](https://github.com/user-attachments/assets/6f93082d-50c4-433b-ae7e-ea3a86a24674)
2. Use **Add new volume** to new volume to you new instance..


### 9. Advanced details
1. Leave all settings as default for a simple setup.
2. For **User data - optional**, copy and upload the code below.
![user data-jpeg](https://github.com/user-attachments/assets/0bd9352b-0476-41e9-8cf5-70156eaa6aea)


### 10. Summary
1. Maintain the number of instances at 1.
![summary jpeg](https://github.com/user-attachments/assets/db9d5c25-0ca3-4b75-8ac1-d3d27ce967b5)
2. Review your settings.
3. Click **Launch instance**.
![launch instance final-jpeg](https://github.com/user-attachments/assets/bc3cbf15-c55a-4f5b-a5ed-de2144e23566)
![launched-jpeg](https://github.com/user-attachments/assets/39726d0f-f1e0-4174-b5a3-f09380a83e6c)


### 11. Verify the Instance
1. Return to the EC2 dashboard and click **Instances** in the left-hand menu.
2. Check the status of your instance. Once it shows **Running**, your EC2 instance is ready for use.

### 12. Verify the Uploaded user data
1. Select the instance you have just created.
2. Under the **Details** tab, copy **Public IPv4 address**.
3. Paste **Public IPv4 address** in the Address Bar of your browser and press the Enter key.
4. If you have a similar screen as indicated below, then you have successfully launch an instance with a user data.
![user data results jpeg](https://github.com/user-attachments/assets/f30a7a3c-19d7-45fe-ada1-26eeb628ea1c)
5. Note: use http// protocol before the copied address incase you couldn't get similar results.


### 13. EC2 Instance State
1. Click on the Instance state to Stop, Start, Reboot, Hibernate and Terminate your instances.
![instance state-jpeg](https://github.com/user-attachments/assets/d90f6aa9-c8be-461e-a309-a7a6e6725317)
