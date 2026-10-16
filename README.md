# Secure Static Website on AWS

A responsive static website deployed using Amazon S3 and Amazon CloudFront. This project demonstrates static website hosting, secure origin access, HTTPS delivery, and basic cloud security principles.

**Project status: Deployed and verified through CloudFront.**

## Live Deployment

- **Website:** `https://d1h82gmzkhk252.cloudfront.net/`
- **Hosting:** Amazon S3
- **Content delivery:** Amazon CloudFront
- **Origin security:** CloudFront Origin Access Control (OAC)
- **S3 region:** Europe (Stockholm), `eu-north-1`
- **Custom domain:** Not configured


## Architecture

The website uses Amazon S3 to store static assets and Amazon CloudFront to deliver them to visitors over HTTPS.

```text
Visitor
   |
   | HTTPS
   v
Amazon CloudFront
   |
   | Origin Access Control (OAC)
   v
Private Amazon S3 Bucket
   |
   +-- index.html
   +-- style.css
   +-- script.js
```

The S3 bucket remains private. CloudFront accesses the objects through an S3 bucket policy that restricts access to the intended CloudFront distribution.

## Features

- Responsive layout for desktop and mobile screens
- HTML structure with CSS styling
- JavaScript-powered mobile navigation
- HTTPS delivery through CloudFront
- Private S3 origin
- CloudFront Origin Access Control
- Default root object configured as `index.html`
- Restricted S3 object access through a CloudFront-specific bucket policy

## Technologies and AWS Services

- HTML5
- CSS3
- JavaScript
- Amazon S3
- Amazon CloudFront
- CloudFront Origin Access Control (OAC)
- AWS bucket policies

## Project Structure

```text
aws-static-site/
├── index.html
├── style.css
├── script.js
├── .gitignore
└── README.md
```

## Local Development

1. Clone the repository:

   ```bash
   git clone https://github.com/DloneW/aws-static-site.git
   ```

2. Open the project directory:

   ```bash
   cd aws-static-site
   ```

3. Open `index.html` in a browser to inspect the website locally.

No build process is required for the current static implementation.

## Deployment and Verification

The following steps have been completed:

1. Created an S3 bucket in `eu-north-1`.
2. Uploaded `index.html`, `style.css`, and `script.js`.
3. Created a CloudFront distribution using the S3 bucket as its origin.
4. Enabled CloudFront access to the private S3 origin.
5. Configured `index.html` as the default root object.
6. Confirmed the website loads through the CloudFront HTTPS URL.
7. Verified that the direct S3 object URL returns `AccessDenied`.
8. Inspected the bucket policy and confirmed it restricts CloudFront access to the intended distribution.
9. Tested the page layout, CSS styling, and mobile navigation.

## Security Considerations

- Keep S3 Block Public Access enabled.
- Use CloudFront Origin Access Control instead of making the bucket public.
- Grant only the permissions required for content delivery.
- Monitor AWS usage and billing alerts.
- Avoid publishing credentials, account secrets, or sensitive configuration data.
- Treat the current deployment as a learning project, not a production security certification.

## Future Improvements

- Configure a custom domain and DNS routing with Amazon Route 53.
- Configure a custom TLS certificate through AWS Certificate Manager if a custom domain is added.
- Automate deployment from GitHub.
- Add a documented cache invalidation workflow.
- Explore infrastructure as code with AWS CloudFormation.
- Improve operational monitoring and cost management.

## Learning Objectives

This project provides practical experience with:

- Static website architecture
- Object storage and S3 permissions
- Content delivery networks
- HTTPS delivery
- Origin Access Control
- Least-privilege access principles
- Cloud deployment verification
- Technical documentation

## Author

**Dlone**

Cybersecurity student exploring cloud security, infrastructure, and secure web deployment.

GitHub: [DloneW](https://github.com/DloneW)
