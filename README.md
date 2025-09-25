# Day 1: Hello DevOps CI/CD Pipeline

A simple DevOps CI/CD pipeline using Docker and Jenkins to build and run a Python Flask app.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Value Highlight](#value-highlight)
4. [Folder Structure](#folder-structure)
5. [Setup & Installation](#setup--installation)
6. [Running the App](#running-the-app)
7. [CI/CD Pipeline (Jenkins)](#cicd-pipeline-jenkins)
8. [Screenshots](#screenshots)
9. [Architecture Diagram](#architecture-diagram)
10. [Notes / Challenges Solved](#notes--challenges-solved)

## Project Overview
This project is a simple Flask web application, dockerized and deployed using a Jenkins CI/CD pipeline. Whenever code is pushed to GitHub, Jenkins automatically builds the Docker image and runs the container, demonstrating an end-to-end DevOps workflow from code commit to deployment.

## Technologies Used
- **Git & GitHub** – Version control & code hosting  
- **Jenkins** – CI/CD automation  
- **Docker** – Containerization  
- **Python (Flask)** – Lightweight web application

## Value Highlight
Demonstrates automated CI/CD workflow, integrating code commits, build, and deployment using industry-standard DevOps tools.

## Folder Structure
Day-1/ 
├── app.py 
├── Dockerfile  
├── Jenkinsfile  
├── requirements.txt  
└── README.md  


## Setup & Installation
1. **Clone the repository**  
```
git clone https://github.com/yourusername/day-1.git
cd day-1
```

2. **Build Docker image**
```
docker build -t day-1-app
```

3. **Running the App**
```
docker run -d -p 5000:5000 day-1-app
```

4. **Open browser at:**
```
http://localhost:5000
```

## Screenshots:
(To be added: terminal outputs, Jenkins pipeline, app running in browser)

## Architecture Diagram:
(To be added: DevOps workflow diagram)

## Notes / Challenges Solved:
Configured Jenkins to build and deploy Docker container automatically

Learned to resolve Docker login issues with Docker Hub using Personal Access Token

Ensured CI/CD pipeline runs successfully on code commit.
