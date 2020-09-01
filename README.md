## Build CI/CD Pipelines, Monitoring, and Logging
This repository provides the supporting material for building a CI/CD pipelines, monitoring, and logging in Jenkins. This repo has two more branches, other than the master branch. 

* Blue/Green branch corresponds to the Blue/Green deployment strategy. Make sure that you checkout branches "blue" and "green" to see how blue/green deployment was performed.
* You can create any more branches for a multiple pipeline set-up. 

### Dependencies
##### 1. AWS account
You are require to have an AWS account to be able to build cloud infrastructure. Particularly, you will need to create S3 buckets, EC2 instances, and IAM users.

#### 2. Jenkins on Ubuntu VM
You will need to install Jenkins and the default plugins to assist your requirements.
Execute the following commands to install Jenkins:

* Step 1 - Update existing packages.
`sudo apt-get update`

* Step 2 - Install Java.
`sudo apt install -y default-jdk`

* Step 3 - Download Jenkins package.
`wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -`

* Step 4 - Add the following entry in your /etc/apt/sources.list.
`sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`

* Step 5 -Update your local package index.
`sudo apt-get update`

* Step 6 - Install Jenkins.
`sudo apt-get install -y jenkins`

* Step 7 - Start the Jenkins server.
`sudo systemctl start jenkins`

* Step 8 - Enable the service to load during boot.
`sudo systemctl enable jenkins`
`sudo systemctl status jenkins`


#### 3. Install Blue Ocean Plugin for Jenkins
You will need to install the following to use the Blue Ocean plugin:
1. Blue Ocean
1. Blue Ocean Executor Info
1. Blue Ocean Pipeline Editor
1. Config API for Blue Ocean
1. Display URL for Blue Ocean
1. Events API for Blue Ocean
1. Git Pipeline for Blue Ocean
1. GitHub Pipeline for Blue Ocean
1. Pipeline implementation for Blue Ocean

#### 4. Install AWS Plugin for Jenkins
You will need to install the following to use the AWS plugin for Jenkins:
1. Pipeline: AWS Steps

#### 4. Install Aqua MicroScanner for Jenkins
1. Go to `https://microscanner.aquasec.com/signup` to register for a Aqua MicroScanner token.
1. Install the Aqua MicroScanner plugin in the Jenkins plugin manager and input the token in the Configure System page.
1. Install Docker by executing the following command: `sudo apt install -y docker.io`
1. Ensure that Jenkins has the proper permissions to access Docker: `sudo usermod -a -G docker jenkins`
1. Restart Jenkins by executing the following command: `sudo systemctl restart jenkins`

## Prerequisite
1. A little knowledge of basic commands in Unix terminal.
1. Understanding of software testing frameworks - JMeter and JUnit
1. Understanding of deployment strategies 






