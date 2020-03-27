# Assignment 5

In this assignment we will learn to create and use S3 buckets, launch an EC2 instance with Jupyter server, create notebooks.


### Part 1: Create a static website from an S3 bucket
1. create an s3 bucket
1. create a static website on s3 https://medium.com/@KerrySheldon/s3-exercise-2-1-host-a-static-website-on-s3-a5f9635c2258

### Part 2: Setup an EC2 instance with a Jupyter server
1. In AWS console, launch an ubuntu EC2 instance and note its security group. 
2. In AWS console, navigate to `Networks and Security > Security Groups`. Find the security group of your EC2 instance. Edit its `Inbound Rules`.

1. configure access, set the security group with inbound access on port 8888 from anywhere (for Jupyter)
1. Connect to your instance using `ssh`.
```bash
ssh -i <your-certificate-file>.pem ubuntu@##-##-###-####.ccompute-#.amazonaws.com
```
1. install python and jupyter on your EC2 instance https://docs.aws.amazon.com/dlami/latest/devguide/setup-jupyter.html
```bash 
sudo apt update 
sudo apt install python3-pip
sudo pip3 install jupyter 
```
1. Set up SSH tunnel to the instance https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-ssh-tunnel-local.html
```bash
ssh -N -L 8888:127.0.0.1:8888 -i <your-certificate-file>.pem ubuntu@##-##-##-###-###.compute-1.amazonaws.com
```
1. Connect to Jupyter notebook in your browser `https://127.0.0.1:8888`

### Part 3: Access S3 objects from Python 
1. install boto3 https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html
1. create access key/secret key pair configure access https://aws.amazon.com/blogs/security/wheres-my-secret-access-key/
1. read/write objects from s3 buckets from python using boto3 https://boto3.amazonaws.com/v1/documentation/api/latest/guide/s3-examples.html

