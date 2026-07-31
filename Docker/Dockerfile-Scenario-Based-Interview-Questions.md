# 🐳 Dockerfile Scenario-Based Interview Questions

> These questions are designed to test your **problem-solving approach**, **Docker fundamentals**, **best practices**, and **real-world production experience**. Focus on explaining **why** you would choose a particular solution, not just **what** the solution is.

---

# 📚 Table of Contents

1. Image Optimization
2. Docker Caching
3. Debugging Containers
4. Networking
5. Kubernetes & Cloud
6. CI/CD
7. Security
8. Performance
9. Dockerfile Design
10. Production Best Practices

---

# 🚀 Scenario-Based Questions

## Scenario 1: Large Docker Image

### Problem

Your Docker image is **2 GB**. How would you reduce its size?

**Things to Discuss**

- Multi-stage builds
- Choosing smaller base images
- Removing unnecessary dependencies
- Cleaning package manager cache
- Combining RUN instructions
- Using `.dockerignore`
- Distroless images
- Static binaries (Go)

---

## Scenario 2: Docker Cache

### Problem

Every code change triggers a full rebuild.

How do you optimize Docker caching?

**Things to Discuss**

- Layer ordering
- Copy dependency files first
- Cache package installation
- Separate frequently changing files
- BuildKit cache mounts

---

## Scenario 3: Container Exits Immediately

### Problem

Your container starts and immediately exits.

How would you troubleshoot?

**Things to Discuss**

- docker logs
- docker inspect
- docker ps -a
- ENTRYPOINT
- CMD
- Foreground vs background processes
- Exit codes

---

## Scenario 4: Works Locally but Not in Docker

### Problem

The application works on your machine but fails inside Docker.

What would you check?

**Things to Discuss**

- Missing dependencies
- File paths
- Environment variables
- Permissions
- Working directory
- Mounted volumes
- Different OS behavior

---

## Scenario 5: Database Connectivity

### Problem

The container cannot connect to the database.

How do you debug networking?

**Things to Discuss**

- Docker networks
- Container DNS
- Service names
- Port mapping
- Firewall
- Database listening address
- docker network inspect

---

## Scenario 6: AWS Access in Kubernetes

### Problem

The application can access AWS resources locally but not inside Kubernetes.

What would you investigate?

**Things to Discuss**

- IAM Role
- IRSA
- EKS Pod Identity
- Service Account
- Trust Policy
- AWS SDK credential chain
- Environment variables

---

## Scenario 7: CI/CD Failure

### Problem

Build succeeds locally but fails in CI/CD.

What differences could cause this?

**Things to Discuss**

- Different Docker versions
- Missing secrets
- Build arguments
- Network restrictions
- File permissions
- Case-sensitive file systems
- Build context

---

## Scenario 8: Secrets in Image

### Problem

Security discovers secrets inside your image.

How did they get there and how do you prevent it?

**Things to Discuss**

- COPY .
- ARG misuse
- ENV misuse
- Secret scanning
- BuildKit secrets
- External secret management

---

## Scenario 9: Development vs Production

### Problem

You need different development and production configurations.

How would you design the Dockerfile?

**Things to Discuss**

- Multi-stage builds
- Build targets
- Build arguments
- Environment variables
- Separate compose files

---

## Scenario 10: Running as Root

### Problem

The application runs as root.

Why is this a security problem?

How would you fix it?

**Things to Discuss**

- USER instruction
- Least privilege
- File ownership
- Attack surface

---

## Scenario 11: Slow Builds

### Problem

Docker image builds take **20 minutes**.

How would you speed them up?

**Things to Discuss**

- Docker cache
- Multi-stage builds
- Smaller base images
- Parallel builds
- BuildKit
- Dependency caching

---

## Scenario 12: Vulnerability Scan

### Problem

A security scan reports critical vulnerabilities.

What steps would you take?

**Things to Discuss**

- Update base image
- Patch packages
- Remove unnecessary tools
- Scan again
- Pin versions
- Distroless images

---

## Scenario 13: Different Ports

### Problem

The application requires different ports in different environments.

How would you handle it?

**Things to Discuss**

- EXPOSE
- Environment variables
- Runtime port mapping
- Reverse proxy

---

## Scenario 14: Missing Logs

### Problem

Nothing appears in `docker logs`.

Why?

**Things to Discuss**

- Logs written to files
- Background processes
- Logging drivers
- stdout
- stderr

---

## Scenario 15: Lost Files

### Problem

The application writes files that disappear after container restart.

Explain why and fix it.

**Things to Discuss**

- Ephemeral containers
- Volumes
- Bind mounts
- Named volumes

---

## Scenario 16: Shared Storage

### Problem

How would you share persistent data between multiple containers?

**Things to Discuss**

- Docker volumes
- Bind mounts
- Shared storage
- NFS
- Kubernetes Persistent Volumes

---

## Scenario 17: Latest Tag

### Problem

Your production image uses `latest`.

Why is that risky?

**Things to Discuss**

- Reproducibility
- Unexpected upgrades
- Rollback difficulty
- Immutable versions

---

## Scenario 18: Failed RUN Instruction

