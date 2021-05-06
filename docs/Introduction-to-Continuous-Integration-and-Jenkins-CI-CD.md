<img src="../images/c4logo.png">

### In this tutorial we are going to learn
   * What is Continuous Integration
   * Jenkins Continuous Integration
   * What is Continuous Deployment
   * Jenkins Vs Jenkins Enterprise

# What is Continuous Integration
Inorder to understand the CI lets take an example

We have multiple Developers working with the same Application and have there own Feature or BugFix that they are working on and they all are contributing to the same Application by pushing there code into the same code repository. The Code Repository could be any Version Control System like gitHub. When a Developer pushes a code to the repository it is linked to a build management system like **Jenkins** that takes the code and builds it. If your application is based on **JAVA** then you can think of this as a **JAR** file. Since ther are multiple Developers pushing there code to the same Application we would like to make sure that it builds correctly and doesn't introduce any new issues into the Application. For this we could configure the build system to run tests on the build package. A popular testing tool framework is Robot Framework which can test your Application, API's or WEB Inerfaces. Once the tests pass successfully we can confirm that the build cycle is complete. This whole process of enabling multiple developers to works seemlessly on the same Application without stepping on each other's toes and at the same time ensuring that these new changes Integrate into the Application without introducing any new issues is know as **Continuous Intigration**    


<img src="../images/Continuous-Intigration.png">

# What is Continuous Delivery / Deployment
Once you package is ready you may release this to an automated pipeline known as **Continuos Delivery** CBA labs is good example. Now the next step would be take the packaged application and automatically deploy it in a target environment this could be **On-Prim Cloud Solution** like VmWare or Public Cloud Platform like  **AWS** ,**GCP** or **Azure**. So this process of automatically updating our production environment with the changes in the application is referred as **Continuous Deployment**.

<img src="../images/Continuous-Deployment.png">
