Calculator Application with CI/CD Pipeline
Overview
This is a simple calculator application that supports basic arithmetic operations such as addition, subtraction, and multiplication. The project implements a CI/CD pipeline using Azure DevOps to automate testing, code quality checks, and deployments to Test and Production environments.
Features
• Arithmetic Operations: Addition, Subtraction, Multiplication and Division
• Error Handling: Ensures all inputs are numbers and throws errors for invalid inputs.
• Unit Testing: Tests for correct functionality and error handling using Jest.
• Static Code Analysis: Uses ESLint to enforce coding standards and identify potential issues.
• CI/CD Pipeline: Automated builds, testing, and deployments with approval gates.
Project Structure

Calculator/
├── calculator.js           # Core application logic
├── calculator.test.js      # Unit tests for the application
├── azure-pipelines.yml     # Azure DevOps CI/CD pipeline configuration
├── eslint.config.js        # ESLint configuration for static analysis
├── package.json            # Node.js dependencies and scripts
├── .gitignore              # Excluded files and directories

CI/CD Pipeline
The project is integrated with Azure DevOps for Continuous Integration and Continuous Deployment (CI/CD).
Pipeline Stages
• Build Stage: Installs dependencies (npm install), Runs ESLint for static code analysis, Executes Jest unit tests.
• Deploy to Test: Automatically deploys the application to the Test environment after a successful build.
• Deploy to Production: Requires manual approval before deploying to the Production environment.
How to Run Locally
1. Clone the repository:
   git clone https://github.com/WilliamAkingba Calculator.git
   cd Calculator
2. Install dependencies:
   npm install
3. Run tests:
   npm test
4. Run ESLint:
   npx eslint .
How to Trigger the Pipeline
1. Push Changes:
   Push changes to the development branch to trigger the pipeline and deploy to the Test environment.
   Push changes to the main branch to trigger the pipeline and deploy to Production (after manual approval).
2. Monitor Pipeline:
   Go to Azure DevOps → Pipelines → View the pipeline logs for each stage.
Manual Approval for Production
Deployment to the Production environment requires manual approval to ensure code quality and stability. Approvers can review pipeline logs, commit history, and test results before approving.
Screenshots
• Pipeline Overview: A screenshot of the Azure DevOps pipeline showing all stages (Build, Deploy to Test, and Deploy to Production).
• Successful Test Deployment: Screenshot showing a successful deployment to the Test environment.
• Approval Screen for Production: Screenshot of the manual approval request for the Production environment.
• Successful Production Deployment: Screenshot showing a successful deployment to the Production environment.
• Test Logs: Screenshot of the pipeline logs showing successful execution of unit tests.
Troubleshooting
• Pipeline Fails in Build Stage: Ensure package.json and dependencies are correctly configured. Fix any ESLint errors or warnings.
• Deployment to Test or Production Fails: Check the environment configuration in Azure DevOps. Verify permissions for the pipeline to access environments.
• Manual Approval Issue: Ensure approvers are correctly assigned to the Production environment in Azure DevOps.
Technologies Used
• Node.js: Application runtime.
• Jest: Unit testing framework.
• ESLint: Static code analysis tool.
• Azure DevOps: CI/CD pipeline management.
