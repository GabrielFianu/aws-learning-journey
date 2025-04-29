# Create an AMI and launch an Instance from it

## Introduction
 In this post, we'll walk through the steps to create an AMI and launch an instance from it, ensuring efficient and consistent deployment of your applications.

---

## Steps in creating an AMI and Launching an Instance from it

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Launch an EC2 Instance
1. Follow the steps iin earlier posts to launch EC2 Instance.
2. In user data, copy and paste the following below to install HTTPD
which is an Apache web server:

#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd

![Image](https://github.com/user-attachments/assets/336deece-615f-4955-b229-76621d5260ff)
![Image](https://github.com/user-attachments/assets/619614f8-ec72-449d-bbf0-988b498d25a9)

3. Click Launch instance and wait for the Instance to be in running state.
4. Copy and paste public IPV4 and paste in a new tab on your browser, my test page appears.
![Image](https://github.com/user-attachments/assets/e87811b5-b834-475f-af0e-2315996acb0e)

---

### 3. Create an AMI 
1. Right click the Instance and choose image and templates
2. Create Image.
3. Enter the name in the image Name
![Image](https://github.com/user-attachments/assets/8e31c919-a1ad-4eb5-8663-1cc70bb96ffc) 
4. Choose create owm AMI
5. Click on create image.
![Image](https://github.com/user-attachments/assets/b5ff83d9-6ea1-456e-b90d-56c6e452946d)
6. Confirm by clicking AMI at the left pane. See if your AMI is registered there.
7. Wait for it go into created state.

---

### 4. launch instances from AMI created.
1. On instance creation page, choose 'my AMI's tab'
![Image](https://github.com/user-attachments/assets/cdd3b504-2a80-4ee5-b774-0a5a18ff5e0e)
2. Select owned by me
![Image](https://github.com/user-attachments/assets/99d72a16-4b9e-4b28-a433-29b983952ab2)
3. Choose the AMI created by yourself
![Image](https://github.com/user-attachments/assets/03736726-288a-4a95-81dd-af83c9d1b008)
4. Do your own settings for Keypair and network
5. In the advanced, copy and paste data below for user data

#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html

![Image](https://github.com/user-attachments/assets/61eeff3d-edec-4baa-84de-3736e6773660)
6. Click on launch an instance and wait for it to be fully created.
7. When your instance is running, copy and paste the public IP address on a new tab on your browser.
8. Your Response should be like the image below.
![Image](https://github.com/user-attachments/assets/3f9ed9ce-eca6-4148-a19a-c98eb367d8fc)

