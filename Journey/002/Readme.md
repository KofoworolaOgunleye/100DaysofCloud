
# IAM and Linux

## Introduction

Identity Access Management (IAM) securely controls who can access resources (Authentification) and what resources users can access (Authorization). For example, an IAM user with only S3FullAccess permissions cannot spin up EC2 servers or use any other services in the account.

IAM users can be people, services or applications.


## Use Case

*Root account shouldn't be used to access your account unless it is absolutely neccessary, IAM users with the right permissions should be used instead.
*Enable MFA for all accounts 
*Never put your credentials in code
• Rotate credentials
• Grant least priviledge; deny all access and allow as needs arises
• Use IAM Roles to provide cross-account access.
• Multiple users with the same policy should be in a group


## Cloud Research

• [AWS Identity and Access Management
User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)


## Try yourself

• Create an Account Alias that will be used as Sign-in url for users
• Create a user with AdministratorAccess, use this instead of your Root Account to log into your AWS console
• Create a user with only S3Full Access and try to use other services
• Create multiple users and assign them to a group e.g DevOps group
• Enable MFA by downloading authenticator, I use LastPass Authenticator app on my phone


## LINUX
I learnt some basic linux commands, did some practice on [kodekloud](https://kodekloud.com/courses/945027/lectures/17487339), installed VirtualBox on my computer because I wanted my own learning environment to break, fix and develop my custom solutions.

