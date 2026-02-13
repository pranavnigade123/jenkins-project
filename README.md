# 🚀 Jenkins CI/CD Demo Project

This project demonstrates the integration of **Jenkins with GitHub** to implement a basic **CI/CD (Continuous Integration / Continuous Deployment)** pipeline using a Jenkinsfile.

The objective of this project is to understand how Jenkins automates development workflows by executing pipeline stages defined as code.

---

## 📌 Project Overview

In this project, Jenkins is configured to:

* Connect with a GitHub repository
* Automatically clone project source code
* Execute pipeline stages defined in a Jenkinsfile
* Run Linux shell commands within Jenkins workspace
* Create and manage files during pipeline execution
* Display output logs in Jenkins Console

This is a beginner-level CI/CD implementation built for learning DevOps automation concepts.

---

## 🛠️ Tools & Technologies Used

* Jenkins
* GitHub
* Ubuntu (WSL - Windows Subsystem for Linux)
* Git
* Linux Shell Scripting
* Groovy (Jenkins Pipeline DSL)

---

## ⚙️ Jenkins Pipeline Stages

The pipeline defined in the Jenkinsfile performs the following automated steps:

1. Creates a directory named `devops`
2. Creates a file inside the directory
3. Writes sample content into the file
4. Reads and displays file content in Jenkins Console Output

---

## 📂 Project Structure

```
jenkins-demo-project/
│
├── README.md
└── Jenkinsfile
```

---

## ▶️ How It Works

1. Jenkins is configured to connect with this GitHub repository.
2. Jenkins pulls the Jenkinsfile from the repository.
3. The pipeline defined in the Jenkinsfile is executed automatically.
4. The execution results can be viewed in Jenkins Console Output.

---

## 🎯 Learning Outcomes

* Understanding Jenkins Pipeline as Code
* Executing Linux commands via Jenkins
* GitHub and Jenkins integration
* Workspace handling in Jenkins
* Basic CI/CD workflow automation

---

## 📌 Author

**Pranav Nigade**
Aspiring DevOps Engineer
