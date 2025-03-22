# 🚀 Project Overview

This project automates the DevOps lifecycle for Abode Software’s product using GitHub, Docker, Jenkins, and Ansible.

GitHub Repo: [Abode Software Project](https://github.com/hshar/website.git )

**📦 1. Configuration Management Setup (Ansible)**
- Install Docker, Jenkins, Git, AWS CLI, and dependencies.

- Configure Docker and Jenkins services.

- Clone GitHub repo and copy the application to /var/www/html.

   - **Playbook Location:** [ansible/play.yml](https://github.com/)

**🔀 2. Git Workflow Implementation**
- Create branches:

   - master → Push to production after testing.

   - develop → Run tests only, no deployment.

- Protect master branch to restrict direct commits.

**🔥 3. CodeBuild Trigger Configuration**
- Configure GitHub Webhooks to trigger Jenkins pipeline:

   - Push to master → Build, test, and deploy.

   - Push to develop → Build and test only.

**🐳 4. Docker Containerization**
- Create a Dockerfile to use a pre-built container:

   - **Dockerfile Location:** [Dockerfile](https://github.com/)

- Build and push Docker image after every commit.

**📝 5. Jenkins Pipeline with 3 Jobs**

- Job 1: Build: Pull code, build Docker image, and push to DockerHub.

- Job 2: Test: Run unit tests using Docker.

- Job 3: Prod: Deploy to production on master commit.

**🎯 7. How to Run the Project**
- Clone the repository:
  
   - git clone https://github.com/hshar/website.git
   
- Run the Ansible playbook:
  
   - ansible-playbook ansible/playbook.yml
     
- Configure Jenkins Webhook for GitHub.

- Push code to master or develop to trigger the pipeline.


