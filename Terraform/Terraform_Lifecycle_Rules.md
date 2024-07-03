## Terraform Lifecycle Rules

```
Create_before_destroy = true   
This rule ensures that when a change in configuration forces the resource to be recreated, a new resource is created first before deleting the old one.
```

```
prevent_destroy = true   
When it is set to true, Terraform will reject any changes that will result in the resource getting destroyed and display an error message like this.This is especially useful to prevent your resources from getting accidentally deleted.
```

```
ignore_changes = [
    attributes
]   
The ignore changes argument accepts a list as inficated by the square brackets, and it will accept any valid resource attribute. This lifecycle rule when applied will prevent a resource from being updated based on a list of attributes that we define within the lifecycle block.
```

