# Taking a Snapshots of a Volume

## Introduction
In this post, we'll walk through the steps to create snapshots of EBS volumes, ensuring your data is securely backed up and easily recoverable.

---

## Steps involved in taking a snapshot of a volume

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Create a snapshot
1. Select the volume
2. Go to Actions and choose create a snapshot
![Image](https://github.com/user-attachments/assets/a3959def-1138-4192-95b8-eae3dbe87a70)
4. Add Description and then click on Create snapshots.
![Image](https://github.com/user-attachments/assets/591ec62b-f2a0-4df8-8d4b-6335a80e2428)
![Image](https://github.com/user-attachments/assets/8d2f74e8-8721-4f54-bcf2-dbf356d7b6b6)
5. So then on the left pane, click on Snapshots and it shows you a list of all the snapshots you have created.
6. Wait for the snapshot to be available before further actions on it.

---

### 3. Copy Snapshot into other regions
1. Right click and choose Copy Snapshots
![Image](https://github.com/user-attachments/assets/c1052232-dde5-441c-82af-04b4af2e3c57)
2. Follow the prompts to copy to another region
![Image](https://github.com/user-attachments/assets/d6441c14-7143-46cf-b822-63884c609af0)

---

### 4. Create a volume from snapshot
1. Select the snapshot
![Image](https://github.com/user-attachments/assets/1d7dd792-f43a-4d5e-a708-e9a787ca89f9)
2. Click on Action and choose Create volume from snapshot.
![Image](https://github.com/user-attachments/assets/3b1d3118-f63d-48d8-b71b-37dcd05d7227)
3. Choose the volume type And AZ 
4. You can encrypt and add some Tags to the volume if you want to.
5. Click on Create volume
![Image](https://github.com/user-attachments/assets/62a46660-de08-492d-84a7-b42cf1de20ff)
6. Click on Volume in the left pane and now you can see two volumes there.

---

### 5. Using Recycle Bin to Protect your EBS Volume from accidental deletion
1. Click on Recycle Bin.
![Image](https://github.com/user-attachments/assets/de225585-e109-495c-abe7-0b0d9bb1ee6d)
2. Choose Create a Retention Rule and name it
![Image](https://github.com/user-attachments/assets/d1c93ca6-9e35-4ec5-8227-e22f9d49ee62)
![Image](https://github.com/user-attachments/assets/2905847b-3009-48b4-8a74-5985cf2ec371)
3. Select EBS Snapshots for resource type.
4. Choose Retain all resources and retain them for one day.
![Image](https://github.com/user-attachments/assets/17a432c8-00fa-4b8f-a398-157f430f951f)
![Image](https://github.com/user-attachments/assets/ce790c04-233b-4f99-89f6-ae7b547c06d9)
5. Leave at unlocked for Rule Lock Setting.
![Image](https://github.com/user-attachments/assets/9f4dab4a-7023-481c-8db8-1baeb4158f49)
6. Click on Create Retention Rule.
![Image](https://github.com/user-attachments/assets/a3dbd085-2097-4b7e-ab5b-8cacb035eafe)

---

### 6. Restoring deleted snapshots using Recycle Bin.
1. Click on resources to see if you have any resources there
![Image](https://github.com/user-attachments/assets/913b9aa6-8013-47bb-8ce6-459a64794888)
2. So let's go back into your Snapshot in the EC2 Console and delete it.
![Image](https://github.com/user-attachments/assets/26dd70eb-3e3b-456f-8197-79dc2cd0d5cb)
3. Go back and refresh your Resources and the deleted snapshot appears here
![Image](https://github.com/user-attachments/assets/4023d226-db9a-45e5-a474-e9e4fb9f81f1)
4. Click on Recover and the deleted snapshot is back to Snapshots on your EC2 console. 
![Image](https://github.com/user-attachments/assets/c178946d-3520-4876-9b08-55c8e1b2bd32)

