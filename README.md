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
- Completed guided training on EC2 storage and network architecture, including EBS volume types, instance store volumes, DNS, and a manual WordPress installation.
- Created an Amazon Machine Image (AMI), launched EC2 instances from the image, and reviewed EC2 purchasing options for workload and cost considerations.
- Configured AWS Certificate Manager DNS validation for the Rich Rome Apparel domain, including `richinrome.com` and `www.richinrome.com`, in preparation for CloudFront HTTPS hosting.
- Configured GitHub Actions with AWS IAM OpenID Connect (OIDC) to automatically deploy website updates to Amazon S3.
- Built and verified a separate GitHub Actions deployment pipeline for the Rich Rome Apparel website using AWS IAM OIDC and a private Amazon S3 bucket.
- Configured `nasirpowell.dev` and `www.nasirpowell.dev` in Amazon Route 53 to route to a CloudFront distribution.
- Configured an AWS Certificate Manager certificate with DNS validation for both resume domains and enabled HTTPS through Amazon CloudFront.
- Added CloudFront origin access to keep the resume's S3 bucket private while serving the site securely.

### Next step

- Continue hands-on AWS CloudFormation learning for repeatable infrastructure deployments.

## Automatic deployments

The GitHub Actions workflow in `.github/workflows/deploy-to-s3.yml` deploys the website to Amazon S3 whenever changes are pushed to the `main` branch, then creates a CloudFront invalidation so visitors receive the newest version. It uses GitHub OpenID Connect (OIDC), which provides temporary AWS access without storing an AWS access key in GitHub.

Before the workflow can run, configure the `AWS_DEPLOY_ROLE_ARN` GitHub Actions secret with the ARN of an AWS IAM role that is limited to deploying this website bucket.

## Current technology

- HTML
- Git and GitHub
- Amazon S3 static website hosting
- Amazon VPC networking: public subnets, route tables, internet and NAT gateways, security groups, network ACLs, and jump hosts (guided training)
- Amazon EC2 access methods and instance types (guided learning)
- Amazon EC2 storage, networking, DNS, and manual WordPress installation (guided training)
- Amazon EC2 AMIs, instance launches, and purchasing options (guided training)
- AWS Certificate Manager DNS validation for a custom domain (Rich Rome Apparel project)
- Amazon CloudFront HTTPS delivery with Amazon Route 53 custom-domain routing (cloud resume)
- AWS CloudFormation (learning in progress)
- GitHub Actions, AWS IAM OIDC, and Amazon S3 automated deployment (Rich Rome Apparel project)
