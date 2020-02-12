
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
 
  



