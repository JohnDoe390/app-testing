# Node.js Enterprise-Ready Deployment (Docker + AWS EC2)

## 📌 Overview
This repository demonstrates a professional, containerised deployment of a **Node.js** application. It is engineered for reliability, using **Docker** for environment consistency and **AWS EC2** for scalable cloud hosting.

## 🚀 Tech Stack
*   **Runtime:** Node.js (v20+)
*   **Containerization:** Docker
*   **Cloud Provider:** AWS (EC2 Instance)
*   **OS:** Ubuntu / Amazon Linux 2

## ✨ Key Features
*   **Dockerized Architecture:** Ensures the app runs the same in development and production.
*   **Optimized Image:** Uses a lightweight base image to reduce deployment time and security surface area.
*   **AWS Cloud Hosting:** Deployed on a high-availability EC2 instance with configured Security Groups.
*   **Automated Lifecycle:** Simple build-and-run commands for rapid scaling.

## 🛠️ Infrastructure Setup (AWS)
1.  **Security Groups:** Configured to allow inbound traffic on Port `3000` (App) and Port `22` (SSH management).
2.  **IAM Roles:** Restricted access following the principle of least privilege.
3.  **Persistence:** EBS volume attached for reliable data storage.

## 📦 Local Installation & Setup

### Prerequisites
*   Docker installed on your machine.
*   AWS CLI (optional, for remote management).

### Steps to Run
1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd pp-testing
