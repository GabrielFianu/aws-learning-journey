# Create and Attach EBS volumes to an Instance.

## Introduction
In this post, we'll walk through the steps to create and attach EBS volumes to EC2 instances, ensuring efficient data management and storage.
---

## Steps involved in ctreating and attaching EBS Volume to an Instance

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Check default EBS Volume attached to your Instance
1. Click on instance
![Image](https://github.com/user-attachments/assets/2d1bd528-ac93-4ed1-b6c8-11b79f628a8d)
2. Choose storage tab and on it you find one volume of eight gigabytes currently attached to your EC2 instance.
3. Click on this volume and it will take me into the interface of the volume.This interface provides details about the attached volume. Take time to go through it. 

---

### 3. Create another Volume
1. click on volumes at the left pane.
![Image](https://github.com/user-attachments/assets/91f97524-76e1-44fd-bb02-04e916d48f88)
2. Choose create a volume.
![Image](https://github.com/user-attachments/assets/72380190-45de-4361-b61a-9bed55d28bf4)
3. From the volume type, you have options to choose from. For the purpose of this exercise, choose GP2 and a volume size of 2 GiB 
![Image](https://github.com/user-attachments/assets/424e5ede-b980-49e3-97aa-2fbdf658905e)
![Image](https://github.com/user-attachments/assets/b6ce16d1-eb1e-48de-8371-a3d2a8f57b70)
4. For availability zone, choose the same zone where your EC2 instance is. To find which availability zone your instance is, choose the instance and click on networking.
Scroll down, and you will find the availability zone.
![Image](https://github.com/user-attachments/assets/2c6c149d-7c45-4b09-9280-a3ce833caece)
5. Click on create volume.
![Image](https://github.com/user-attachments/assets/cb66244c-3046-4459-aa19-82d6e60f3bed)
![Image](https://github.com/user-attachments/assets/14160844-9e16-4b33-9515-70129a111dc2)
6. Refresh for your new volume to appear. Click on the new volume fo details and note that it is available, but not attached.
![Image](https://github.com/user-attachments/assets/57711887-5c95-4ca4-8d8a-89d32e7a5ae1)
[Image](https://github.com/user-attachments/assets/8202224c-e49b-44f6-80c7-b5d34a03dcd8)
![Image](https://github.com/user-attachments/assets/5d99dec8-f3c3-4e44-afb6-e37b7d472ef8)

---

### 4. Attach Volume to an Instance
1. Select the volume you want to attach.
![Image](https://github.com/user-attachments/assets/95844ce8-a43f-42b8-9f88-1e3bd3fb466b)
2. Click on Action
3. Choose attach volume
![Image](https://github.com/user-attachments/assets/26adc926-67dc-4265-aabc-ce4b4a252b6c)
4. Choose the Instance you want to attach it to.
5. Click Attach Volume and the voulme is attached to our instance.
![Image](https://github.com/user-attachments/assets/35310f0f-1229-4710-8a62-c82e3ac02d18)
![Image](https://github.com/user-attachments/assets/f337c0bc-a00d-4393-b56d-c3aacca2a7d9)
![Image](https://github.com/user-attachments/assets/f3a2fa36-a0f0-43e4-b62d-e02fb425bc7a)
6. To confirm that our new volume is attached to the instance, go to storage tab on my EC2 console and scroll down. There you will find
two block devices.

---

### 5. Delete Attached Volume
1. Select the volume
2. Go to action and choose detach volume and follow the prompt to detach the volume
3. select the volume again, go to action and choose delete volume.
4. Follow the prompt to delete it.
Note: the first volume which is default storage has delete on termination attribute so once the instance is terminated, the volume is deleted.

---
