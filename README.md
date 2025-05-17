 # SETTING UP A SCALABLE FILE STORAGE SYSTEM USING AMAZON ELASTIC FILE SYSTEM
  ## AIM
       To  setting up a scalable file storage system using Amazon Elastic File System (EFS) for two EC2 instances in different availability zones. 
## PROBLEM STATEMENT
    Explain about the Experiment.

## ALGORITHM
 ### Steps 1: Create two EC2 instances in different availability zones.
 ### Steps 2: Set up a security group that allows necessary communication between the instances and EFS.
 ### Steps 3: Create an EFS file system and mount it to both EC2 instances.
 ### Steps 4: Ensure that the EC2 instances can access the file system and share data between them.

## COMMANDS
```
sudo su
yum install httpd -y
yum install -y amazon-efs-utils
mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
cd /var/www/html
vi file  # Create a file and add some text
```
EC2 Instance 2
```
sudo su
yum install httpd -y
yum install -y amazon-efs-utils
mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
cd /var/www/html
ls
cat file  # Verify shared access by reading content created in Instance 1
```

## OUTPUT
Both EC2 instances showing EFS mounting.


![image](https://github.com/user-attachments/assets/3b9b7b96-e492-46b6-a8fd-5b84a38cd966)

The creation of a file on Instance 1.


![image](https://github.com/user-attachments/assets/7b1fdb37-293f-4c18-9692-84ea9c36d40a)



The display of that file’s contents on Instance 2 to verify shared access


![image](https://github.com/user-attachments/assets/ed03a424-2cec-45db-88cd-eacb187f4167)

## RESULT
 
Successfully set up a scalable file storage system using Amazon EFS shared between two Linux EC2 instances in different availability zones, enabling consistent data sharing.
  


