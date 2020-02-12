
<img src="images/c4logo.png">

# In this tutorials we are going to learn
 1. **Downloading and Installing Jenkins using TomCat**
 2. **Creating Jenkins as a Service**
 3. **Starting and Stopping Jenkins**



## Install the Java Development Kit
```code
sudo yum install java-11-openjdk-devel
``` 

Download the Tomcat tarball [click me](https://tomcat.apache.org/download-90.cgi)

>wget http://apachemirror.wuchna.com/tomcat/tomcat-9/v9.0.31/bin/apache-tomcat-9.0.31.tar.gz

## Installing Tomcat 
```code
sudo yum update -y
sudo tar -xvf apache-tomcat-9.0.31.tar.gz -C /opt/
sudo ln -s apache-tomcat-9.0.31 tomcat #To create a symbolic link

sudo sh /opt/tomcat/bin/startup.sh #To start the Tomcat
```
> Note: Now you can access the tomcat Web-UI with Node-IP:8080

## Downloading jenkins WAR package

```code
sudo wget https://updates.jenkins-ci.org/download/war/2.220/jenkins.war
```

## Installing the WAR
```code
sudo cp jenkins.war tomcat/webapps/
```
```diff
- To get Jenkins Initial password for login 
+ cat /root/.jenkins/secrets/initialAdminPassword
```
> Note: Now you can access the Jenkins Web-UI with **Node-IP:8080/jenkins**

## You can install jenkins directly through yum package
```code
#Enable Jenkins repository by importing hte GPG key
sudo curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | sudo tee /etc/yum.repos.d/jenkins.repo

#Add the repository to your system with
sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key

#Once the repository is enabled, install the latest stable version of Jenkins by
sudo yum install jenkins -y

#start the Jenkins service with
sudo systemctl start jenkins

#To check whether it started successfully
sudo systemctl status jenkins

#Finally enable the Jenkins service to start on system boot
sudo systemctl enable jenkins
```

## Setting Up Jenkins
To set up your new Jenkins installation, open your browser and type your domain or IP address followed by port 8080:

```code
http://your_ip_or_domain:8080
```
A screen similar to the following will appear, prompting you to enter the Administrator password that is created during the installation:

<img src="images/Unlock-Jenkins.PNG">

## Creating Jenkins as a Service
When you Install the Jenkins through Yum package a jenkins service already created by default.

## Starting and Stopping Jenkins
```code
sudo service jenkins stop
sudo service jenkins start
```

 
  



