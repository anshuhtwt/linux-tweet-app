**SETUP OVERVIEW**
* First we need to create a VPC on AWS
* Install Kubernetes Cluster inside VPC
<img width="1024" alt="Screenshot 2023-04-17 at 10 12 35 AM" src="https://user-images.githubusercontent.com/95365748/232380118-2e8388a2-bf20-4135-8c48-e1bf03559cf2.png">


* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

**INSTALLATION PART** <br>
<br> 1)Launch an ec2 instance for running Jenkins and add port 8080 in security group of the instance to access Jenkins. <br>
<br> 2)Connect to instance and install Jenkins, Kubectl, AWS-CLI, Git and Docker. <br>
<br> 3)Install these plugins
- Docker
- Docker Pipeline
- Kubernetes
- Kuberneets Credentials
- Kubernetes CLI

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

**CONFIGURATION PART** <br>
<br> 1)Add jenkins as user to docker group so that jenkins can run docker command for building image and pushing it to docker hub. <br>
<br> 2)Add jenkins user to sudoers file so that password is not asked while performing some tasks by jenkins user. <br>
<br> 3)To switch to jenkins user make some changes inside /etc/passwd file and copy env-variables files into present home directory of user. <br>
<br> 4)Switch to jenkins user <br>
<br> 5)Configure AWS. <br>
<br> 6)Intergrate Kubernetes with Jenkins using kube-config file. <br>
<br> 7)Add docker hub credentials. <br>
<br> <img width="1436" alt="Screenshot 2023-04-17 at 11 35 31 AM" src="https://user-images.githubusercontent.com/95365748/232397693-8c64d246-03f6-4b7f-8ac6-7c56595fa15a.png"> <br>

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

**PIPELINE SETUP**
<br> 1)Create a new job and select Multibranch Pipeline. <br>
<br> <img width="1438" alt="Screenshot 2023-04-17 at 11 40 12 AM" src="https://user-images.githubusercontent.com/95365748/232398828-07c999eb-f818-44fa-89d3-852080530534.png"> <br>







