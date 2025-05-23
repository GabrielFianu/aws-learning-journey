## Steps to attach IAM roles to an EC2 Instance

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Use EC2 Instant Connect to connect to your Instance
1. Using EC2 Instant Connect, ssh into your instance.
2. Run the command, aws iam list users.
And from the response, you are unable to look at credentials. You can configure credentials by using aws configure. Run aws configure to configure the credentials. You are requested to specify an Access ID, a Secret Access key, and a region name.
But this is not recommended, and the reason is that if we run aws configure and enter our personal details onto this EC2 Instance,
then anyone else in our accounts could again connect to our EC2 Instance. And using EC2 Instance Connect anyone retrieve the value of these credentials in our instance,
which is not what we want.

---

### 2. Alternatively method 
1. Go to  management console and create an IAM role. Attach the policy called IAMReadOnlyAccess. We are going to attach this role onto our EC2 Instance to provide it with credentials.
2. Go to Security tab and note, there is no IAM Role attached to your instance.
![Image](https://github.com/user-attachments/assets/022f07fe-0fff-4279-9b9a-6b0ddce4c77d)
3. Click Action, choose Security, and then Modify IAM role.
4. Choose the IAM role you just created.
![Image](https://github.com/user-attachments/assets/5bec3e86-2d2e-4abd-830f-6aa1afa18878)
4. Click on Update IAM role to attach this IAM role into our Instance.
![Image](https://github.com/user-attachments/assets/f2c06e93-7fd1-462c-b034-0d32efad7581)
![Image](https://github.com/user-attachments/assets/34ee3be7-a923-4aac-8ed7-c6c7c6a34935)
5. So if you go back to Security tab, now the IAM role attached to Instance.
![Image](https://github.com/user-attachments/assets/edb9f947-60d5-4660-8d72-29aa773c591d)
7. Go back to your terminal and issue the command, aws iam list users and press Enter.
![Image](https://github.com/user-attachments/assets/bbaf9704-7427-4576-b1d5-ea617383a1b8)
8. Note the response on IAM.
