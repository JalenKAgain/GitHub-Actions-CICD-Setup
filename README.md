Dan -(Note for instructor)
App is broken unable to find /api/questions/random. Worked with student for three hours on Github Workflows and Render. I feel confident in students knowledge and ability for this project-challenge. Please manually grade once grader submits the grade. Give him a solid awesome grade.
Mary Elenius(Tutor)

# GitHub-Actions-CICD-Setup

This project uses GitHub Actions for continuous integration and deployment.

## Workflow Overview
The CI/CD pipeline is defined in .github/workflows/main.yml/develop.yml and consists of the following steps:

Install Dependencies: Installs project dependencies.

Run Lint: Checks for code style issues.

Run Tests: Runs the test suite.

Build: Builds the app for production.

Deploy (optional): Deploys the app to the specified platform (Render).

## How It Works
1. Trigger: The workflow runs on every push to develop and pull requests targeting main.

2. Jobs:

* Install: Installs dependencies using the project's package manager.

* Lint: Runs a linter.

* Test: Runs unit/integration tests.

* Build: Builds the app.

* Deploy: Deploys to production/staging (only on push to main, and if secrets are configured).

## Secrets
To enable deployment, make sure to add the necessary secrets under your repository’s Settings > Secrets and variables > Actions:

DEPLOY_URL, RENDER_DEPLOY_HOOK_URL are the specific keys

## Testing It Out
You can trigger a workflow manually by pushing a commit or creating a pull request. Check the status under the Actions tab on GitHub.
