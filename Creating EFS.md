# Create an Elastic File System

## Introduction
Amazon Elastic File System (EFS) provides scalable and shared file storage for EC2 instances, enabling flexible data access and collaboration. In this post, we'll walk through the steps to set up and utilize EFS, ensuring seamless data sharing and storage for your applications.

---

## Steps in creating an Elastic File System

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Create an Elastic File System (option One)
1. Search for Elastic File System and choose EFS from the result.
![Image](https://github.com/user-attachments/assets/b579b382-b511-4967-87b0-fcbf70e433a6)
2. Click Create File System
![Image](https://github.com/user-attachments/assets/b7200af2-e470-4c91-b106-52dc06b6a708)
3. Leave default settings for optional name and vpc
4. click on create file system and that is it.
![Image](https://github.com/user-attachments/assets/60714448-d455-4265-8dce-c252f73efb48)


---

### 3. Create an Elastic File System (option Two)
Note: For this method, create a security group before you start with the process.
1. Search for Elastic File System and choose EFS from the result.
![Image](https://github.com/user-attachments/assets/b579b382-b511-4967-87b0-fcbf70e433a6)
2. Click on Create File System and then choose Customize
![Image](https://github.com/user-attachments/assets/b7200af2-e470-4c91-b106-52dc06b6a708)
![Image](https://github.com/user-attachments/assets/53228848-48e5-410a-8d69-1f4373c10989)
3. Leave default settings for optional name
4. Choose a file system type. For the this exercise, choose Regional.
5. For enable or disabled automatic backups, choose the recommended- keep it enabled.
6. For lifecycle management, encryption, performance settings and addtional settings, keep the recommended settings.
7. Click on Next for the network access settings
8. Choose the default VPC  for VPC and then the mount targets.
![Image](https://github.com/user-attachments/assets/c9fe610e-df29-4480-aa7f-5f4245808d63)
9. For subnets, maintain the default subnets.
10. Replace the security groups with the one you created earlier by deleting the default Security Group.
11. Click on Next.
12. Leave file system policy which is optional
13. Click on Next.
14. Review all the file system settings.
15. Click on Create.

---


### 4. Attaching Elastic File system onto EC2 instances
1. On the left pane, choose Instances and click launch Instances. 
2. For this exercise, choose Amazon Linux version 2, t2.micro and proceed without keypair.
3. For network settings, click edit and in subnet choose an AZ. Configure security group to allow SSH traffic from anywhere or use an existing Security Group such as Launch-wizard-2
4. Click add Shared EFS file system
![Image](https://github.com/user-attachments/assets/cfd5bb70-7ac5-46bb-9a09-2b4e293df825)
5. Take note of  /mnt/efs/fs1. 
6. Choose one for the number of instances and launch it.
7. Click view all instances
8. Using the same process launch a new one in another AZ.
9. Refresh until both instances are running.
10. Connect to one of Instances using EC2 instance Connect
11. Connect to the other Instance using EC2 instance Connect
12. In the first terminal enter ls /mnt/efs/fs1/ to verify the existence of an EFS file system.
13. Write a file in EFS by typing sudo SU 
14. Type echo "hello world!" > /mnt/efs/fs1/hello.txt. to craete a file named hello.txt
15. Enter ls /mnt/efs/fs1/ to verify the file you just created. The result should be, hello.txt
16. Enter cat /mnt/efs/fs1/hello.txt and the result should be hello world!.
![Image](https://github.com/user-attachments/assets/32163fed-2b4f-4a27-9bf0-bd34d77fd5b4)
17. In the second terminal, type ls /mnt/efs/fs1/ and the result should be hello.txt
18. Enter cat /mnt/efs/fs1/hello.txt and the result should be Hello World!
![Image](https://github.com/user-attachments/assets/32163fed-2b4f-4a27-9bf0-bd34d77fd5b4)

---

### 5. Conclusion
From the above exercise, you can note, that the EFS file system is indeed mounted as a network drive onto both my EC2 instances
and they are in different AZs and they share it the same EFS.

Terminate these two EC2 instances and delete the EFS File System and extra security groups
 
