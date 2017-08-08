# Configure jenkins 2.x with tomcat 8.x in AWS (Amazon Linux AMI)
The objective is to create a Jenkins job to automatically deploy a built war file to a Tomcat instance. This project basically covers the configuration of Jenkins.



## Software already installed
The machine already has the following software installed from my previous tutorials:

 1. [Jenkins 2.x](https://youtu.be/MSkcjqIU5SI): This video explains how to install jenkins in an AWS EC2 instance.
 * Port: 8081
 
 2. [Tomcat 8.x](https://youtu.be/lCex88J-fIo): This video explains how to install tomcat in an AWS EC2 instance.
 * Port: 8080
 * User: admin
 * Password: adminadmin
 
 
 
 ## Software & Plugins to install
 **1. Git**
```
sudo yum install git
```
To know the installation path:
```
which git
whereis git
```
output: /usr/bin/git



**2. Java 8**
* It wil be installed automatically from Jenkins Tool Configuration (web).



**3. Maven 3**
* It will be installed automatically from Jenkins Tool Configuration (web).



**4. Deploy to Container plugin**
* It should be done manually.
* Path: Manage Jenkins -> Manage Plugins -> Available -> Deploy to Container plugin
* Restart Jenkins after installation.



## Spring Project
[Empty Spring Rest Project](https://github.com/carlosCharz/emptyspringrestexample): GitHub link to download the empty spring rest project.
 * This is the WAR file that we are going to deploy from Jenkins to the Tomcat container.
 * url: https://github.com/carlosCharz/emptyspringrestexample
 * You should have a github account (username and password).



## Jenkins Web Configuration Steps
**1. Installation - Java**
![Java](http://corporacionkristalia.com/jenkins-sources/1-install-java.png)


**2. Installation - Git**
![Git](http://corporacionkristalia.com/jenkins-sources/2-install-git.png)


**3. Installation - Maven**
![Maven](http://corporacionkristalia.com/jenkins-sources/3-install-maven.png)


**4. Job Configuration - Project Type**
![Project Type](http://corporacionkristalia.com/jenkins-sources/4-project.png)


**5. Job Configuration - General Data**
![General Data](http://corporacionkristalia.com/jenkins-sources/5-general-data.png)


**6. Job Configuration - Source Code**
![Source Code](http://corporacionkristalia.com/jenkins-sources/6-source-code.png)


**7. Build Configuration - Delete Workspace**
![Delete Workspace](http://corporacionkristalia.com/jenkins-sources/7-build-delete.png)


**8. Build Configuration - Maven Goals**
![Maven Goals](http://corporacionkristalia.com/jenkins-sources/8-build-maven.png)


**9. Post Build Configuration - Deploy WAR & Delete Workspace**
![Deploy WAR](http://corporacionkristalia.com/jenkins-sources/9-build-deploy.png)
