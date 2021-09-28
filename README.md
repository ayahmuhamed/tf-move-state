# tf-move-state
Used for move state
## Pre-requirements

* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) 
* [Terraform cli](https://learn.hashicorp.com/tutorials/terraform/install-cli)


## How to use this repo

- Clone
- Run

---

### Clone the repo

```
git clone https://github.com/ayahmuhamed/tf-move-state
```

### Change directory

```
cd tf-move-state/sample
```

### Run

* Init and apply:

```
terraform init && terraform apply --auto-approve
```



* Check state:

```
terraform state list
```

_sample_:

```
terraform state list
null_resource.hello
random_pet.name
```

* Update the code to use the module:

```
cp change-main.txt main.tf
```

* Run terraform init again to initialize the module:

```
terraform init
```


* Run terraform apply again. Confirm there is no change:

```
terraform apply
```




* Check state once again:

```
terraform state list
```

_sample_:

```
terraform state list
null_resource.hello
module.mymodule.random_pet.name
```

* Run terraform destroy and confirm both resources are destroyed

```
terraform destroy
```

