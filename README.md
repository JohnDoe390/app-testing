📦 DevOps Training – Node.js Docker Deployment
📖 Description

This project demonstrates deploying a Node.js application using Docker on an AWS EC2 instance. The application is containerized, deployed, and updated on a live server.

🚀 Features
Node.js application
Docker containerization
Deployment on AWS EC2
Public access via EC2 public IP
Application update (v2 redeployment)
⚙️ How It Works
Build Docker image
Run container with port mapping
Access application via public IP
Update by rebuilding and restarting container
🛠️ Tech Stack
AWS EC2
Docker
Node.js
Ubuntu Linux
🔗 Demo

Accessible via:

https://www.youtube.com/watch?v=CBpNdnFJ2Y8

(Video demo included in repository / YouTube)

🧠 What I Learned
Containerizing applications using Docker
Deploying applications on cloud (EC2)
Debugging using logs and curl
Updating applications safely

🚀 Recent Optimizations & Production Readiness
I recently refactored the backend architecture and containerization strategy to meet industry standards for security and CI/CD efficiency.
1. Infrastructure & Networking
Dynamic Port Mapping: Migrated from hardcoded ports to process.env.PORT with a fail-safe fallback. This allows the container to be injected with any port by AWS Load Balancers or Docker without code changes.
Health Check Implementation: Added a /health endpoint (Status 200). This provides a "heartbeat" for Target Group Health Checks and Docker restart policies, ensuring high availability.
2. Docker Optimization
Layer Caching Strategy: Reorganized the Dockerfile to copy package.json and run npm install separately. This leverages Docker Layer Caching, reducing build times in the CI/CD pipeline by up to 80% when dependencies haven't changed.
Security & Footprint: Switched to node:20-alpine base image to minimize the attack surface and reduce image size for faster deployment to EC2.
Resource Management: Implemented .dockerignore to exclude node_modules and local secrets, preventing architecture conflicts and keeping production images "lean."
3. Security & Environment
Secrets Management: Decoupled configuration from logic using .env files.
Repository Hygiene: Configured .gitignore to prevent sensitive environment variables from leaking into version control.
