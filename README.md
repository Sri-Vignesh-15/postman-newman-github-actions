# API Automation Testing – Postman + Newman + GitHub Actions

## Project Overview
This project demonstrates automated REST API testing using Postman collections executed with Newman. The tests are integrated with GitHub Actions to enable CI/CD and generate detailed HTML reports.

## Tech Stack
- Postman
- Newman
- Node.js & npm
- GitHub Actions
- Newman HTML Extra Reporter

## Project Structure
postman-newman-ci/
├── collections/
│   └── User Flow Automation.postman_collection.json
├── environments/
│   └── MiniEnvironment.postman_environment.json
├── reports/
│   └── report.html
├── package.json
└── .github/
    └── workflows/
        └── newman.yml

## Features
- Automated execution of Postman API tests
- Environment-based testing support
- Live CLI test logs
- HTML report generation
- CI/CD execution using GitHub Actions

## Prerequisites
- Node.js installed
- npm installed

## Install Dependencies
npm install

## Run Tests Locally
npm run test-API

This will run the Postman collection using Newman, display execution results in the terminal, and generate an HTML report inside the reports folder.

## Test Report
After execution, open the report at:
reports/report.html

The report contains request execution details, assertion results, and performance statistics.

## CI/CD Integration
This project uses GitHub Actions to automatically execute API tests on every push and pull request to the main branch.

## npm Test Script Used
"scripts": {
    "test-API": "npx newman run \"collections/User Flow Automation.postman_collection.json\" -e \"environments/MiniEnvironment.postman_environment.json\" -r cli,htmlextra --reporter-htmlextra-export reports/report.html"
  }

## Author
Sri Vignesh Natarajan
