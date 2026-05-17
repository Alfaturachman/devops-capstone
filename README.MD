# Customer Accounts Microservice — IBM DevOps Capstone Project

[![Build Status](https://github.com/nikeshkumar/devops-capstone/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/nikeshkumar/devops-capstone/actions/workflows/ci-build.yaml)
[![Python Version](https://img.shields.io/badge/python-3.9%20%7C%203.10-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/framework-Flask-red.svg)](https://flask.palletsprojects.com/)
[![Docker](https://img.shields.io/badge/container-Docker-blue.svg)](https://www.docker.com/)
[![Kubernetes](https://img.shields.io/badge/orchestration-Kubernetes-blue.svg)](https://kubernetes.io/)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-Tekton%20%26%20GitHub%20Actions-orange.svg)](https://tekton.dev/)
[![Security](https://img.shields.io/badge/security-Talisman%20%26%20CORS-green.svg)](https://github.com/thoughtworks/talisman)

This repository contains the final Capstone Project for the **IBM DevOps and Software Engineering Professional Certificate**. The project implements a secure, containerized, and automated **Customer Accounts Microservice** using modern DevOps practices, Agile methodology, CI/CD pipelines, and cloud-native deployments.

---

## Project Overview

The **Customer Accounts Microservice** is a RESTful API designed to manage customer details and account data. Over the course of three sprints, the application was moved from a basic Python Flask template to a fully containerized, securely configured, and automatically deployed microservice.

### Key DevOps Capabilities Demonstrated:

- **Agile Project Management**: Managed user stories, estimated points, and tracked progress across multiple sprints using a visual Kanban Board on GitHub.
- **RESTful API Development**: Implemented full CRUD functionality with standard Python testing and linting configuration.
- **Continuous Integration (CI)**: Integrated automated checking, linting (`Flake8`, `Pylint`), security checks (`Talisman`), and unit tests (`nosetests`) using GitHub Actions.
- **Application Security**: Configured CORS policies and Talisman security headers to protect against cross-site scripting (XSS) and injection attacks.
- **Containerization**: Maintained high-efficiency Docker configurations for building clean application containers.
- **Orchestration & Cloud Deployment**: Deployed and scaled the microservice in a Kubernetes/OpenShift environment, managing Pods, Deployments, ReplicaSets, and Services.
- **Continuous Delivery (CD)**: Automated builds and zero-downtime deployment pipelines using Tekton.

---

## Technology Stack

- **Backend**: Python, Flask, Flask-RESTful, SQLAlchemy
- **Testing & Quality**: Nosetests, Coverage, Flake8, Pylint
- **Security**: Talisman, CORS policies
- **CI/CD**: GitHub Actions, Tekton Pipelines
- **Containers & Orchestration**: Docker, Kubernetes, Red Hat OpenShift

---

## API Reference & cURL Commands

The service provides standard RESTful endpoints for managing customer accounts.

| HTTP Method | Endpoint         | Description                         | Sample cURL Command                                                                                                                    |
| :---------- | :--------------- | :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| **POST**    | `/accounts`      | Create a new customer account       | `curl -X POST -H "Content-Type: application/json" -d '{"name":"John Doe", "email":"john@example.com"}' http://localhost:8080/accounts` |
| **GET**     | `/accounts`      | List all customer accounts          | `curl -X GET http://localhost:8080/accounts`                                                                                           |
| **GET**     | `/accounts/<id>` | Read a specific customer account    | `curl -X GET http://localhost:8080/accounts/1`                                                                                         |
| **PUT**     | `/accounts/<id>` | Update an existing customer account | `curl -X PUT -H "Content-Type: application/json" -d '{"name":"John Smith"}' http://localhost:8080/accounts/1`                          |
| **DELETE**  | `/accounts/<id>` | Delete a customer account           | `curl -X DELETE http://localhost:8080/accounts/1`                                                                                      |

---

## Agile Planning & Kanban Stages

The project lifecycle is organized into three progressive sprints, documented step-by-step:

### Sprint 1: Project Setup & Core API

- Initialize GitHub repository, draft project requirements, and configure templates.
- Define Core User Stories in a visual Kanban Board (New Issues -> Ice Box -> Sprint Backlog).
- Create configuration files for styling, linting, and testing (`setup.cfg`).
- Develop core RESTful endpoints (Create, Read, Update, Delete, List) for Customer Accounts.

### Sprint 2: CI Automation & Security Headers

- Implement CI workflow using GitHub Actions (`ci-build.yaml`).
- Incorporate Talisman pre-commit security analysis and HTTP security headers.
- Apply CORS rules to secure API access and check code styling with Flake8/Pylint.

### Sprint 3: Containerization, Kubernetes & CD

- Write a multi-stage, high-performance `Dockerfile`.
- Deploy the containerized service locally and test the JSON response on port `8080`.
- Deploy resources to Kubernetes/OpenShift (Deployments, Pods, Services, and ReplicaSets).
- Automate deployment pipelines from source to active cluster using Tekton.

---

## Submission Evidence & Artifacts

To make the evaluation process seamless, the complete checklist and all required artifacts for both **AI-Graded (Option 1)** and **Peer-Graded (Option 2)** tracks are structured below.

---

### Option 1: AI-Graded Submission Checklist

<details>
<summary><b>Click to expand the AI-Graded Checklist (Tasks 1 - 33)</b></summary>

Here are the direct links, text files, and images required to verify the successful automated execution of all capstone tasks:

#### Group A: Public GitHub URLs (8 Points)

- [ ] **Task 1: GitHub README URL (2 pts)** — [Link to README.MD](README.MD) (This file containing the updated Build Status badge).
- [ ] **Task 2: User Story Template URL (1 pt)** — [Link to user-story.md](user-story.md) (Contains the user story template).
- [ ] **Task 7: Test Config URL (1 pt)** — [Link to setup.cfg](setup.cfg) (Contains nosetests, coverage, Flake8, and Pylint configurations).
- [ ] **Task 21: CI Workflow YAML URL (4 pts)** — [Link to ci-build.yaml](.github/workflows/ci-build.yaml) (GitHub Actions workflow configurations).
- [ ] **Task 22: Talisman Init URL (1 pt)** — [Link to **init**.py](service/__init__.py) (Talisman security headers configuration).
- [ ] **Task 29: Dockerfile URL (2 pts)** — [Link to Dockerfile](Dockerfile) (Complete Docker configurations).

---

#### Group B: Kanban Board & Story Tracking Screenshots (13 Points)

- [ ] **Task 3: Sprint 1 User Stories (1 pt)** — `planning-userstories-done.png` showing all user stories listed in _New Issues_.
- [ ] **Task 4: Ice Box Status (1 pt)** — `planning-productbacklog-done.png` showing stories listed under the _Ice Box_.
- [ ] **Task 5: Technical Debt / Enhancements (1 pt)** — `planning-labels-done.png` showing stories labeled correctly.
- [ ] **Task 6: Sprint Backlog (1 pt)** — `planning-kanban-done.png` showing stories estimated and assigned to Sprint 1.
- [ ] **Task 8: Dev Env Setup Done (1 pt)** — `rest-techdebt-done.png` showing "Setting up the development environment" in _Done_.
- [ ] **Task 9: Read Account Done (1 pt)** — `read-accounts.png` showing "Read an account from the service" in _Done_.
- [ ] **Task 10: List Accounts Done (1 pt)** — `list-accounts.png` showing "List all accounts in the service" in _Done_.
- [ ] **Task 11: Update Account Done (1 pt)** — `update-accounts.png` showing "Update an account in the service" in _Done_.
- [ ] **Task 12: Delete Account Done (1 pt)** — `delete-accounts.png` showing "Delete an account from the service" in _Done_.
- [ ] **Task 18: Sprint 2 Planning (1 pt)** — `sprint2-plan.png` showing the two new Sprint 2 stories in the _Sprint Backlog_.
- [ ] **Task 20: CI Automation Done (1 pt)** — `ci-kanban-done.png` showing "Need the ability to automate continuous integration checks" in _Done_.
- [ ] **Task 24: Security Story Done (1 pt)** — `security-kanban-done.png` showing "Need to add security headers and CORS policies" in _Done_.
- [ ] **Task 25: Sprint 3 Planning (1 pt)** — `sprint3-plan.png` showing the three user stories added to _Sprint 3_.
- [ ] **Task 27: Docker Containerization Done (1 pt)** — `kube-docker-done.png` showing "Containerize your microservice using Docker" in _Done_.
- [ ] **Task 28: Kubernetes Deployment Done (1 pt)** — `kube-kubernetes-done.png` showing "Deploy your Docker image to Kubernetes" in _Done_.
- [ ] **Task 33: CD Pipeline Done (1 pt)** — `cd-pipeline-done.png` showing the Tekton CD Pipeline story in _Done_.

---

#### Group C: Command Logs, Outputs & Artifacts (29 Points)

- [ ] **Task 13: Account CREATE API Output (2 pts)** — [rest-create-done](rest-create-done) (cURL command demonstrating account creation).
- [ ] **Task 14: Account LIST API Output (2 pts)** — [rest-list-done](rest-list-done) (cURL command listing all accounts).
- [ ] **Task 15: Account READ API Output (2 pts)** — [rest-read-done](rest-read-done) (cURL command reading a specific account).
- [ ] **Task 16: Account UPDATE API Output (2 pts)** — [rest-update-done](rest-update-done) (cURL command updating an account).
- [ ] **Task 17: Account DELETE API Output (2 pts)** — [rest-delete-done](rest-delete-done) (cURL command deleting an account).
- [ ] **Task 19: CI Actions Execution Log (2 pts)** — [ci-workflow-done](ci-workflow-done) (Logs verifying all GitHub Actions CI checks passed).
- [ ] **Task 23: Security CORS Nose Tests (1 pt)** — [security-headers-done](security-headers-done) (Nosetests showing all tests passing with CORS).
- [ ] **Task 26: Microservice Port 8080 Launch (1 pt)** — [kube-app-output](kube-app-output) (JSON response generated upon successful launch).
- [ ] **Task 30: Docker Images Info (2 pts)** — [kube-images](kube-images) (Output showing Name, Tag, Image ID, Created, and Size).
- [ ] **Task 31: Kubernetes Deployment Details (2 pts)** — [kube-deploy-accounts](kube-deploy-accounts) (Deployments, Pods, ReplicaSets, and Services detail logs).
- [ ] **Task 32: Tekton Pipeline Logs (5 pts)** — [pipelinerun.txt](pipelinerun.txt) (Complete build/deployment execution logs).

</details>

---

### Option 2: Peer-Graded Submission Checklist

<details>
<summary><b>Click to expand the Peer-Graded Checklist (Tasks 1 - 5)</b></summary>

For peer evaluators reviewing the manual track, use the checklist below to easily cross-reference the corresponding screenshots and deliverables:

#### Phase 1: Planning & Agile (6 Points)

- [ ] **Task 1 a**: `planning-repository-done.jpg` — Verification of repository created successfully. (1 pt)
- [ ] **Task 1 b**: `planning-storytemplate-done.jpg` — User story template file `user-story.md` added. (1 pt)
- [ ] **Task 1 c**: `planning-userstories-done.jpg` — Stories displayed in the _New Issues_ column. (1 pt)
- [ ] **Task 1 d**: `planning-productbacklog-done.jpg` — Stories moved and listed under _Ice Box_. (1 pt)
- [ ] **Task 1 e**: `planning-labels-done.jpg` — Enhancement & Technical Debt tags applied. (1 pt)
- [ ] **Task 1 f**: `planning-kanban-done.jpg` — Sprint Backlog contains active Sprint 1 estimates and assignments. (1 pt)

#### Phase 2: REST APIs & Development (12 Points)

- [ ] **Task 2 a**: `rest-setupcfg-done.jpg` — The `setup.cfg` file featuring testing/linting configurations. (1 pt)
- [ ] **Task 2 b**: `rest-techdebt-done.jpg` — Setting up development environment story moved to _Done_. (1 pt)
- [ ] **Task 2 c**: `read-accounts.jpg` — "Read an account" story moved to _Done_. (1 pt)
- [ ] **Task 2 d**: `list-accounts.jpg` — "List accounts" story moved to _Done_. (1 pt)
- [ ] **Task 2 e**: `update-accounts.jpg` — "Update account" story moved to _Done_. (1 pt)
- [ ] **Task 2 f**: `delete-accounts.jpg` — "Delete account" story moved to _Done_. (1 pt)
- [ ] **Task 2 g**: `rest-create-done.jpg` — cURL request & response demonstrating the `CREATE` API. (2 pts)
- [ ] **Task 2 h**: `rest-read-done.jpg` — cURL request & response demonstrating the `READ` API. (2 pts)
- [ ] **Task 2 i**: `rest-list-done.jpg` — cURL request & response demonstrating the `LIST` API. (2 pts)
- [ ] **Task 2 j**: `rest-update-done.jpg` — cURL request & response demonstrating the `UPDATE` API. (2 pts)
- [ ] **Task 2 k**: `rest-delete-done.jpg` — cURL request & response demonstrating the `DELETE` API. (2 pts)

#### Phase 3: CI Pipelines & Security Headers (9 Points)

- [ ] **Task 3 a**: `sprint2-plan.jpg` — Two Sprint 2 user stories assigned to _Sprint Backlog_. (1 pt)
- [ ] **Task 3 b**: `ci-workflow-done.jpg` — Successful execution log/run in GitHub Actions. (2 pts)
- [ ] **Task 3 c**: `ci-badge-done.jpg` — Build status badge actively rendering in the README header. (1 pt)
- [ ] **Task 3 d**: `ci-kanban-done.jpg` — CI automation story successfully moved to _Done_. (1 pt)
- [ ] **Task 3 e**: [ci-build.yaml URL](.github/workflows/ci-build.yaml) — Link to CI configurations. (4 pts)
- [ ] **Task 3 i**: `security-code-done.jpg` — Talisman initialization and CORS middleware setup in the code. (1 pt)
- [ ] **Task 3 j**: `security-headers-done.jpg` — Headers verify command showing CORS policy in action. (1 pt)
- [ ] **Task 3 k**: `security-kanban-done.jpg` — Security story successfully moved to _Done_. (1 pt)

#### Phase 4: Kubernetes & Containerization (10 Points)

- [ ] **Task 4 a**: `sprint3-plan.jpg` — Three Sprint 3 user stories assigned to _Sprint Backlog_. (1 pt)
- [ ] **Task 4 b**: `kube-app-output.jpg` — Successful launch page displaying JSON format. (1 pt)
- [ ] **Task 4 c**: `kube-docker-done.jpg` — Containerization story moved to _Done_. (1 pt)
- [ ] **Task 4 d**: [Dockerfile URL](Dockerfile) — Link to Docker containerization script. (2 pts)
- [ ] **Task 4 e**: `kube-images.jpg` — Active Docker build image list output. (2 pts)
- [ ] **Task 4 f**: `kube-deploy-accounts.jpg` — Deployed Pods, Services, and ReplicaSets in target namespaces. (2 pts)
- [ ] **Task 4 g**: `kube-kubernetes-done.jpg` — Deploying Docker image to Kubernetes story moved to _Done_. (1 pt)

#### Phase 5: Continuous Delivery Pipelines (6 Points)

- [ ] **Task 5 a**: [pipelinerun.txt](pipelinerun.txt) — Log verifying successful Tekton Pipeline runs. (5 pts)
- [ ] **Task 5 b**: `cd-pipeline-done.jpg` — CD pipeline automation story moved to _Done_. (1 pt)

</details>

---

## Author(s)

- **Nikesh Kumar** — _Lead Developer & DevOps Engineer_

---

_Thank you for reviewing this Capstone Project! If you find it helpful, please consider giving it a star!_
