##### Terraform Language Basics
- Template syntax

```terraform
resource "azure"
```

#### Terraform Providers
- Terraform dependancy locak file to maintain the version of the provider in cross system.

**Note:** Find how we can store a terraform dependancy lock file in a centralized remote location like statefile.

#### Resource Meta-Arguments
- **depends_on :** To handle `hidden resource or module dependancies` that terraform can't automatically infer.
- **count :** For creating multiple resource instances according to a count.
- **for_each :** To create `multiple instances` according to a <span style="color: green;">map</span>, or <span style="color: green;">set</span> of string.
- **provider :** For selecting a `non-default provider` configuration.
- **lifecycle :** Standard `Resource behavior can be altered` using special nested <span style="color: green;">lifecycle block</span> within a resource block body. 


