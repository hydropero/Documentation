- ### [Return to main index page](https://github.com/hydropero/Terminology)
- ### [Return to main documentation page](https://github.com/hydropero/Documentation/blob/main/Documentation_Tutorials.md)

# How to SSH into your EC2 Instance created via (AWS Canvas Lab 1 Sandbox)

1. Follow this link [AWS Console](https://labs.vocareum.com/main/main.php?m=clabide&mode=s&asnid=1458055&stepid=1458056&hideNavBar=1) to provision your AWS account or start the lab from Canvas `1-[CF]-Lab - Sandbox Environment`
<br>

2. Click `Start Lab` to begin the lab, then select the `AWS Details` menu once the left-most light turn green. A Credentials window will be presented, titled **Cloud Access**
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%205.49.51%20PM.png?raw=true">
<br>

3. Select the `Download PEM` button and save the labsuser.pem file.
<img src="https://raw.githubusercontent.com/hydropero/Documentation/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%205.59.40%20PM.png">
<br>

4. Open your terminal and navigate to where to you saved the labsuser.pem file. Example below, use the<code>ls</code> command to verify the file exists in your directory
<img src="https://raw.githubusercontent.com/hydropero/Documentation/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-21-12.png">
<br>

5. Change the name of the labsuser.pem file to vockey.pem using the following command as shown  <code>mv labsuser.pem vockey.pem</code>
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-24-23.png?raw=true">
<br>

6. Create your EC2 Instance and be sure to select to use the existing key pair called **vockey**, then finish provisioning the instance.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%206.03.45%20PM.png?raw=true">
<br>

7. Navigate into your EC2 instance within AWS
<br>

8. Enter into your instance, select it using the checkbox on the left and then copy the Public IP Address, we will use it later.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/Screen%20Shot%202023-02-04%20at%206.29.15%20PM.png?raw=true">
<br>

9. Back in your terminal - change the permissions on the vockey.pem key to be read-only, by running this command:
<code>chmod 400 vockey.pem</code>
<br>

10. Run the below command (replace `<public-ip>` with the PublicIP address you copied earlier).
Alternatively, return to the EC2 Console and select Instances. Check the box next to the instance you want to connect to and in the Description tab copy the IPv4 Public IP value.:
<br>

11. <code>ssh ec2-user@54.149.188.49 -i vockey.pem</code>
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-39-39.png?raw=true">
<br>

12. When prompted regarding the server's fingerprint, enter yes.
<img src="https://github.com/hydropero/Documentation/blob/main/Screenshots/AWS_SSH/AzureWebHosting_2023-02-04_18-39-55.png?raw=true">
<br>

13. Celebrate, because congrats you've successfully SSH'd into your remote AWS EC2 Instance
