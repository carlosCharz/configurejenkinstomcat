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
 3. Git
```
sudo yum install git
```

4. Java 8
* It wil be installed automatically from Jenkins Tool Configuration.

5. Deploy to Container plugin
* It should be done manually.
* Path: Manage Jenkins -> Manage Plugins -> Available -> Deploy to Container plugin
* Restart Jenkins after installation.

6. Maven3
* It will be installed automatically from Jenkins Tool Configuration.

## Project
[Empty Spring Rest Project](https://github.com/carlosCharz/emptyspringrestexample): GitHub link to download the empty spring rest project.
 * This is the WAR file we are going to deploy from Jenkins to the Tomcat container.
 * url: https://github.com/carlosCharz/emptyspringrestexample
 * username: xxxx@xxxx.com
 * password: xxxxxxxxx

## Commands to know the paths
```
which git
whereis git
```
output: /usr/bin/git
