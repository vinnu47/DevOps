## how CloudFormation works
- Templates must be uploaded in S3 and then referenced in CloudFormation  
- To update a template, we cant edit previous ones. We have to re-upload a new version of the template to AWS  
- Stacks are identified by a name  
- Deleting a stack deletes every single artifact was created by CloudFormation  
 
 ## CloudFormation Update Behaviour
- CloudFormation updates resources based on difference between what you submit and stacks's current template  
- which method to use depend on which property you update for a resource  
- **Update with No Interruption**
 - Without disrupting resources operation & without chaning physical ID  
 - Example:updating the IAM instance profile of an EC2 instance  
- **Update with some interruption**  
 - Example:updating an EC2 instance type fro t2.micro to t2.large  
- **Replacement**
 - Recreating the resource with new physcial ID  
 - Creates the new resource, change references from other resources to the new resource, then deletes the old resource   
 - Example:updating an RDS DB instance availability zone    

### How to Refeence a Parameter 
- The Fn::Ref fucntion can be leveraged to reference parameters  
- parameters can be used anywhere in a template, except:  
 - AWSTemplateFormatVersion  
 - Description   
 - Transform  
 - Mappings   
- The shorthand for this in YAML is !Ref   
- The function can also refernce other elements within the template    


