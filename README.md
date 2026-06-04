#  Dockerized Web Application Deployment on AWS

## 📌 Project Overview

This project demonstrates the end-to-end process of containerizing a web application using Docker and deploying it on an AWS EC2 instance. The application is served using the Nginx web server and made accessible over the internet through proper networking and security configurations.

This project highlights core DevOps concepts such as containerization, cloud deployment, and environment consistency.

---

## 🧰 Tech Stack

* **Docker** – Containerization platform
* **AWS EC2** – Cloud compute service
* **Nginx** – Web server
* **Git & GitHub** – Version control
* **Linux (Ubuntu)** – Server environment

---

## ⚙️ Key Features

* Containerized a web application using Docker
* Created a custom Dockerfile for consistent environment setup
* Deployed application on AWS EC2 instance
* Configured port mapping to expose application externally
* Enabled access over the internet via public IP
* Ensured portability across different environments

---

## 📁 Project Structure

```
devops-project/
│── index.html
│── Dockerfile
```

---

## 🐳 Docker Configuration

### 🔹 Dockerfile

```
FROM nginx:latest
COPY . /usr/share/nginx/html/
```

### 🔹 Build Docker Image

```
docker build -t devops-project .
```

### 🔹 Run Docker Container

```
docker run -d -p 80:80 devops-project
```

---

## ☁️ AWS Deployment Steps

### 🔹 1. Launch EC2 Instance

* Choose Ubuntu OS
* Select t2.micro (Free Tier)
* Allow inbound rules:

  * SSH (22)
  * HTTP (80)

---

### 🔹 2. Connect to EC2

Use EC2 Instance Connect or SSH

---

### 🔹 3. Install Docker

```
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
```

---

### 🔹 4. Clone Repository

```
git clone <your-github-repo-link>
cd devops-project
```

---

### 🔹 5. Build and Run Application

```
sudo docker build -t devops-project .
sudo docker run -d -p 80:80 devops-project
```

---

### 🔹 6. Access Application

Open browser and navigate to:

```
http://<your-ec2-public-ip>
```
---

## 🎯 Project Outcome

* Successfully containerized a web application
* Deployed application on AWS cloud
* Made application accessible over the internet
* Demonstrated real-world DevOps workflow

---

## 🚀 Future Enhancements

* Implement CI/CD pipeline using Jenkins
* Integrate GitHub Webhooks for automation
* Use Docker Compose for multi-container setup
* Deploy using Kubernetes for scalability

---

