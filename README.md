# Configure jenkins 2.x with tomcat 8.x in AWS (Amazon Linux AMI)

## Software already installed
The machine already has the following software installed:
 * [Jenkins 2.x](https://youtu.be/MSkcjqIU5SI): This video explains how to install jenkins in an AWS EC2 instance.
 * [Tomcat 8.x](https://youtu.be/lCex88J-fIo): This video explains how to install tomcat in an AWS EC2 instance.
 * [Java 8](): Both of the previous videos install java 8 at the beginning.

## Project
This is the WAR file we are going to deploy from Jenkins to the Tomcat container.
 * [Empty Spring Rest Project](https://github.com/carlosCharz/emptyspringrestexample): GitHub link to download the empty spring rest project.

## Jenkins Configuration
* fuser: to display the process id(PID) of every process using the specified files
```
fuser -v -n tcp 8080
```
