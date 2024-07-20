### AWS DevOps CodePipeline Guide

This guide will help you set up AWS CodePipeline with CodeCommit, including creating a repository, setting up IAM roles, and cloning the repository locally.

#### Stage 1: CodeCommit Repository Setup

##### Step 1: Create the CodeCommit Repository

1. **Log in to the AWS Management Console**.
2. **Navigate to the CodeCommit service**.
3. **Create a new repository**:
   - Click on **"Create repository"**.
   - Enter a **repository name** and an **optional description**.
   - Click on **"Create"**.

##### Step 2: Create the IAM User Role for CodeCommit

1. **Navigate to the IAM service**.
2. **Create a new user** or select an existing user who will interact with CodeCommit.
3. **Attach the `AWSCodeCommitPowerUser` policy**:
   - Go to the **Permissions** tab of the user.
   - Click on **"Add permissions"**.
   - Choose **"Attach policies directly"**.
   - Search for **`AWSCodeCommitPowerUser`**.
   - Select the policy and click **"Next: Review"**.
   - Click on **"Add permissions"** to finalize.

##### Step 3: Clone Your CodeCommit Repository Locally

1. **Ensure AWS CLI is configured**:
   - Run the following command in your terminal:
     ```bash
     aws configure
     ```
   - Enter your **AWS Access Key ID**, **AWS Secret Access Key**, **Default region name**, and **Default output format**.

2. **Clone the repository**:
   - Obtain the HTTPS URL of your CodeCommit repository from the AWS Management Console.
   - Run the following command in your terminal:
     ```bash
     git clone <repository-url>
     ```
   - Replace `<repository-url>` with the actual URL of your CodeCommit repository.

