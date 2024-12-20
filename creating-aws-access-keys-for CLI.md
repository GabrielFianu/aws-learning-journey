# AWS Access Key Setup for CLI Usage

This guide describes how to create and configure AWS access keys for CLI or SDK usage.

## Steps to Create Access Keys
1. **Log in to AWS**: Visit [AWS Console](https://aws.amazon.com/console/).
2. **Navigate to IAM**: Search for **IAM** and select it.
3. **Access User Settings**:
   - Select an existing user or create a new one.
   - Go to **Security credentials** > **Access keys**.
4. **Create and Save Keys**:
   - Click **Create access key**.
   - Choose **Command Line Interface** (CLI) from **Access key best practices & alternatives**
   - Check the cormfirmation box and choose **Next**.
   - Copy the **Access Key ID** and **Secret Access Key** securely or download .csv file and click **Done**.

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
