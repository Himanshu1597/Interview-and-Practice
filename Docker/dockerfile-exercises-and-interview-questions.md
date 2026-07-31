---

# 📘 Dockerfile Practice Exercises & Interview Questions

*A complete hands-on guide to mastering Dockerfiles*

---

# 📚 Practice Exercises

## 🟢 Exercise 1 — Basic Static Website using Nginx

**Objective**

Create a Docker image that serves a simple HTML website using Nginx.

**Skills Practiced**

* FROM
* COPY
* EXPOSE
* CMD

---

## 🟢 Exercise 2 — Python Flask App Dockerfile

**Objective**

Containerize a simple Flask application.

**Skills Practiced**

* WORKDIR
* requirements.txt
* pip install
* CMD

---

## 🟢 Exercise 3 — Node.js App with Cache Optimization

**Objective**

Create a Dockerfile that rebuilds quickly by taking advantage of Docker layer caching.

**Skills Practiced**

* COPY package.json first
* npm install
* Docker cache

---

## 🟢 Exercise 4 — Java Spring Boot JAR Dockerfile

**Objective**

Run a Spring Boot application packaged as a JAR file.

**Skills Practiced**

* Java Runtime image
* COPY
* ENTRYPOINT

---

## 🟢 Exercise 5 — Multi-stage Go Build (Under 20 MB)

**Objective**

Build a Go application using multi-stage builds and produce a lightweight final image.

**Skills Practiced**

* Multi-stage builds
* Scratch/Alpine images
* Binary optimization

---

## 🟢 Exercise 6 — Review & Secure a Poor Dockerfile

**Objective**

Identify security and performance issues in a Dockerfile and improve it.

**Focus Areas**

* Root user
* Image size
* Secrets
* Layers

---

## 🟢 Exercise 7 — Optimize Docker Cache for Node.js

**Objective**

Improve Docker build performance for a large Node.js project.

---

## 🟢 Exercise 8 — Use ARG & ENV

**Objective**

Pass configuration during build time and runtime.

**Topics**

* ARG
* ENV
* Build arguments
* Runtime variables

---

## 🟢 Exercise 9 — Add HEALTHCHECK

**Objective**

Add a HEALTHCHECK instruction to an Nginx image.

---

## 🟢 Exercise 10 — Production-ready Flask Dockerfile

**Objective**

Write a Dockerfile suitable for production deployment.

Include:

* Non-root user
* Gunicorn
* Healthcheck
* Optimized layers
* Small image

---

## 🟢 Exercise 11 — Improve a Basic Node.js Dockerfile

**Objective**

Take a beginner Dockerfile and make it production-ready.

---

## 🟢 Exercise 12 — Debug a Container That Exits Immediately

**Objective**

Find why a container exits and fix the issue.

Use commands like:

* docker logs
* docker exec
* docker inspect

---

## 🟢 Exercise 13 — Dockerize an Existing GitHub Project

**Objective**

Pick any public GitHub project and containerize it from scratch.

---

# 🎯 Dockerfile Interview Questions

## 🟦 Basics

1. What is a Dockerfile?
2. CMD vs ENTRYPOINT?
3. COPY vs ADD?
4. RUN vs CMD?
5. ARG vs ENV?
6. Why use WORKDIR instead of RUN cd?
7. What happens if multiple CMD instructions exist?
8. What happens if EXPOSE is omitted?

---

## 🟨 Docker Internals

9. What is a Docker layer?
10. Which Dockerfile instructions create layers?
11. How does Docker layer caching work?
12. How can you improve Docker build speed?
13. Why copy package.json before the source code?
14. What is a multi-stage build?
15. Why use Alpine? When should you avoid it?

---

## 🟥 Security

16. Why avoid running containers as root?
17. What is `.dockerignore`?
18. Why should secrets never be stored inside Dockerfiles?
19. How do you securely pass secrets during build?
20. How do you scan Docker images for vulnerabilities?

---

## 🟩 Image Optimization

21. How do you reduce Docker image size?
22. Why do layers rebuild after changing one file?
23. Explain the Docker image build process.
24. Why should you avoid using the `latest` tag?

---

## 🟪 Troubleshooting

25. How do you debug a failed Docker build?
26. Explain the lifecycle from Dockerfile → Image → Container.
27. An application works locally but not inside Docker. What would you check first?

---

## ⭐ Scenario-Based Questions

### Scenario 1

Optimize a **2 GB Docker image**.

Discuss:

* Multi-stage builds
* Smaller base images
* Layer optimization
* Removing unnecessary files

---

### Scenario 2

Docker builds take **10 minutes** after every code change.

How would you optimize caching?

---

### Scenario 3

Your application cannot connect to the database inside Docker.

What would you troubleshoot?

---

### Scenario 4

The application works on your laptop but fails in Production.

Possible causes?

* Environment variables
* Networking
* Volumes
* File permissions
* Image version
* Missing dependencies

---

# 🚀 Goal

After completing all exercises, you should be comfortable with:

* ✅ Writing Dockerfiles from scratch
* ✅ Optimizing Docker images
* ✅ Understanding Docker caching
* ✅ Debugging container issues
* ✅ Writing production-ready Dockerfiles
* ✅ Answering Docker interview questions confidently

---

### Recommendation

Instead of saving this as a plain `.txt` file, save it as **Markdown (`.md`)** or **Word (`.docx`)**. On a Mac, Markdown previews beautifully in editors like VS Code, Obsidian, Typora, or even GitHub, and a `.docx` version with colored headings and proper fonts will look polished in Microsoft Word or Apple Pages.
