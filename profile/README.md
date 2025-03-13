# Fog Security

Welcome to Fog Security, where we're working to prevent ransomware, bring clarity to cloud encryption, and build better data perimeters.

- Fog Security: https://www.fogsecurity.io
- Fog Security Technical Blog: https://www.fogsecurity.io/blog/
- Contact: info@fogsecurity.io

Resources:

- [Finders Keypers (AWS KMS Key Usage Finder)](#finders-keypers)
- [AWS Default Encryption Tracker](#aws-default-encryption-tracker)
- [IAM References for AWS Data Perimeters](#iam-references-for-aws-data-perimeters)
  - [Ransomware Prevention in AWS for S3 and KMS](#ransomware-prevention-in-aws-for-s3-and-kms)
  - [IAM Actions to update encryption for existing AWS resources](#iam-actions-to-update-encryption-for-existing-aws-resources)
  - [Organizational Resource Control Policies (RCPs) and Service Control Policies (SCPs) for AWS](#organizational-RCPs-and-SCPs)
- [AWS IAM Tagging](#aws-iam-tagging)
- [AWS Managed Keys Tracker](#AWS-Managed-Keys-Tracker)



### Finders Keypers

This open source CLI python tool helps determine blast radius and usage of AWS KMS Keys.  Currently, this is difficult to do and requires custom tooling or incomplete searches through CloudTrail and IAM references in KMS key policies and KMS key grants.  Finders Keypers is a tool built that checks service resources via boto3 API calls to better understand current usage of KMS keys for encryption.

Read more in our blog post here: https://www.fogsecurity.io/blog/introducing-finders-keypers-a-tool-to-discover-usage-and-blast-radius-of-encryption-keys-in-aws \
Repository: https://github.com/FogSecurity/finders-keypers


### AWS Default Encryption Tracker

This repository tracks default encryption settings across AWS resources.  In our research of 50+ resources across 40+ AWS services, resources were found to either be unencrypted, default encrypted with AWS owned keys, or default encrypted with AWS managed keys.  

Read more in our blog post here: https://www.fogsecurity.io/blog/are-my-aws-resources-encrypted-or-unencrypted-by-default \
Repository: https://github.com/FogSecurity/aws-default-encryption-tracker

### AWS IAM Tagging

This repository contains listings of:
* All 1000+ IAM Actions to tag resources in AWS
* Listing of 1400+ AWS Resources that support tagging.

Repository: https://github.com/FogSecurity/aws-iam-tagging

### IAM References for AWS Data Perimeters

This repository contains multiple IAM references including:

#### Ransomware Prevention in AWS for S3 and KMS
These reference policies (including SCPs, RCPs, Bucket Policies, and more) help with preventing ransomware in Amazon S3 and KMS.  These include policies to prevent against data access, data deletion, and data corruption (such as encryption with SSE-C, customer-provided encryption)

#### Organizational RCPs and SCPs
These reference Resource Control Policies (RCPs) and Service Control Policies (SCPs) help with creating data perimeters and improving cloud security within your AWS Organization at scale.  These policies protect resources and can also limit potential actions taken by IAM principals within your AWS Organization and AWS accounts within.
  
#### IAM Actions to update encryption for existing AWS resources
This is helpful to help prevent against ransomware, as a cloud ransomware technique is to hold data hostage by changing encryption keys.  This also aids in teams who need to update or manage encryption for existing AWS resources.  This repository details the IAM actions required to update encryption for cloud resources that support encryption update and details which cloud resources do not support updating in place and thus need to be recreated.

Read more in our blog posts here: 
* https://www.fogsecurity.io/blog/updating-encryption-aws-resources-ransonware 
* https://www.fogsecurity.io/blog/data-perimeters-with-resource-control-policies-and-aws-kms
* https://www.fogsecurity.io/blog/the-complete-guide-to-ransomware-protection-in-s3-and-kms

Repository: [https://github.com/FogSecurity/aws-data-perimeter-iam](https://github.com/FogSecurity/aws-data-perimeter-iam)

### AWS Managed Keys Tracker

This tool checks which AWS Services support AWS Managed Keys, a type of KMS Encryption Key where the encryption key is managed by AWS, but exists only within the customer AWS Account.  Additionally, the tool pulls the managed key policies and uploads them to a repository for reference.

Read more in our blog post here: https://www.fogsecurity.io/blog/encryption-aws-managed-kms-keys \
Repository: https://github.com/FogSecurity/aws-managed-kms-keys

