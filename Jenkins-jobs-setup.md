
<img src="images/c4logo.png">

# In this tutorials we are going to learn
  1. **Setting Up Jenkins Maven and Freestyle job**
  2. **Jenkins parametrized jobs setup (choice params,boolean params)**
  3. **Email notification jobs**
  4. **Parallel jobs configuration**
  5. **nodes (slaves) configuration**


  ## Setting Up Jenkins Maven and Freestyle job

  #### Freestyle job
  For Freestyle job Login to jenkins then click on New Item then provide a name to youre job then select FreeStyle then click on OK.

  <img src="images/Jenkins-New-Item.PNG">

  <img src="images/Jenkins-Dev.PNG">

  Now got to the Build and click on **Add Build Step** then select **Execute Shell**. In the Command box provide the command to execute, then click on **save** button then click on BuildNow to trigger a build.

  <img src="images/Jenkins-FreeStyle-Job.PNG">

  <img src="images/Jenkins-FreeStyle-Job-BuildNow.PNG">

  To view the Console output

  <img src="images/Jenkins-FreeStyle-Job-Log.PNG">

  <img src="images/Jenkins-FreeStyle-Job-ConsoleOutput.PNG"> 
  
  #### Maven job
  Login to Jenkins then click on **Manage Jenkins** then click on **Global Tool Configuration**. Go to Maven and click on the checkbox to Install automatically then save the changes.
  
  To Install Git 
  <img src="images/Jenkins-Maven-Git-Installation.PNG">
  
  <img src="images/Jenkins-Maven-Installation.PNG">

  To Create a Maven job Click on New Item on you Jenkins dashboard then provide name to you job then select Maven Project

  <img src="images/Jenkins-Maven-Job.PNG">

  GitHub Project URL https://github.com/submah/deploy-hello-world-with-jenkins.git
 
  Go to Source Code Management and select Git then provide the repository url as above else you can specify you own github url.
  
  <img src="Jenkins-Maven-Git.PNG">
  
  On Build specify the Goals and Options as **clean package**

  <img src="images/Jenkins-Maven-Build.PNG">
 
  Save the changes and clik on Build now, to see the Console Output click on hte build Number

  <img src="images/Jenkins-Maven-Build-Console-Outpu.PNG">

  ## Jenkins parametrized jobs setup
  #### Choice Parameter
 Go to Any Job and click on **This project is parameterized** checkbox. Then click on Add parameter and select **Choice Parameter**
 
 <img src="images/Jenkins-Choice-Parameter.PNG">
 Go to Build and select **Execute Shell** and Provide the below command 
 ```shell
 echo "You have selected ${Fruit}"
 ```
 <img src="images/Jenkins-Choice-Parameter-Build.PNG">
