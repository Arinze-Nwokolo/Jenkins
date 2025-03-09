# Jenkins Installation.
Pre-Requisites:

### Update package repositories
 sudo apt update 
 ![sudo](./img/1.%20sudo%20apt%20%20update.png)

### install Java (JDK)

- sudo apt install openjdk-17-jre
![sudo](./img/2.%20install%20java.png)

### Verify Java is Installed 

java -version
![sudo](./img/3.%20java.png)

Now , you can proceed with installing Jenkins

![sudo](./img/4.%20jenkins%20installation.png)

### The command installs Jenkins.It involves importing the Jenkins GPG key for package verification , adding the jenkins repository to the system's sources , updating package lists , and finally , installing Jenkins through the package manager (apt-get)

Check if jenkins has been installeed , and it is up and running 

![sudo](./img/5.%20sudo%20systemctl%20enable%20jenkins.png)
![sudo](./img/6.%20sudo%20systemctl%20start%20jenkins.png)
![sudo](./img/7%20.%20sudo%20systemctl%20status%20jenkins.png)


By default , jenkins listens on port 8080 . we need create an inbound rule for this is the security group of our jenkins instance.

![sudo](./img/8.%20edit%20inbound%20rules.png)

### Set up Jenkins on the web console

http://:8080 [You can get the ec2-instance-public-ip-address from your AWS EC2 console page]

Note: If you are not interested in allowing All Traffic to your EC2 instance 1. Delete the inbound traffic rule for your instance 2. Edit the inbound traffic rule to only allow custom TCP port 8080

After you login to Jenkins, - Run the command to copy the Jenkins Admin Password - sudo cat /var/lib/jenkins/secrets/initialAdminPassword - Enter the Administrator password

![sudo](./img/9.%20unlock%20jenkins.png)

![sudo](./img/10%20.%20cat%20password.png)

### Installed suggested plugins

![sudo](./img/11.%20customize%20jenkins.png)




### Log in to jenkins console

![sudo](./img/13%20.%20new%20item.png)











