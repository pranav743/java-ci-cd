# Spring Boot CI/CD Example

This project demonstrates a complete CI/CD pipeline for a Spring Boot application using Maven, GitHub Actions, and Docker Hub.

---

## 🚀 Build & Run Locally

### 1. Build & Run with Maven

```
mvn clean package
mvn spring-boot:run
```

App will be available at: http://localhost:8080

---

### 2. Build & Run with Docker

#### Build Docker Image
```
docker build -t masterpranav07/springboot-cicd .
```

#### Run Docker Container
```
docker run -p 8080:8080 masterpranav07/springboot-cicd
```

---

## 🔄 CI/CD Pipeline (GitHub Actions)

- On every push to the `main` branch:
  1. Maven build & test
  2. Docker image build
  3. Docker image push to Docker Hub: [`masterpranav07/springboot-cicd`](https://hub.docker.com/r/masterpranav07/springboot-cicd)

### GitHub Secrets Required
- `DOCKERHUB_USERNAME` = `masterpranav07`
- `DOCKERHUB_TOKEN` = Docker Hub access token

---

## ✅ How to Verify CI/CD Workflow

1. Push code to the `main` branch.
2. Go to the **Actions** tab in your GitHub repo to see the workflow run.
3. On success, check Docker Hub for the updated image: [`masterpranav07/springboot-cicd`](https://hub.docker.com/r/masterpranav07/springboot-cicd)

---

## 📎 Useful Links
- **GitHub Repo:** [YOUR_REPO_LINK_HERE]
- **Docker Hub:** [https://hub.docker.com/r/masterpranav07/springboot-cicd](https://hub.docker.com/r/masterpranav07/springboot-cicd)

---

## 📝 Notes
- Make sure to set the required GitHub secrets before running the workflow.
- The Docker image exposes port 8080.
- For Apple Silicon (M1/M2/M4), Docker will build for your architecture by default.
