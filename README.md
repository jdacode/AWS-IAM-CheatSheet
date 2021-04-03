
# AWS-IAM-CheatSheet

<br><br>
## AWS IAM Diagram

![iam](/img/iam.png)

## AWS IAM

## IAM users:

        - USER is an entity that you create in AWS to represent the person or application that uses it to interact with AWS. A user in AWS consists of a name and credentials.

        - An IAM user with administrator permissions is not the same thing as the AWS account root user. 

## IAM groups:

        - An IAM group is a collection of IAM users. Groups let you specify permissions for multiple users, which can make it easier to manage the permissions for those users.

## IAM ROLES:
        
### Role

Allow users or services to access resources.
        
Roles can be used by the following:

        - An IAM user in the same AWS account as the role
        - An IAM user in a different AWS account than the role
        - A web service offered by AWS such as Amazon Elastic Compute Cloud (Amazon EC2)
        - An external user authenticated by an external identity provider (IdP) service that is compatible with SAML 2.0 or OpenID Connect, or a custom-built identity broker.


| Role| Description |
|-|-|
| **AWS service role** | A role that a service assumes to perform actions in your account on your behalf. | 
| **AWS service role for an EC2 instance** | A special type of service role that an application running on an Amazon EC2 instance can assume to perform actions in your account. | 
| **AWS service-linked role** | SysAdmin | 
| **Role chaining** | SysAdmin | 
| **Delegation** | SysAdmin | 
| **Federation** | SysAdmin | 
| **Federated user** | SysAdmin | 
| **Trust policy** | SysAdmin | 
| **Permissions policy** | SysAdmin | 
| **Permissions boundary** | SysAdmin | 
| **Principal** | SysAdmin | 
| **Role for cross-account access** | SysAdmin | 



### IAM POLICY:
        
        - Helps to determine what they can access

### RESOURCE POLICY:

        - Resource based policy allows you to attach a policy directly to the resource that you want to share, instead of using a role as a proxy.

### FUNCTION POLICY:

### EXECUTION ROLE:

### TRUST POLICY:
        
        - Helps determine who can access the resources


<br><br>
## Determining whether a request is allowed or denied within an account 

![PolicyEvaluationHorizontal](/img/PolicyEvaluationHorizontal.png)

<br><br>
## License

> Licensed under the [MIT](license) license.