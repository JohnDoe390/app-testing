# app-testing

#Description
This is a node.js application that is containerized using Docker and deployed on a aws ec2 instance

#Feature
-Node.js
-Containerize using Docker
-Deploy on ec2 instance

#How to run

```bash
-docker build -t myapp .
-docker run -d -p 3000:3000 myapp

Deployment
This is deployed to aws ec2 instance and can be accessed via public ip
