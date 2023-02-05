# How to SSH into your EC2 Instance created via (AWS Canvas Lab)

1. Select the Details drop-down menu above these instructions you are currently reading, and then select Show. A Credentials window will be presented.
<br>
2. Select the Download PEM button and save the labsuser.pem file.
<br>
3. Navigate in your terminal to where to you saved the labsuser.pem file
<br>
4. <code>mv labsuser.pem vockey.pem</code>
Change the name of the labsuser.pem file to vockey.pem
<br>
5. Navigate into your EC2 instance from AWS
<br>
6. Make a note of the PublicIP address.
<br>
4. Then exit the Details panel by selecting the X.
<br>
5. Open a terminal window, and change directory cd to the directory where the labsuser.pem file was downloaded. For example, if the labuser.pem file was saved to your Downloads directory, run this command:
<br>
6. <code>cd ~/Downloads</code>
Change the permissions on the key to be read-only, by running this command:
<br>
7. <code>chmod 400 labsuser.pem</code>
Run the below command (replace <public-ip> with the PublicIP address you copied earlier).
Alternatively, return to the EC2 Console and select Instances. Check the box next to the instance you want to connect to and in the Description tab copy the IPv4 Public IP value.:
<br>
8. <code>ssh -i labsuser.pem ec2-user@<public-ip></code>
Type yes when prompted to allow the first connection to this remote SSH server.
Because you are using a key pair for authentication, you will not be prompted for a password.
