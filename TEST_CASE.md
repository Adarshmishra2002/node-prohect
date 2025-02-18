# TEST CASES - CI/CD Pipelines with Jenkins

**Submitted By**  
Adarsh Mishra

**Submitted To**  
Vipin Tripathi

**Test Case Version**  
1

**Reviewer Name**  
Manmeet Narang

## Goal
I need to pull a Node.js project from GitHub, and then create a Dockerfile for it. After that, I need to build an image using that Dockerfile with Podman and then create a container from that image. Once the container is running, I will check it in the browser.

Next, I will write a shell script to automate this entire process. After that, I need to set up a Podman registry and push my project’s image into it. Then, I will configure GitHub and Jenkins to trigger a webhook for this process. Later, I will set up the same webhook trigger using Gitea instead of GitHub. Finally, I will create containers for Gitea and Jenkins, ensuring the webhook trigger works correctly.

## Table of Contents
- Test Environment
- TC1: Verify Webhook Trigger
- TC2: Check if the Jenkins Job Runs Successfully
- TC3: Check Build Logs in Jenkins
- TC4: Check Post-Build Actions
- TC5: Check Error Handling in Jenkins

## Test Environment
- Ubuntu 24.04
- Git, Podman, Node.js, npm pre-installed
- Gitea, ngrok, and Jenkins configured

---

### TC1: Verify Webhook Trigger

**Scenario**  
Verify that the Jenkins webhook is triggered when a commit is pushed to the Gitea repository.

**Given**  
A Gitea repository is linked with Jenkins, and a Jenkins job is active.

**When**  
A user pushes a new commit to the Gitea repository.

**Then**  
The Jenkins webhook will start, and the job will begin running.

**Test Run**  
Date: (To be filled)  
Result: Pending / Pass / Fail  
Testing outputs: (Paste your output/snapshots here)

---

### TC2: Check if the Jenkins Job Runs Successfully

**Scenario**  
Confirm that Jenkins runs the job after a webhook trigger, considering different types of commits.

**Given**  
Jenkins is set to run a job when the webhook is triggered.

**When**  
A new commit is pushed to Gitea.

- **Variation 1:** A new file is added to the repository.
- **Variation 2:** An existing file is modified.
- **Variation 3:** A file is deleted from the repository.

**Then**  
The Jenkins job will start and complete successfully for all cases.

**Test Run**  
Date: (To be filled)  
Result: Pending / Pass / Fail  
Testing outputs: (Paste your output/snapshots here)

---

### TC3: Check Build Logs in Jenkins

**Scenario**  
Confirm that Jenkins logs all steps of the build process.

**Given**  
Jenkins is set to log everything when a job runs.

**When**  
A build starts in Jenkins.

**Then**  
The build logs will be visible and show each step of the build.

**Test Run**  
Date: (To be filled)  
Result: Pending / Pass / Fail  
Testing outputs: (Paste your output/snapshots here)

---

### TC4: Check Post-Build Actions

**Scenario**  
Confirm that all post-build steps run correctly.

**Given**  
Jenkins job has post-build actions (e.g., send notification, deploy).

**When**  
The job is completed successfully.

**Then**  
All post-build steps will run without errors.

**Test Run**  
Date: (To be filled)  
Result: Pending / Pass / Fail  
Testing outputs: (Paste your output/snapshots here)

---

### TC5: Check Error Handling in Jenkins

**Scenario**  
Confirm that Jenkins shows errors when the build fails due to different failure points.

**Given**  
Jenkins is set to catch and show errors.

**When**  
The Jenkins job fails due to an error.

- **Scenario 1:** Webhook trigger failure (e.g., incorrect URL, authentication issue).
- **Scenario 2:** Container fails to start after build.
- **Scenario 3:** Podman image build fails (e.g., missing dependencies, incorrect Dockerfile).

**Then**  
Jenkins will show an appropriate error message in the logs for each case.

**Test Run**  
Date: (To be filled)  
Result: Pending / Pass / Fail  
Testing outputs: (Paste your output/snapshots here)
