# cloud-resume

Nasir Powell's AWS cloud resume website, documenting a hands-on journey in cloud architecture, automation, and DevOps.

## Project progress

### Completed

- Created an initial static resume website using HTML.
- Added the professional website title: `Nasir Powell | AWS Cloud Resume`.
- Published the source code to GitHub in the `cloud-resume` repository.
- Created an Amazon S3 bucket and enabled static website hosting.
- Uploaded the resume website and configured public read access for website files.
- Published the first live version at http://nasir-powell-cloud-resume.s3-website-us-east-1.amazonaws.com.
- Completed guided training configuring a multi-tier Amazon VPC with public subnets, route tables, internet and NAT gateways, security groups, network ACLs, and a jump host.
- Completed guided learning on Amazon EC2 access methods, distinguishing SSH from EC2 Instance Connect, and reviewed EC2 instance types for workload needs.
- Configured GitHub Actions with AWS IAM OpenID Connect (OIDC) to automatically deploy website updates to Amazon S3.

### Next step

- Add HTTPS and a custom domain with Amazon CloudFront and Route 53.

## Automatic deployments

The GitHub Actions workflow in `.github/workflows/deploy-to-s3.yml` deploys the website to Amazon S3 whenever changes are pushed to the `main` branch. It uses GitHub OpenID Connect (OIDC), which provides temporary AWS access without storing an AWS access key in GitHub.

Before the workflow can run, configure the `AWS_DEPLOY_ROLE_ARN` GitHub Actions secret with the ARN of an AWS IAM role that is limited to deploying this website bucket.

## Current technology

- HTML
- Git and GitHub
- Amazon S3 static website hosting
- Amazon VPC networking: public subnets, route tables, internet and NAT gateways, security groups, network ACLs, and jump hosts (guided training)
- Amazon EC2 access methods and instance types (guided learning)
