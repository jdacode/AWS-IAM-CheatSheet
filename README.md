
# AWS-IAM-CheatSheet

<br><br>
## AWS IAM Diagram

![iam](/img/iam.png)

## AWS IAM

### IAM users:

        USER is an entity that you create in AWS to represent the person or application that uses it to interact with AWS. A user in AWS consists of a name and credentials.

        An IAM user with administrator permissions is not the same thing as the AWS account root user. 

### IAM ROLES:
        
        Allow users or services to access resources

### IAM POLICY:
        
        Helps to determine what they can access

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