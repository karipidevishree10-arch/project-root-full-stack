In professional software development, code should never be merged or deployed without being tested. Manually running tests before every push is unreliable and error-prone.

Your task is to implement an automated Continuous Integration (CI) pipeline using GitHub Actions so that every push and pull request to the main branch automatically runs both server and client tests.

By completing this assignment, you will ensure that broken code cannot pass unnoticed and that your project follows real-world development practices.

Tasks
You are required to:

Create a GitHub Actions workflow file.
Configure it to run on both push and pull_request to the main branch.
Set up a job that runs on ubuntu-latest.
Install dependencies and run tests for both the server and client.
Verify that the workflow runs successfully.
Demonstrate what happens when a test fails.
Record a short explanation video.
Instructions
Step 1: Create Workflow Directory
Create the required directory from your project root:

mkdir -p .github/workflows
Step 2: Create Workflow File
Create a file named:

.github/workflows/ci.yml
Your workflow must:

Trigger on push to main
Trigger on pull_request to main
Define a job named test
Use ubuntu-latest as the runner
Step 3: Add Required Steps
Your workflow must include the following steps:

Checkout repository using actions/checkout@v3
Setup Node.js 18 using actions/setup-node@v3
Install server dependencies using npm ci
Run server tests using npm test
Install client dependencies using npm ci
Run client tests using npm test
Step 4: Commit and Push
Commit and push your workflow:

git add .github/workflows/ci.yml
git commit -m "Add CI workflow"
git push origin main
Verify that the workflow runs automatically in the Actions tab.

Step 5: Test Failure Scenario
Intentionally break one test.
Push the change.
Verify that the workflow fails (red X).
Fix the test.
Push again and verify that the workflow passes (green check).
Step 6: Test CI on Pull Request
Create a new branch.
Make a small change.
Open a Pull Request to main.
Verify that CI runs on the PR.
Step 7: Record a 3–5 Minute Video
Your video must include:

A brief explanation of what CI is.
Explanation of your workflow file structure.
Explanation of each major step.
What happens when tests fail.
A short demonstration of a successful workflow run.
Note: You do not need Ubuntu installed locally. The ubuntu-latest runner is a cloud-based virtual machine provided by GitHub Actions. You can complete this assignment on Windows, macOS, or Linux.

Rubrics Overview
PR Implementation

Correct workflow file and structure
Proper triggers configured
All required steps implemented
Successful workflow execution
Failure scenario tested
CI verified on pull request
