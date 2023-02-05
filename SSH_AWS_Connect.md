# How to SSH into your EC2 Instance created via (AWS Canvas Lab)

1. Select the AWS Details drop-down menu. A Credentials window will be presented.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%205.49.51%20PM.png?raw=true">
<br>
2. Select the Download PEM button and save the labsuser.pem file.
<img src="https://raw.githubusercontent.com/hydropero/Documentation/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%205.59.40%20PM.png">
<br>
3. Navigate in your terminal to where to you saved the labsuser.pem file. Example below.
<img src="https://raw.githubusercontent.com/hydropero/Documentation/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-21-12.png">
<br>

4. <code>mv labsuser.pem vockey.pem</code>
Change the name of the labsuser.pem file to vockey.pem
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-24-23.png?raw=true">
<br>

5. Create your EC2 Instance and be sure to select to use the existing key pair called **vockey**, then finish provisioning the instance.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%206.03.45%20PM.png?raw=true">
<br>

6. Navigate into your EC2 instance from AWS
<br>

7. Enter into your instance, select it using the checkbox on the left and then copy the Public IP Address, we will use it later.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%206.29.15%20PM.png?raw=true">
<br>

10. Back in your terminal - change the permissions on the vockey.pem key to be read-only, by running this command:
<code>chmod 400 labsuser.pem</code>
<br>

11. Run the below command (replace <public-ip> with the PublicIP address you copied earlier).
Alternatively, return to the EC2 Console and select Instances. Check the box next to the instance you want to connect to and in the Description tab copy the IPv4 Public IP value.:
<br>

12. <code>ssh ec2-user@54.149.188.49 -i labsuser.pem</code>
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-39-39.png?raw=true">
<br>

13. When prompted regarding the server's fingerprint, enter yes.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-39-55.png?raw=true">
<br>

14. Celebrate, because congrats you've successfully SSH'd into your remote AWS EC2 Instance
