
---

# **Introduction to Jenkins and CI/CD**

## **Introduction to CI/CD**

**Continuous Integration (CI)** and **Continuous Delivery/Deployment (CD)** are modern software development practices designed to **enhance efficiency, reliability, and speed**.

- **CI** involves developers frequently integrating their code into a shared repository. Each integration triggers **automated builds and tests**, allowing for early detection of errors.
- **CD** (Continuous Delivery/Deployment) ensures the software is always in a **deployable state**. It automates the deployment process for faster and safer releases.

> The CI/CD pipeline encourages **automation**, **collaboration**, and **continuous improvement**, helping teams release high-quality software rapidly and reliably.

---

## **What is Jenkins?**

**Jenkins** is a leading **open-source automation server** used for building, testing, and deploying software.

- Automates repetitive development tasks
- Supports **CI/CD pipelines**
- Integrates with **version control systems** like Git
- Highly extensible with **hundreds of plugins**
- Allows you to define workflows as code using **Jenkins Pipelines**

### **Why Jenkins?**

- Automates the software development lifecycle
- Improves software delivery speed and quality
- Reduces human error and manual intervention
- Works well with tools like **Docker, GitHub, Maven**, and more

---

## **Project Pre-requisites**

To follow this project smoothly, learners should have completed:

- Foundation Core Programs 1 – 3

---

## **Project Goals**

By the end of this project, you will:

✅ Understand **CI/CD principles** and their value in software development  
✅ Gain proficiency in **installing, configuring, and navigating Jenkins**  
✅ Be able to **create and manage Jenkins jobs**  
✅ Learn how to automate builds, run tests, and deploy apps using Jenkins  
✅ Apply best practices like:
- **Parameterized builds**
- **Tool integrations**
- **Docker-based pipelines**

---

## **Project Highlights**

- Introduction to CI/CD  
- What is Jenkins?  
- Project Prerequisites  
- Project Goals  
- Getting Started with Jenkins  
- Jenkins Jobs  
- Creating a Freestyle Project  
- Connecting Jenkins to Source Code Management  
- Configuring Build Triggers  
- Creating a Pipeline Job  
- Writing Jenkins Pipeline Script  
- Installing Docker  
- Building a Pipeline Script

---

## **Getting Started with Jenkins**

Let’s begin by installing and setting up Jenkins on a Linux server (e.g., Ubuntu).

---

### **1. Update Package Repositories**

```bash
sudo apt update
```

---

### **2. Install JDK (Java Development Kit)**

Jenkins requires Java to run.

```bash
sudo apt install default-jdk-headless
```

---

### **3. Install Jenkins**

```bash
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

sudo apt update

sudo apt-get install jenkins
```

This does the following:
- Adds the Jenkins GPG key
- Adds the Jenkins repository
- Updates the system package index
- Installs Jenkins using `apt-get`

---

### **4. Start and Verify Jenkins Service**

Check if Jenkins is running:

```bash
sudo systemctl status jenkins
```

---

### **5. Configure Security Group (For Cloud Instances)**

By default, Jenkins runs on **port 8080**.  
👉 Ensure your instance’s **security group** has an **inbound rule** that allows traffic on **TCP port 8080**.

---

## **Access Jenkins Web Interface**

1. Open your browser and navigate to:

```
http://<your-public-ip>:8080
```

2. Unlock Jenkins by retrieving the initial admin password:

```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

3. Install the **Suggested Plugins**

4. Create an **Admin User Account**

5. Log in to the Jenkins dashboard

---