### Problem

A RUN instruction fails during `docker build`.

How would you debug it?

**Things to Discuss**

- Build logs
- Intermediate containers
- Interactive debugging
- Verbose mode

---

## Scenario 19: Cache Invalidation

### Problem

A package installation step keeps invalidating Docker cache.

How do you reorganize the Dockerfile?

**Things to Discuss**

- Copy dependency files first
- Separate application code
- Stable layers

---

## Scenario 20: Monorepo

### Problem

You have a monorepo containing multiple services.

How would you structure Dockerfiles?

**Things to Discuss**

- One Dockerfile per service
- Shared base images
- Build contexts
- Docker Compose

---

## Scenario 21: Multi-Architecture Builds

### Problem

How would you build images for multiple CPU architectures?

**Things to Discuss**

- Buildx
- Multi-platform images
- amd64
- arm64
- QEMU

---

## Scenario 22: Attack Surface

### Problem

How would you reduce the attack surface of a production image?

**Things to Discuss**

- Distroless images
- Non-root user
- Remove package managers
- Minimal packages

---

## Scenario 23: Multi-stage Builds

### Problem

Explain how you would use multi-stage builds for:

- Go
- Java
- Node.js
- Python

**Things to Discuss**

- Build stage
- Runtime stage
- Copy artifacts only
- Smaller final image

---

## Scenario 24: .dockerignore

### Problem

What would you include in a `.dockerignore` file?

Why?

**Things to Discuss**

- .git
- node_modules
- logs
- IDE files
- build artifacts
- secrets
- temporary files

---

## Scenario 25: Build-Time Secrets

### Problem

How do you securely pass secrets during Docker build?

**Things to Discuss**

- BuildKit secrets
- Secret mounts
- Avoid ARG
- Avoid ENV

---

## Scenario 26: Image Verification

### Problem

How do you verify the image contains only the expected files?

**Things to Discuss**

- docker run
- docker exec
- docker image inspect
- Dive
- Syft

---

## Scenario 27: CMD & ENTRYPOINT

### Problem

What happens if both `CMD` and `ENTRYPOINT` are present?

How are runtime arguments handled?

**Things to Discuss**

- Default arguments
- Runtime overrides
- Exec form
- Shell form

---

## Scenario 28: Base Image Selection

### Problem

How would you choose between:

- Alpine
- Debian Slim
- Distroless

Explain the trade-offs.

---

## Scenario 29: Version Pinning

### Problem

How do you pin image versions?

Why is version pinning important?

**Things to Discuss**

- Deterministic builds
- Security
- Rollbacks
- Image digests

---

## Scenario 30: Docker Lifecycle

### Problem

Walk through the complete lifecycle from Dockerfile to a running container.

**Things to Discuss**

- Dockerfile
- Build Context
- Image
- Registry
- Pull
- Run
- Container

---

## Scenario 31: Monitoring

### Problem

What monitoring and health checks would you add for production containers?

**Things to Discuss**

- HEALTHCHECK
- Metrics
- Logging
- Prometheus
- Grafana
- Liveness
- Readiness

---

## Scenario 32: Exec Format Error

### Problem

Your container fails with:

```text
exec format error
```

How would you troubleshoot it?

**Things to Discuss**

- CPU architecture mismatch
- Incorrect ENTRYPOINT
- Missing execute permissions
- Windows line endings

---

## Scenario 33: Permission Denied

### Problem

Your container fails with:

```text
permission denied
```

How would you troubleshoot?

**Things to Discuss**

- USER
- chmod
- chown
- File permissions
- SELinux
- Mount permissions

---

## Scenario 34: Native Dependencies

### Problem

Your application requires native OS dependencies.

How would you package it?

**Things to Discuss**

- Install OS packages
- Multi-stage builds
- Runtime libraries
- Package cleanup

---

## Scenario 35: Zero-Downtime Deployment

### Problem

How would you minimize downtime while deploying a new container version?

**Things to Discuss**

- Rolling updates
- Blue-Green deployment
- Canary deployment
- Health checks
- Readiness probes

---

## Scenario 36: Dockerfile Code Review

### Problem

What Dockerfile best practices do you enforce during code reviews?

**Checklist**

- ✅ Small base image
- ✅ Multi-stage build
- ✅ Non-root user
- ✅ Version pinning
- ✅ Proper layer ordering
- ✅ Efficient caching
- ✅ Minimal dependencies
- ✅ `.dockerignore`
- ✅ No secrets
- ✅ HEALTHCHECK
- ✅ Correct ENTRYPOINT/CMD
- ✅ Image scanning
- ✅ Reproducible builds

---

# 🎯 Interview Preparation Tips

When answering scenario-based questions:

1. **Understand the problem** before jumping to a solution.
2. **Explain your reasoning** step by step.
3. **Mention Docker best practices** where applicable.
4. **Discuss trade-offs** between different approaches.
5. **Relate your answer to production environments** and real-world experience.

---

> **Tip:** Interviewers often value your troubleshooting methodology and decision-making process more than memorizing commands. Think aloud, justify your choices, and consider security, performance, and maintainability in every answer.