
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

<br><br>

| Role | Description |
|-|-|
| **AWS service role** | A role that a service assumes to perform actions in your account on your behalf. | 
| **AWS service role for an EC2 instance** | A special type of service role that an application running on an Amazon EC2 instance can assume to perform actions in your account. | 
| **AWS service-linked role** | A unique type of service role that is linked directly to an AWS service. Service-linked roles are predefined by the service and include all the permissions that the service requires to call other AWS services on your behalf. The linked service also defines how you create, modify, and delete a service-linked role. A service might automatically create or delete the role. | 
| **Role chaining** | Role chaining occurs when you use a role to assume a second role through the AWS CLI or API. | 

<br><br>

| CONCEPTS | Description |
|-|-|
| **Trust policy** | A JSON policy document in which you define the principals that you trust to assume the role. A role trust policy is a required resource-based policy that is attached to a role in IAM. The principals that you can specify in the trust policy include users, roles, accounts, and services. | 
| **Permissions policy** | A permissions document in JSON format in which you define what actions and resources the role can use. | 
| **Permissions boundary** | An advanced feature in which you use policies to limit the maximum permissions that an identity-based policy can grant to a role | 
| **Principal** | An entity in AWS that can perform actions and access resources. A principal can be an AWS account root user, an IAM user, or a role. | 

<br><br>

### Temporary security credentials in IAM:

You can use the AWS Security Token Service (AWS STS) to create and provide trusted users with temporary security credentials that can control access to your AWS resources. 

<br><br>

| AWS STS | Description |
|-|-|
| **Delegation** | The granting of permissions to someone to allow access to resources that you control. Delegation involves setting up a trust between two accounts. | 
| **Federation** | The creation of a trust relationship between an external identity provider and AWS. Users can sign in to a web identity provider, such as Login with Amazon, Facebook, Google, or any IdP that is compatible with OpenID Connect (OIDC). Users can also sign in to an enterprise identity system that is compatible with Security Assertion Markup Language (SAML) 2.0, such as Microsoft Active Directory Federation Services. | 
| **Federated user** | Instead of creating an IAM user, you can use existing identities from AWS Directory Service, your enterprise user directory, or a web identity provider. | 
| **Role for cross-account access** | A role that grants access to resources in one account to a trusted principal in a different account. | 


<br><br>

## IAM POLICY:
        
Helps to determine what they can access


<br><br>

| Policy types | Description |
|-|-|
| **Identity-based policies** | Attach managed and inline policies to IAM identities (users, groups to which users belong, or roles). Identity-based policies grant permissions to an identity. |
| **Resource-based policies** | Attach inline policies to resources. The most common examples of resource-based policies are Amazon S3 bucket policies and IAM role trust policies. Resource-based policies grant permissions to the principal that is specified in the policy. Principals can be in the same account as the resource or in other accounts. | 
| **Permissions boundaries** | Use a managed policy as the permissions boundary for an IAM entity (user or role). That policy defines the maximum permissions that the identity-based policies can grant to an entity, but does not grant permissions. Permissions boundaries do not define the maximum permissions that a resource-based policy can grant to an entity. | 
| **Organizations SCPs** | Use an AWS Organizations service control policy (SCP) to define the maximum permissions for account members of an organization or organizational unit (OU). SCPs limit permissions that identity-based policies or resource-based policies grant to entities (users or roles) within the account, but do not grant permissions. | 
| **Access control lists (ACLs)** | Use ACLs to control which principals in other accounts can access the resource to which the ACL is attached. ACLs are similar to resource-based policies, although they are the only policy type that does not use the JSON policy document structure. ACLs are cross-account permissions policies that grant permissions to the specified principal. ACLs cannot grant permissions to entities within the same account. | 
| **Session policies** | Pass advanced session policies when you use the AWS CLI or AWS API to assume a role or a federated user. Session policies limit the permissions that the role or user's identity-based policies grant to the session. Session policies limit permissions for a created session, but do not grant permissions. | 


<br><br>

| Policy types | Description |
|-|-|
| **policy** | JSON |
| **policy** | JSON | 
| **policy** | JSON | 
| **policy** | JSON | 
| **policy** | JSON | 
| **policy** | JSON | 


### RESOURCE POLICY:

Resource based policy allows you to attach a policy directly to the resource that you want to share, instead of using a role as a proxy.

### FUNCTION POLICY:

### EXECUTION ROLE:

### TRUST POLICY:
        
Helps determine who can access the resources




<br><br>

## Determining whether a request is allowed or denied within an account 

![PolicyEvaluationHorizontal](/img/PolicyEvaluationHorizontal.png)

<br><br>

## License

> Licensed under the [MIT](license) license.