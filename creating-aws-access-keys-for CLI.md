# AWS Access Key Setup for CLI Usage

This guide describes how to create and configure AWS access keys for CLI or SDK usage.

## Steps to Create Access Keys
1. **Log in to AWS**: Visit [AWS Console](https://aws.amazon.com/console/).
2. **Navigate to IAM**: Search for **IAM** and select it.
   ![IAM-png](https://github.com/user-attachments/assets/a3855e98-5c9e-4af5-8e9b-1fbd128b0741)
3. **Access User Settings**:
   - Select an existing user or create a new one.
   - Go to **Security credentials** > **Access keys**.
   ![security-credentials-tab-png](https://github.com/user-attachments/assets/c99cffe2-6e30-4678-84ff-9b3acced3407)
4. **Create and Save Keys**:
   - Click **Create access key**.
   ![create access keys-png](https://github.com/user-attachments/assets/96639a65-ab9a-45e8-b9fd-c0cc71c0610b)
   - Choose **Command Line Interface** (CLI) from **Access key best practices & alternatives**
   ![choose-cli-png](https://github.com/user-attachments/assets/301e9d7c-1cf1-4de2-a825-c56bec2738a2)
   - Check the cormfirmation box and choose **Next**.
   ![confirmation-next-png](https://github.com/user-attachments/assets/4fcb215b-29ef-430b-a9f3-1e7cbd8dd26e)
   - Choose **Create access keys**
   ![real create access keys-png](https://github.com/user-attachments/assets/fed481f3-dc86-4f54-98b2-e8a3668a84d9)
   ![access key created](https://github.com/user-attachments/assets/2a46169e-d581-424a-875b-7d3f2cb388a7)
   - Copy the **Access Key ID** and **Secret Access Key** securely or download .csv file and click **Done**.
   ![Download-done-png](https://github.com/user-attachments/assets/ae73f4fe-b481-438a-aa72-1ab1502e6d63)

## Configure AWS CLI
1. Open a terminal or command prompt.
2. Run the following command:
   aws configure
3. Enter the required details:
   - AWS Access Key ID: Your key ID from the AWS Management Console.
   - AWS Secret Access Key: Your secret key from the AWS Management Console.
   - Default region name: (e.g., us-east-1).
   - Default output format: json (recommended).
4. Test Configuration
   - Run the following command to test your setup:
   - aws iam list-users
If configured correctly, you'll see a list of your of all IAM users in your account, along with their user names, User ID and other details (if any).
