# Setting Up AWS CLI on Windows

## Introduction
The AWS Command Line Interface (CLI) enables you to interact with AWS services through terminal commands. This guide provides step-by-step instructions to install AWS CLI on Windows.

---

## Prerequisites
- An AWS account. Sign up at [AWS Console](https://aws.amazon.com/console/) if you don't have one.
- Basic knowledge of terminal/command prompt usage.

---

## Steps to Set Up AWS CLI on Windows

### 1. Download the Installer
1. Go to (https://aws.amazon.com/cli/).
2. Click **Windows (64-bit)** under "AWS CLI Version 2".
![64 bits-png](https://github.com/user-attachments/assets/bb016d73-600c-47c6-8714-2516efecc3c9)

### 2. Install AWS CLI
1. Run the downloaded `.msi` file.
2. Follow the installer prompts:
   - Accept the license agreement.
   - Choose the installation location (default is recommended).

### 3. Verify Installation
1. Open the **Command Prompt** by searching for **cmd** on the search bar located beside the start menu (for Windows 10).
2. From the Search Results, choose **Command Prompt**.
3. Run the command **aws --version**

You should see an output similar to:
aws-cli/2.x.x Python/3.x.x Windows/10
