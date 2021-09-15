<img src="../images/c4logo.png">


## Steps:
1. Open the file tomathomedir/webapps/manager/META-INF/context.xml and Change the allow field to allow="^.*$"
2. Open file tomcathomedir/conf/tomcat-users.xml remove all the predefined roles and users and add the below lines to the file.
```text
<role rolename="tomcat"/>
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<user username="tomcat" password="password" roles="tomcat"/>
<user username="manager" password="password" roles="tomcat,manager-gui"/>
<user username="jenkins" password="jenkins" roles="tomcat,manager-gui,manager-script"/>
```

3. 
