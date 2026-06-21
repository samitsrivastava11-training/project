# ci-cd-final-project

This project demonstrates a complete Cloud-Native CI/CD pipeline implementation using GitHub Actions for Continuous Integration (CI) and Red Hat OpenShift with Tekton for Continuous Deployment (CD).

## Project Details
* **Course Assignment:** ci-cd-final-project
* **Student Name:** Samit Srivastava
* **Date:** [20th June 2026]
* **Target Environment:** Red Hat OpenShift Cluster

---

## Pipeline Architecture

### 1. Continuous Integration (GitHub Actions)
The local integration pipeline is triggered on every `push` and `pull_request` to the main branch. It automates:
* Environment setup (Python / Node.js)
* **Linting:** Code style analysis via `flake8` / `ESLint` to ensure code quality.
* **Unit Testing:** Automated test execution via `pytest` / `Jest` to ensure code stability before deployment.

### 2. Continuous Deployment (Tekton / OpenShift Pipelines)
The cloud deployment pipeline automates the packaging and delivery of the application to OpenShift using:
* **Workspace Cleanup:** A Tekton task ensuring an isolated, clean directory for every run.
* **Testing Task:** Running tests in an isolated cluster container.
* **PersistentVolumeClaims (PVC):** Dynamically allocating storage to share workspaces between Tekton tasks.

---

## Repository Structure

* `.github/workflows/workflow.yml` — GitHub Actions automated CI definition.
* `.tekton/tasks.yml` — Tekton Pipeline custom task definitions (Cleanup & Testing).
* `README.md` — Project layout and structural overview.
# ci-cd-final-project

This project demonstrates a complete Cloud-Native CI/CD pipeline implementation using GitHub Actions for Continuous Integration (CI) and Red Hat OpenShift with Tekton for Continuous Deployment (CD).

## Project Details
* **Course Assignment:** ci-cd-final-project
* **Student Name:** Samit Srivastava
* **Date:** 20 June 2026
* **Target Environment:** Red Hat OpenShift Cluster

---

## Pipeline Architecture

### 1. Continuous Integration (GitHub Actions)
The local integration pipeline is triggered on every `push` and `pull_request` to the main branch. It automates:
* Environment setup (Python / Node.js)
* **Linting:** Code style analysis via `flake8` / `ESLint` to ensure code quality.
* **Unit Testing:** Automated test execution via `pytest` / `Jest` to ensure code stability before deployment.

### 2. Continuous Deployment (Tekton / OpenShift Pipelines)
The cloud deployment pipeline automates the packaging and delivery of the application to OpenShift using:
* **Workspace Cleanup:** A Tekton task ensuring an isolated, clean directory for every run.
* **Testing Task:** Running tests in an isolated cluster container.
* **PersistentVolumeClaims (PVC):** Dynamically allocating storage to share workspaces between Tekton tasks.

---

## Repository Structure

* `.github/workflows/workflow.yml` — GitHub Actions automated CI definition.
* `.tekton/tasks.yml` — Tekton Pipeline custom task definitions (Cleanup & Testing).
* `README.md` — Project layout and structural overview.
