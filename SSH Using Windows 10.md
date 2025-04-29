# How to SSH using Windows 10

## Introduction
In this post, we will walk through the steps to set up and use SSH on Windows 10, enabling secure connections and efficient remote work.

---


## Steps to SSH using Windows 10

### 1. Log in to AWS Management Console
1. Navigate to the [AWS Management Console](https://aws.amazon.com/console/).
2. Log in with your credentials.

---

### 2. Launch Windows PowerShell
1. Type SSH and press enter key and if you see this,
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Try the new cross-platform PowerShell https://aka.ms/pscore6

PS C:\Users\USER> ssh
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface] [-b bind_address]
           [-c cipher_spec] [-D [bind_address:]port] [-E log_file]
           [-e escape_char] [-F configfile] [-I pkcs11] [-i identity_file]
           [-J destination] [-L address] [-l login_name] [-m mac_spec]
           [-O ctl_cmd] [-o option] [-P tag] [-p port] [-Q query_option]
           [-R address] [-S ctl_path] [-W host:port] [-w local_tun[:remote_tun]]
           destination [command [argument ...]]
PS C:\Users\USER>

that means that it's available. Otherwise, you can also use the command prompt and do SSH.

If you don't see the SSH command on your Windows, that means that you don't have it and therefore,
you must use the patching method using  PuTTY. For this exercise, we are going to use PowerShell.

---


### 3. Run SSH command.
1. So the first thing I have to do is to be in the directory of where my pem file is.For example, if .pem file is on the desktop, change the directory to desktop. 
In this case, issue the command, cd.\Desktop.
2. Enter ls and your .pem file you downloaded is right there.
Note: make sure that on the security group of tab you have the port 22 open for SSH.
3. Enter ssh -i [name of .pem file] [ec2-user]@[public ip of my EC2 Instance]
4. Press enter.
And it says, well, the authenticity of the host cannot be trusted, do you want to continue?
5. Type and enter yes and we are in the machine.
6. Your expected output should look like: 

,     #_
   ~\_  ####_        Amazon Linux 2
  ~~  \_#####\
  ~~     \###|       AL2 End of Life is 2025-06-30.
  ~~       \#/ ___
   ~~       V~' '->
    ~~~         /    A newer version of Amazon Linux is available!
      ~~._.   _/
         _/ _/       Amazon Linux 2023, GA and supported until 2028-03-15.
       _/m/'           https://aws.amazon.com/linux/amazon-linux-2023/

53 package(s) needed for security, out of 61 available
Run "sudo yum update" to apply all updates.

6. To exit, type exit or do Control + D
