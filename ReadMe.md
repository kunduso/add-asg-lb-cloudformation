[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-white.svg)](https://choosealicense.com/licenses/unlicense/) [![GitHub pull-requests closed](https://img.shields.io/github/issues-pr-closed/kunduso/add-asg-lb-cloudformation)](https://github.com/kunduso/add-asg-lb-cloudformation/pulls?q=is%3Apr+is%3Aclosed) [![GitHub pull-requests](https://img.shields.io/github/issues-pr/kunduso/add-asg-lb-cloudformation)](https://GitHub.com/kunduso/add-asg-lb-cloudformation/pull/) 
[![GitHub issues-closed](https://img.shields.io/github/issues-closed/kunduso/add-asg-lb-cloudformation)](https://github.com/kunduso/add-asg-lb-cloudformation/issues?q=is%3Aissue+is%3Aclosed) [![GitHub issues](https://img.shields.io/github/issues/kunduso/add-asg-lb-cloudformation)](https://GitHub.com/kunduso/add-asg-lb-cloudformation/issues/) [![deploy-cloudformation](https://github.com/kunduso/add-asg-lb-cloudformation/actions/workflows/deploy-cfn.yml/badge.svg?branch=main)](https://github.com/kunduso/add-asg-lb-cloudformation/actions/workflows/deploy-cfn.yml) [![checkov-static-analysis-scan](https://github.com/kunduso/add-asg-lb-cloudformation/actions/workflows/code-scan.yml/badge.svg?branch=main)](https://github.com/kunduso/add-asg-lb-cloudformation/actions/workflows/code-scan.yml)
# AWS Infrastructure Deployment with CloudFormation and GitHub Actions
![Image](https://skdevops.files.wordpress.com/2024/05/93-image-0.png)

This repository contains the necessary files and configurations to deploy AWS infrastructure resources using CloudFormation templates and automate the deployment process with GitHub Actions. For a detailed walkthrough on using AWS CloudFormation with GitHub Actions please check [automating-aws-infrastructure-with-cloudformation-and-github-actions.](https://skundunotes.com/2024/05/24/automating-aws-infrastructure-with-cloudformation-and-github-actions-a-tutorial/)

## Repository Structure

- `templates/`: This folder contains the CloudFormation templates in YAML or JSON format, which define the AWS resources to be created.
- `parameters/`: This folder includes parameter files in JSON format, which provide input values for the CloudFormation templates.
- `.github/workflows/`: This folder contains the GitHub Actions workflow files (e.g., `deploy-cfn.yml`) that automate the deployment process.
- `iam_policy/`: This folder stores the necessary IAM permission policies and configurations required for the deployment process.

## Prerequisites

Before using this repository, ensure you have the following:

1. An AWS account with appropriate permissions to create and manage resources.
2. AWS CLI installed and configured on your local machine or the GitHub Actions runner.
3. GitHub account and a new or existing repository to store the code.
4. Create two AWS IAM roles with trust and permission policies
5. AWS Secrets (e.g., IAM Role ARNs) stored as GitHub Repository Secrets for authentication and access during the deployment process.

## Usage

1. Clone this repository to your local machine or create a new repository and copy the contents.
2. Navigate to the `iam_policy/` folder and update the necessary IAM policies with the appropriate ARNs and configurations for your AWS account.
3. Store the required IAM Role ARNs as GitHub Repository Secrets (e.g., `IAM_ROLE`, `CFN_ROLE`).
4. Customize the CloudFormation templates in the `templates/` folder based on your infrastructure requirements.
5. Update the parameter files in the `parameters/` folder with the desired input values for your templates.
6. Commit and push your changes to the GitHub repository.
7. The GitHub Actions workflow in `.github/workflows/deploy-cfn.yml` will automatically trigger and deploy the CloudFormation stacks based on the templates and parameters provided.

## Contribution

If you find any issues or have suggestions for improvement, please feel free to open an issue or submit a pull request. Contributions are always welcome!

## License
This code is released under the Unlincse License. See [LICENSE](LICENSE).
