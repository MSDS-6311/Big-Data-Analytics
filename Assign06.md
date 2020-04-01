# Assignment 6

Read [User Guide to EC2 Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)

In this assignment we learn by example to launch an EC2 instance, install open-source software for data science, and connect to the server.

The aim is to use a Jupyter notebook on an EC2 instance running in the cloud. 

### Part 1. Launch an EC2 Instance
After logging into your AWS console https://aws.amazon.com/console, navigate to the EC2 section to launch an Ubuntu EC2 instance. The interface prompts you through the process. 
 * Step 1: Choose an AMI: Select an Ubuntu 18.04 system of the 64-bit `x86` archiecture.  
 * Step 2: Choose Instance Type: pick `t2.medium`. Read about other instance types too. 
 * Step 3: Configure Instance Details. Accept defaults > Next
 * Step 4: Add Storage: Expand to more storage (e.g. 128 GiB) to work with bigger files.
 * Step 5: Add Tags: Accept defaults > Next
 * Step 6: Security Group: Accept defaults > Next
 * Step 7: Review and Launch using one of your existing key pairs.

### Part 2. Connect to your instance**
 The instance will take a minute to initialize. Once it's ready, right-click on it and select "Connect". Follow the same process to connect to your new instance and you did to the course instance earlier in the course. 
```bash
ssh -i <your-certificate-file>.pem ubuntu@##-##-###-####.ccompute-#.amazonaws.com
```

### Part 3. Install open-source software** 
We will install python and jupyter. 

Ubuntu has a software packaging tool named `apt`.  It can quickly install any selection of free software. Learn about `apt`: https://help.ubuntu.com/lts/serverguide/apt.html.

You can log in as a system administrator, so you can execute commands for the whole system using the `sudo` command. Update the system, install the python package manager `pip` and then use it to install jupyter.

```bash 
$ sudo apt update 
$ sudo apt install python3-pip
$ sudo pip3 install jupyter 
```

### Part 4. Launch the Jupyter Notebook server
On your remote server, follow these instructions to launch a jupyter server 

Launch jupyter server 
```
$ jupyter-notebook 
```
The notebook server will launch on port 8888.

### Part 5. Connect from your local computer 

Before you can connect to the jupyter server, you need to set up an SSH tunnel to map port 8888 on the remote server to some port (e.g. 9000) on your local machine. 

You can do this by adding `-N -L 8888:127.0.0.1:9999` to ssh connection command from Part 2.

```bash
ssh -i <your-certificate-file>.pem ubuntu@##-##-###-####.ccompute-#.amazonaws.com -N -L 8888:127.0.0.1:9999
```

You can now connect to the remote notebook using the browser at the address: https://127.0.0.1:9000 (as if it were running on your computer).

### Part 6. Stop your instance 
After you are done playing with jupyter notebooks and save your work, go back to the AWS console and stop your instance. You can start it again next time. 
Select the instance. Select *Action* - *Instance State* - *Stop*.
