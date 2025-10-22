# Node.js Jenkins CI/CD Pipeline

This repository demonstrates a simple **CI/CD pipeline** for a Node.js application using **Jenkins**.

## Tech Stack
- Node.js
- Jenkins (CI/CD)
- Docker (optional for deploy steps)

## Overview

This project includes a Jenkins pipeline that automates:

1. **Build**: Runs build commands for the Node.js app  
2. **Test**: Executes basic test steps  
3. **Deploy**: Deploys the app (currently mocked with echo commands)



## How to Run Locally

1. **Clone the repository**
   git clone [https://github.com/git-nxbl/nodejs-jenkins-pipeline.git](https://github.com/git-nxbl/nodejs-jenkins-pipeline.git)
   cd nodejs-jenkins-pipeline

2. **Start Jenkins**

* Make sure Jenkins is installed and running (default URL: [http://localhost:8080](http://localhost:8080))
* Log in and create a new **Pipeline job**
* Under **Pipeline → Definition**, select **Pipeline script from SCM**
* Set:

  * **SCM**: Git
  * **Repository URL**: [https://github.com/git-nxbl/nodejs-jenkins-pipeline.git](https://github.com/git-nxbl/nodejs-jenkins-pipeline.git)
  * **Branch**: main
  * **Script Path**: Jenkinsfile

3. **Run the Pipeline**

* Click **Build Now** in Jenkins
* You should see the pipeline run through these stages:

  * Build
  * Test
  * Deploy
* Each stage prints messages confirming successful execution

## Optional: Automatic GitHub Trigger

* Normally, you could expose Jenkins to the internet (e.g., via ngrok) to trigger builds automatically when pushing to GitHub.
* For this submission, the pipeline is run manually locally.

## Notes

* The pipeline uses echo commands for demonstration. You can replace them with actual build/test/deploy commands later.
* Jenkinsfile is written in declarative syntax for readability and maintainability.

---

