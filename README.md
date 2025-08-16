# Node.js Demo App – Jenkins CI/CD Pipeline

This project demonstrates a complete CI/CD pipeline using **Jenkins** to:
- Build a Docker image for a Node.js application
- Push the image to DockerHub
- Run the container automatically

The application is based on [HashiCorp's Demo Node.js App](https://github.com/hashicorp/demo-app-nodejs).

---

## 🚀 Workflow Overview

1. **Source Code** – Hosted on GitHub
2. **Jenkins Pipeline** – Triggered on code push to `main` branch
3. **Docker Build** – Builds the application image from the `Dockerfile`
4. **Docker Push** – Pushes the image to DockerHub
5. **Run Container** – Starts the application inside a container

---

## 🛠 Technologies Used

- **Node.js** (18-alpine base image)
- **Docker**
- **Jenkins** (Pipeline as Code with `Jenkinsfile`)
- **GitHub** (Source control)
- **DockerHub** (Container registry)

---

## 📂 Repository S
