# How to SSH into your EC2 Instance created via (AWS Canvas Lab)

1. Select the AWS Details drop-down menu. A Credentials window will be presented.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%205.49.51%20PM.png?raw=true">
<br>
2. Select the Download PEM button and save the labsuser.pem file.
<img src="https://raw.githubusercontent.com/hydropero/Documentation/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%205.59.40%20PM.png">
<br>
3. Navigate in your terminal to where to you saved the labsuser.pem file. Example below.

<br>
4. <code>mv labsuser.pem vockey.pem</code>
Change the name of the labsuser.pem file to vockey.pem

<br>
5. Navigate into your EC2 instance from AWS

6. Create your EC2 Instance and be sure to select to use the existing key pair called **vockey**, then finish provisioning the instance.
<image>

7. Enter into your instance, select it using the checkbox on the left and then copy the Public IP Address, we will use it later.

<br>

8. Then exit the Details panel by selecting the X.
<br>

9. Open a terminal window, and change directory cd to the directory where the labsuser.pem file was downloaded. For example, if the labuser.pem file was saved to your Downloads directory, run this command:
<br>

10. <code>cd ~/Downloads</code>
Change the permissions on the key to be read-only, by running this command:
<br>

11. <code>chmod 400 labsuser.pem</code>
Run the below command (replace <public-ip> with the PublicIP address you copied earlier).
Alternatively, return to the EC2 Console and select Instances. Check the box next to the instance you want to connect to and in the Description tab copy the IPv4 Public IP value.:
<br>

12. <code>ssh -i labsuser.pem ec2-user@<public-ip></code>
Type yes when prompted to allow the first connection to this remote SSH server.
Because you are using a key pair for authentication, you will not be prompted for a password.
