 
# CI/CD Workflows

This repository contains GitHub Actions workflows for linting, testing, building, and deploying a static site. The workflows ensure code quality and automate the deployment process to both AWS and GCP.

## Workflows Overview

### Lint and Test Workflow

This workflow runs on every new pull request to the `develop` branch. It lints the code and runs unit tests to ensure code quality before merging.

### Deploy to AWS Workflow

This workflow runs on every push to the `develop` branch. It builds the static site and deploys it to AWS S3.

### Deploy to GCP Workflow

This workflow runs on every push to the `develop` branch. It builds the static site and deploys it to Google Cloud Storage.

## Branching and Pull Requests

1. **Develop features or updates directly in the `develop` branch.**

2. **Create a pull request (PR) to merge changes from the `develop` branch into the `master` branch.**

3. **Lint and Test Workflow is triggered by the PR to ensure code quality.**

4. **Once the PR is reviewed and approved, merge it into the `master` branch.**

5. **The Deploy to AWS Workflow and Deploy to GCP Workflow are triggered upon merging to build and deploy the static site to the respective cloud platforms.**

## Setting Up Secrets

To securely use sensitive information like AWS and GCP credentials, add the following secrets in your GitHub repository settings:

- `SINDHU_AWS_ACCESS_KEY_ID`: Your AWS Access Key ID.
- `SINDHU_AWS_SECRET_KEY`: Your AWS Secret Access Key.
- `AWS_REGION`: Your AWS region.
- `GCP_KEY`: Your GCP service account key in JSON format.
- `GCP_PROJECT_ID`: Your GCP Project ID.

## Command to Execute

### Lint and Test Workflow

This workflow is automatically triggered on pull requests to the `develop` branch.

### Deploy to AWS Workflow

This workflow is automatically triggered on pushes to the `develop` branch.

### Deploy to GCP Workflow

This workflow is automatically triggered on pushes to the `develop` branch.

## Conclusion

This README provides an overview of the CI/CD workflows implemented using GitHub Actions. It explains the flow of each workflow and how to set up the necessary secrets for secure deployment to AWS and GCP. Additionally, it outlines the branching strategy and the process for creating and merging pull requests to ensure code quality and automated deployment.
 
