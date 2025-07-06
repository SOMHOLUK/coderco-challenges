# Challenge 1

## Scenario:

You're the new DevOps hire at a startup. They've given you a fresh Linux VM and asked you to build a production-ready Linux service setup for their Python app. But there’s no infra — you have to do it all.

Prerequisites
A fresh Linux VM. We recommend using Killercoda to get started. Or you can use your own Linux machine (AWS EC2 etc)
Challenge Requirements:

You must create a setup.sh (or Makefile) that does all of the following:

## 1. User & Permissions

Create a user called appuser (non-root) Creating a User on the Linux module
Create a directory /opt/coderco-app Creating directories
Place a server.py file in it (can be a simple http.server). The server.py is located here and the .env file is located here
Give appuser full access to /opt/coderco-app only - Setting Permissions
Make sure no other user (except root) can read/write to it

# The steps I have taken to solve the "user & permissions" challenge can be seen in the screenshots below:

## Step 1

![image1](images/code-challenge-pic-1.png)

## Step 2

![image2](images/code-challenge-pic-2.png)

## Step 3

![image3](images/code-challenge-pic-3.png)

## Step 4

![image4](images/code-challenge-pic-4.png)

## Step 5

![image5](images/code-challenge-pic-5.png)

## Step 6

![image6](images/code-challenge-pic-6.png)

## Step 7

![image7](images/code-challenge-pic-7.png)

## Step 8

![image8](images/code-challenge-pic-8.png)

## Step 9

![image9](images/code-challenge-pic-9.png)

## Step 10

![image10](images/code-challenge-pic-10.png)

## Step 11

![image11](images/code-challenge-pic-11.png)

## Step 12

![image12](images/code-challenge-pic-12.png)

## 2. Systemd Service

For some help: Creating a Linux service with systemd

Create a coderco-app.service under /etc/systemd/system

It should:

Run python3 /opt/coderco-app/server.py
Run as appuser
Restart if it fails
Enable and start the service
Show that it’s running using curl localhost:8080
Use EnvironmentFile=/opt/coderco-app/.env in your systemd unit to inject PORT and LOG_PATH. You can add this line to the [Service] section of the service file.

# The steps I have taken to solve the "Systemd Service" challenge can be seen in the screenshots below:

## Step 1

![image2](images/code-challenge-systemd-1.png)

## Step 2

![image2](images/code-challenge-systemd-2.png)

## Step 3

![image3](images/code-challenge-systemd-3.png)

## Step 4

![image4](images/code-challenge-systemd-4.png)

## Step 5

![image5](images/code-challenge-systemd-5.png)

## Step 6

![image6](images/code-challenge-systemd-6.png)

## Step 7

![image7](images/code-challenge-systemd-7.png)

## Step 8

![image8](images/code-challenge-systemd-8.png)

## Step 9

![image9](images/code-challenge-systemd-9.png)

## Step 10

![image10](images/code-challenge-systemd-10.png)

## Step 11

![image11](images/code-challenge-systemd-11.png)
