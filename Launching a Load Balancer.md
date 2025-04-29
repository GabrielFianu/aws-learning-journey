# Launching a Load Balancer

## Introduction

## Steps in launching a Load Balancer

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Launch two instances. 
1. Launch two instances. Remember to use security group that allowed us to do HTTP traffic and SSH traffic into our EC2 instance.
For EC2 user data, copy and paste following below:

#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html

Wait for these instances to be ready.

2. Copy the first IPv4 address and paste it in a new tab on your browser and note the response. 
3. Copy the second IPv4 address and paste it in a new tab on your browser and note the response. 
So as you can see, two instances give us the same response with different IP addresses.
![Image](https://github.com/user-attachments/assets/18601cc7-f61b-4d54-ac98-d812cc22fee7)
![Image](https://github.com/user-attachments/assets/3913a300-e6eb-4e37-8ed4-02be7176abe7)

---


### 3. Create Application load balancer.
1. In the left pane, scroll down and choose Load balancer
![Image](https://github.com/user-attachments/assets/a5ae99eb-f603-4d89-9237-7966bfad86be)
2. Click Create load application
![Image](https://github.com/user-attachments/assets/fff1bfa4-c297-4eaf-b594-3524009a8097)
2. Choose create under application load balancer.
![Image](https://github.com/user-attachments/assets/d4bccde9-a7f3-409a-a936-e06ba896790d)
3. Give the name 
![Image](https://github.com/user-attachments/assets/a21d7a73-4dc9-4108-b123-ed59cfccf53b)
4. Choose internet facing, IPv4 and choose all availability zones.
![Image](https://github.com/user-attachments/assets/f859824e-6c60-4561-a950-2f96ed96b431)
5. create a new security group for it to only allow HTTP traffic from anywhere.
6. Go back to your ALB and remove the default security group
![Image](https://github.com/user-attachments/assets/fce62974-0e36-4e82-a72a-8deb700cfab8)
7. Scroll down to listeners and routing, make sure traffic is routed through HTTP on port 80 to a target group.
![Image](https://github.com/user-attachments/assets/3e33de57-ae76-445c-875d-4879d459cf23)
---

### 3. Create Target Group.
1. click on create Target Group
![Image](https://github.com/user-attachments/assets/d9177301-8586-4eeb-9f0a-24ca306d55cc)
2. Enter the Target Group Name and for the protocol keep HTTP on Port 80.
![Image](https://github.com/user-attachments/assets/82498d80-02c9-449c-abf6-f2a4f3a27a96)
3. For IP Address Type, maintain IPv4 
4. Click Next
5. Next, register our target which is the two EC2 instances on port 80
6. Click on Create target group
![Image](https://github.com/user-attachments/assets/252ead1e-99ee-4e92-849b-fa5c34b8f2c1)
7. So this target group is created and it's linked to the listener on my load balancer on port 80.
![Image](https://github.com/user-attachments/assets/c262d1d8-f5d4-4525-95f5-55951e464443)

---


### 4. Verify if the Load Balancer is working.
1. Go to you ALB console and wait or refresh till it is provisioned.
2. Copy the DNS name and paste it in a new tab and through the application load balancer I'm able to get a response-hello world.
3. Keep refreshing the page and you will notice that the Target Group keep changing. Note the IP address anytime you refresh. 
That's because my application load balancer is actually redirecting between both my EC2 instances.
and that's the proof that load balancing is actually happening.
4. Stop one of the the instance and refresh the page and notice the outcome as compared to the previous.

---

### 5. Access EC2 Instances through Load Balancer Only.
From our previous exercise on Load Balancer, we can deduce that we can access our EC2 Instances directly using their Public IP address and through the load Balancer.
In this exercise, we are going access our EC2 Instances through the load balancer only.
1. Go to the security Group of your EC2 Instances and  choose edit the Inbound rules
2. Delete the exist rule and click on add new rule
3. Choose HTTP and for the CIDR block, choose the security group of the Load Balancer
4. Refresh the page where you pasted the Public IP address of your EC2 Instance, and you will note that it's timing out
5. But our ALB can still access our EC2 Instances. Refresh the load balancer page for a proof.
This has further tighten the security of our EC2 Intances.
