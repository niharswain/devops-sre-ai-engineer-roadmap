# 5. IAM Interview Revision

Try answering each question aloud before reading the short answer.

## Fundamentals

**1. What is AWS IAM?**  
IAM is the global AWS service used to manage identities and permissions.

**2. What is the root user?**  
It is the original identity created with the AWS account. Avoid using it for everyday work and protect it carefully.

**3. What is an IAM user?**  
An identity representing a person or other user that needs access to AWS.

**4. What is an IAM group?**  
A collection of IAM users. Groups help assign common permissions to multiple users.

**5. Can an IAM group contain another group?**  
No. IAM groups contain users, not other groups.

**6. Can one user belong to multiple groups?**  
Yes.

## Policies

**7. What is an IAM policy?**  
A JSON document that defines permissions.

**8. What does least privilege mean?**  
Give only the permissions required for the task.

**9. What is the purpose of `Effect`?**  
It specifies `Allow` or `Deny` for a statement.

**10. What does `Action` represent?**  
The AWS API operations covered by a statement.

**11. What does `Resource` represent?**  
The AWS resources to which the actions apply.

**12. What is a policy condition?**  
An optional rule that controls when a statement applies.

## Authentication and access

**13. What is MFA?**  
An additional authentication factor, typically a password plus a device or authenticator.

**14. What is the difference between an Access Key ID and Secret Access Key?**  
The ID identifies the key; the secret is confidential and must be protected.

**15. What is the AWS CLI?**  
A command-line tool for interacting with AWS services.

**16. What is the AWS SDK?**  
A set of language-specific libraries that application code can use to access AWS services.

**17. What are the three access methods covered in this topic?**  
Management Console, CLI, and SDK.

## Roles and auditing

**18. Why use an IAM role for EC2?**  
It gives the instance permissions to call AWS services without putting a user's long-lived access keys into the application.

**19. Name three examples of AWS services that can use roles.**  
EC2, Lambda, and CloudFormation.

**20. What is the IAM Credentials Report?**  
An account-level report showing users and the status of their credentials.

**21. What is IAM Access Advisor?**  
A user-level view of service permissions and when those services were last accessed.

**22. How can Access Advisor help with least privilege?**  
It can help identify permissions that may be unused and should be reviewed.

## Practical scenario questions

**23. A developer needs read-only access to EC2 information. What should you consider?**  
Create or assign a policy that grants only the required read/describe actions and limits resources where supported.

**24. A team of developers needs the same permissions. How can you manage this efficiently?**  
Create an IAM group, attach the appropriate policy to the group, and add the individual users.

**25. A developer has moved to another team. What should you review?**  
Their group memberships, directly attached policies, and any other access they still need. Remove old access only after confirming the new responsibilities.

**26. An EC2-hosted application needs to call an AWS API. What is the preferred IAM concept from this topic?**  
Use an IAM role for the EC2 instance with narrowly scoped permissions.

## Quick memory sheet

| Topic | Remember |
|---|---|
| IAM | Global identity and access service |
| Root user | Do not use for daily work |
| User | Individual identity |
| Group | Contains users only |
| Policy | JSON permissions document |
| Least privilege | Only required permissions |
| MFA | Password + device/authenticator |
| Console | Password + MFA |
| CLI / SDK | Programmatic access |
| Access keys | Keep secret; never share |
| Role | Permissions for AWS services |
| Credentials Report | Account-level credential review |
| Access Advisor | User-level service access review |
