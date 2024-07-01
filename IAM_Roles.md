## AWS Authentication & Acees control (IAM)

- The user gives the permissions applied to the group through the policy    
- Indentify based polices can be applied to users, groups and roles.    
- Roles are used for delegation and are assumed.  

### IAM USERS
1. Root user has full permissions. Its a best practice to avoid using the root user accout + enable MFA  
2. Upto 500 individual users accounts can be created users have no permission by default.  

### IAM User Groups  
1. Admin group  
2. Development group  
3. Operative group  

- user groups are collection of users  
- The main reason to use groups is to apply permissions to users using policies  

### IAM Roles
- An IAM Role is an IAM identy that has specific permissions  
- Roles are assumed by users, application and services.  
- Once assumed, the identity becomes the role and fain the roles permission.  

Adminstrator Access - Polices are documents that define permissions and are written in json  
Bucket Policy - Resource based policy apply to resources such as s3 buckets  


