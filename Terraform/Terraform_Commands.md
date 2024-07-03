## Terraform Commands

```
terraform valid - used to check the syntax of the file instead of running plan and apply
```

```
terraform fmt - used to format the code to more readable form
````

```
terraform show - used to print all the attributes created by terraform for that resource   
terraform show -json - to print all the contents in json
```

```
terraform providers - to print the providers 
terraform providers mirror directory - to print the contents to a particular file
```

```
terraform output - to print all the ouput variables on the current configuration
```

```
terraform refresh - if there are any changes made to a resource created by terraform outside its control, such as a manual update, the terraform refresh command will pick it up and update the state file. This reconciliation is useful to determine what action to take during the next apply.
This command will not modify any infrastructure resource but it will modify the state file.As we saw earlier, terraform refresh is also run automatically by commands such as terraform plan and terraform apply.This is done prior to Terraform generating an execution plan.   
This can however be bypassed by using the -refresh=false option with the commands.
```

```
terraform graph - is used to create a visual representation of the dependencies and a Terraform configuration or an execution plan.
we need an external tool called graphviz to comprehend that data to visual format   
$ apt update
$ apt install graphviz -y  
$ terraform graph | dot -Tsvg > graph.svg 
```

```
terraform apply - The terraform apply failed in spite of our validation working! This is because the validate command only carries out a general verification of the configuration. It validated the resource block and the argument syntax but not the values the arguments expect for a specific resource!
```

