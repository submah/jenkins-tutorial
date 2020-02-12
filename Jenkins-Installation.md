
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
 
  



