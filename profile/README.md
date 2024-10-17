# Fog Security

Welcome to Fog Security, where we're working to bring clarity to cloud data security.

Check out our resources:

- Fog Security: https://www.fogsecurity.io
- Fog Security Technical Blog: https://www.fogsecurity.io/blog/
- Contact: info@fogsecurity.io

## Encryption in AWS Tooling

We've created the following resources to help with understanding encryption and improving cloud security.

### AWS Default Encryption Tracker

This repository tracks default encryption settings across AWS resources.  In our research of 50+ resources across 40+ AWS services, resources were found to either be unencrypted, default encrypted with AWS owned keys, or default encrypted with AWS managed keys.  

Read more in our blog post here: https://www.fogsecurity.io/blog/are-my-aws-resources-encrypted-or-unencrypted-by-default \
Repository: https://github.com/FogSecurity/aws-default-encryption-tracker

### AWS Managed Keys Tracker

This tool checks which AWS Services support AWS Managed Keys, a type of KMS Encryption Key where the encryption key is managed by AWS, but exists only within the customer AWS Account.  Additionally, the tool pulls the managed key policies and uploads them to a repository for reference.

Read more in our blog post here: https://www.fogsecurity.io/blog/encryption-aws-managed-kms-keys \
Repository: https://github.com/FogSecurity/aws-managed-kms-keys
 
### IAM References for AWS KMS Encryption

Currently, this repository covers how to update encryption for existing AWS resources.  This is helpful to help prevent against ransomware, as a cloud ransomware technique is to hold data hostage by changing encryption keys.  This also aids in teams who need to update or manage encryption for existing AWS resources.  This repository details the IAM actions required to update encryption for cloud resources that support encryption update and details which cloud resources do not support updating in place and thus need to be recreated.

Read more in our blog post here: https://www.fogsecurity.io/blog/updating-encryption-aws-resources-ransonware \
Repository: https://github.com/FogSecurity/aws-kms-encryption-iam/blob/main/README.md
