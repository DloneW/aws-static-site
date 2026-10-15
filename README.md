# AWS Static Website

A responsive static website built with HTML, CSS, and JavaScript as a hands-on project for learning AWS infrastructure, Git, and deployment workflows.

## Project Status

**Current stage:** Website built locally and source code pushed to GitHub.

The website has not yet been deployed to AWS. AWS infrastructure and public hosting will be configured and verified in later stages.

## Features

- Responsive layout for desktop and mobile screens
- Mobile navigation menu
- Semantic HTML structure
- Keyboard-accessible navigation controls
- CSS styling with responsive breakpoints
- JavaScript for mobile menu interactions

## Technologies

- HTML5
- CSS3
- JavaScript
- Git and GitHub

## Planned AWS Architecture

The intended deployment architecture is:

1. **Amazon S3:** Store the static website files in a private bucket.
2. **Amazon CloudFront:** Deliver website content over HTTPS.
3. **Origin Access Control (OAC):** Allow CloudFront to access the private S3 origin.
4. **Amazon Route 53:** Route a custom domain to CloudFront.
5. **AWS Certificate Manager (ACM):** Provide the TLS certificate for HTTPS.

These AWS resources are planned, not yet deployed or verified.

## Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/DloneW/aws-static-site.git
   ```

2. Enter the project directory:

   ```bash
   cd aws-static-site
   ```

3. Open `index.html` in a browser.

Alternatively, open the folder in Visual Studio Code and use a local development server.

No package installation or build process is currently required.

## Project Structure

```text
aws-static-site/
├── index.html
├── style.css
├── script.js
├── .gitignore
└── README.md
```

## Learning Objectives

- Understand static website hosting
- Learn how Amazon S3 and CloudFront work together
- Configure a private S3 origin using CloudFront OAC
- Understand DNS routing and HTTPS certificates
- Practise Git version control and deployment workflows
- Recreate validated infrastructure using AWS CloudFormation

## Security Notes

- Keep the S3 bucket private when using CloudFront OAC.
- Do not commit AWS access keys, passwords, private keys, or other secrets.
- Review AWS permissions and estimated costs before creating resources.
- Verify security settings and deployment behaviour rather than assuming they are correct.

## Author

**Dlone**

Cybersecurity student learning cloud infrastructure and secure deployment through practical projects.
