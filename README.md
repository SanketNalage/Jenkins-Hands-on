# Jenkins-Hands-on

<a href="https://www.jenkins.io">
  <img src="https://www.jenkins.io/images/logos/jenkins/jenkins.png" alt="Jenkins Logo" width="100">
</a>

Jenkins is like a **robot assistant** for developers. It helps automate repetitive tasks in the process of building, testing, and deploying software. Think of it as a **super-efficient** helper that takes care of all the boring and time-consuming work so developers can focus on writing code.

This repository contains hands-on examples and tutorials for setting up **Jenkins CI/CD pipelines**. It is designed to help beginners and intermediate users understand how to automate build, test, and deployment processes using Jenkins. The repository includes:

- **Sample Jenkins pipelines** (Declarative and Scripted syntax).
- **Integration with Docker** for containerized applications.
- **Integration with GitHub** for source code management.
- **Deployment examples** using Docker Compose, Kubernetes, and more.
- **Step-by-step guides** for setting up Jenkins on Ubuntu and other platforms.

Whether you're new to Jenkins or looking to enhance your CI/CD skills, this repository provides practical examples to get you started.

---

## Key Features

- **Jenkins Pipeline Examples**:
  - Basic pipeline for building and testing applications.
  - Advanced pipelines with Docker, GitHub, and deployment automation.
- **Docker Integration**:
  - Build and push Docker images to Docker Hub.
  - Deploy applications using Docker Compose.
- **GitHub Integration**:
  - Automatically trigger Jenkins builds on GitHub commits.
- **Deployment Examples**:
  - Deploy applications to local servers, cloud platforms, or Kubernetes clusters.
- **Documentation**:
  - Detailed README files for each example.
  - Step-by-step setup instructions for Jenkins and dependencies.

---

## Getting Started

### 1.Update the System:
```bash
sudo apt update
sudo apt upgrade -y
```

### 2.Install Java:
```bash
sudo apt install openjdk-11-jdk -y
```

### 3.Add Jenkins Repository:
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt update
```

### 4.Install Jenkins:
```bash
sudo apt install jenkins -y
```

### 5.Start and Enable Jenkins
```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins
```

### 5.Access Jenkins:
->Open your browser and go to http://<your-server-ip>:8080.
->Unlock Jenkins using the initial admin password:
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```