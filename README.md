# AWS EC2 Task 2 — Deploy a Node.js Application

## Overview

This task involved deploying a simple Node.js application on an Ubuntu EC2 instance on AWS.

## Objectives

- Launch and connect to an AWS EC2 instance.
- Install Node.js and npm.
- Create a Node.js application using Express.js.
- Run the application on port 3000.
- Configure the EC2 Security Group to allow traffic on port 3000.
- Access and verify the application through the EC2 public IP address.

## Steps Taken

### 1. Updated the Ubuntu Server

Updated the system packages using:

```bash
sudo apt update
sudo apt upgrade -y

2. Installed Node.js

Installed Node.js using NodeSource and verified the installation:
node -v
npm -v

3. Created the Node.js Application

Created the application directory:
mkdir ~/node-app
cd ~/node-app

Initialized the Node.js project:
npm init -y

Installed Express:
npm install express

4. Created the Application

Created app.js containing a simple Express server.

The application listens on port 3000 and responds with:

Hello from my Node.js app running on AWS EC2!

5. Started the Application

The application was started with:

node app.js

The server displayed:

Server running on port 3000

6. Configured the Security Group

Added an inbound Security Group rule allowing TCP traffic on port 3000.

7. Tested the Application

First tested the application locally from the EC2 server:

curl http://localhost:3000

The application returned:

Hello from my Node.js app running

The application was then successfully accessed through the EC2 public IP address using:

http://16.170.7.25:3000

#Difficulty Faced

The application initially did not load in the browser. After checking the application and testing it locally with curl, I identified that the issue was with the way the public IP address was entered.

I initially entered the IP address using hyphens instead of dots.

Correct format:

http://16.170.7.25:3000

The application then loaded successfully.

#What I Learned
How to install Node.js on an Ubuntu EC2 instance.
How to initialize a Node.js project.
How to install and use Express.js.
How to run a Node.js server on an EC2 instance.
How AWS Security Groups control inbound traffic.
How to expose an application through a specific port.
How to test a running web application using curl.
How to access a Node.js application remotely using an EC2 public IP address.
Verification

The Node.js application was successfully deployed and accessed through the EC2 public IP address on port 3000.

Conclusion

Task 2 was successfully completed. I deployed a Node.js application on an AWS EC2 Ubuntu server and verified that it was accessible from a web browser.
