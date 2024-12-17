# How to Avoid Charges When Using AWS Free Tier service

## Introduction
AWS Free Tier provides an excellent way to explore cloud services for free, but exceeding limits can lead to unexpected charges. Here’s a guide to help you avoid unnecessary costs.

## Steps to Avoid Charges

### 1. Understand Free Tier Limits
- AWS Free Tier has three types:
  - **Always Free**: Limits that do not expire (e.g., Lambda).
  - **12-Month Free**: Free for the first 12 months from your initial sign up activation date to AWS (e.g., EC2 t2 Micro).
  - **Trials**: Short-term free trials for specific services from the day you activate those services.(e.g., Amazon SageMaker and Redshift have two months of free trial whiles Amazon LightSail offers three months.
  - **Note**: You must stay within the usage limits established for the services under free tier.
 
### 2. Checking Usage Limits Services
  - Go to [AWS Console](https://aws.amazon.com)
  - Scroll to Console Overview and choose the arrow beside **Learn more about AWS Service**
  - Under **Free Tier Details**, search for each service you want. (e.g., EC2)
    ![Search ec2-png](https://github.com/user-attachments/assets/283e6fe8-2d31-4e5c-8507-a72d9f3bf061)
 
### 3. Check the Number of Hours you use in a given month
  - Go to [AWS Console](https://aws.amazon.com/console/).
  - Enter your **email** and **password** to log in.
    ![sign in page](https://github.com/user-attachments/assets/1dcf438b-956a-44f6-8b56-42bdb616b91f)
  - Choose your account name and choose **Billing and Cost management**.
    ![under account name-png](https://github.com/user-attachments/assets/efe9386e-bf4d-493b-b4b2-c8b4a4cdb740)
  - Check the cost summary
    ![Cost Summary-png](https://github.com/user-attachments/assets/1326c12d-881d-4a55-9a72-ee150a66c6d9)
  - In the left panel, choose **Free Tier** (this shows the service used, the usage limit and also how much you have already used the current month).
    ![choose free tier-png](https://github.com/user-attachments/assets/e06fe4f1-793a-4b68-b4a4-abe827c09b27)

### 4. Turn on AWS Free Tier Usage Alert  
  - Under **preferences** in the left pane, **choose billing preferences**.
    ![choose billing preferences-png](https://github.com/user-attachments/assets/1ec04ae5-d4e6-4865-8088-a7dda426f66f)
  - Beside Alert Preferences, select **Edit**.
  - Check **Receive AWS Free Tier Alert** box.
  - You can give an optional email.
     ![alert preferences-png](https://github.com/user-attachments/assets/443a5c5e-2bee-43ae-b255-05e2212f8be7)
  - Choose **Update**.
    ![aws-widget added-png](https://github.com/user-attachments/assets/2faf1dc7-dd4c-4fab-ae98-442afc2b58da)

### 5. Checking for Active Resources
  - In the navigation panel choose **Bills**.
    ![choose bills-png](https://github.com/user-attachments/assets/ab1916ef-200c-4424-8672-6154bdb34d8a)
  - Choose a month to see the services used in the month
   

 ### 6. Terminating Resources you no longer needed
   - Go to Console Home by choosing aws at upper left corner.
     ![aws button-png](https://github.com/user-attachments/assets/433eab58-043e-4004-8667-30e29c44f3ed)
   - Search for services that contain the resources and terminate them. make sure you select the region the service is located.
    ![search 4 ec2-png](https://github.com/user-attachments/assets/6bab1eb0-c1b7-4aa5-a079-d47e75a2b8bb)

## Summary
This guide can help you avoid unnecessary costs.
