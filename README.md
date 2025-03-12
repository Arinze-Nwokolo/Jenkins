# The project is Jenkins Installation.

## Project Objective 

The ojective of this project that aims at Jenkins installation is to successfully set up Jenkins ,an open-source automation server,to facilitate continuous integration (CI)and continuous deployment(CD).




## Step 1. Pre-requisites
              
To install and run Jenkins effectively , its essential to meet specific software prerequisites

### 1 Update package repositories
 - sudo apt update 
 ![sudo](./img/1.%20sudo%20apt%20%20update.png)

### 2 install Java (JDK)

Jenkins is a Java-based application and requires a compatible JDK.
Ensure you have JDK 17 OR 21 Installed.(jenkins.io)

- sudo apt install openjdk-17-jre
![sudo](./img/2.%20install%20java.png)

### 3  Verify Java is Installed 

- java -version
![sudo](./img/3.%20java.png)

## Step 2 Jenkins Installation]
 - The command installs Jenkins . It involves importing the Jenkins GPG key for package verification , adding the jenkins repository to the system's sources , updating package lists , and finally , installing Jenkins through the package manager

![sudo](./img/4.%20jenkins%20installation.png)



## Step 3 Check if jenkins has been installeed , and it is up and running 
- Sudo systemctl status Jenkins

![sudo](./img/5.%20sudo%20systemctl%20enable%20jenkins.png)
![sudo](./img/6.%20sudo%20systemctl%20start%20jenkins.png)
![sudo](./img/7%20.%20sudo%20systemctl%20status%20jenkins.png)

## Step 4 AWS EC2 INSTANCE INBOUND RULES

 ** Note ** By default, Jenkins will not accessiable to the external world due to the inbound traffice restriction by AWS. Open port 8080 in the inbound traffic rules as show below.

- Ec2 > Instance >Click on 
- In the bottom tabs > Click on Security
- Security groups
- Add inbound traffic rules as shown in the image( you canjust allow TCP 8080 as well )


![sudo](./img/8.%20edit%20inbound%20rules.png)

## Step 5 Set up Jenkins on the web console

-http://:8080 [You can get the ec2-instance-public-ip-address from your AWS EC2 console page]

Note: If you are not interested in allowing All Traffic to your EC2 instance 1. Delete the inbound traffic rule for your instance 2. Edit the inbound traffic rule to only allow custom TCP port 8080

After you login to Jenkins, - Run the command to copy the Jenkins Admin Password - sudo cat /var/lib/jenkins/secrets/initialAdminPassword - Enter the Administrator password

![sudo](./img/9.%20unlock%20jenkins.png)

![sudo](./img/10%20.%20cat%20password.png)

## Step 6  Click on Installed suggested plugins

![sudo](./img/11.%20customize%20jenkins.png)




## Step 7 Log in to jenkins console

![sudo](./img/13%20.%20new%20item.png)











