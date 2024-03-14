<b>Here is the steps to create an CI/CD using GitHub and AWS</b><br/>
<b>Follow th below steps to create images are attached below</b>

<b>Create an Repository in GitHub</b>
![image](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/566d0e79-c211-4364-b6a1-2c1eb265910e)
<br />
<b>Create IAM Roles</b>
![image](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/2c2d90cf-7e30-41d4-bb21-47e17dec9a75)
![image](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/c202afd7-0290-4598-ba30-5daf25c63f34)
<br />
<b>Create an EC2 Instance with IAM Role
![image](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/faaca3a4-8066-448a-adb9-d49ccad76db5)
<br />
<b>Add User data while creting EC2 Intance</b>
<b>User Data for Dependencies installations for AMAZON Linux 2:-</b>

#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install ruby<br />
sudo yum -y install wget<br />
cd /home/ec2-user<br />
wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install<br />
sudo chmod +x ./install<br />
sudo ./install auto<br />
sudo yum install -y python-pip<br />
sudo pip install awscli<br />
<br />
<b>Create Code Deploy Application</b>
![Screenshot 2024-03-14 113236](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/8defc7d6-b801-4576-b2fa-6710eebc44bd)
<b>Create an Deployment group</b>
![Screenshot 2024-03-14 113305](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/8aa00f92-dbed-429c-8895-ac5f6468fdb2)

<b>Create Deployment</b>
![Screenshot 2024-03-14 113330](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/24cb8729-3e6d-43bc-8b9f-7a98ed37d581)
<b>Create Code Pipeline</b>
![Screenshot 2024-03-14 113349](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/ced736e3-c27d-4db3-be33-72d30e983932)
![Screenshot 2024-03-14 113410](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/30fa019b-fd4c-4730-8157-03fdce24f8f2)
![Screenshot 2024-03-14 113418](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/0987fcab-e248-414c-a09d-fe4a28dd95f0)
<b>S3 Bucket will be created automatically while creating code deploy</b>
![Screenshot 2024-03-14 113456](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/214d69e3-e4c2-480d-9e62-b08b032e9f8b)
<b>Final output of the website from the github if you change anything in the git repo its autmoatically changed and deployed automatically</b><br />
<b>To check the page was running or not Copy the EC2 Instance IP and paste it on new tab</b>
![Screenshot 2024-03-14 113542](https://github.com/suryaprakash-r/AWS-CICD/assets/129744688/7e73ae8d-eab9-4cf3-97c7-b26f322f701f)
