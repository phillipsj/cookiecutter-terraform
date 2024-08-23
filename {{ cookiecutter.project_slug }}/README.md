# Getting started.

This Terraform roughly follows the style guide in the [HashiCorp docs](https://developer.hashicorp.com/terraform/language/style#file-names). The main differences are with the envs and 
backends directories. These directories are for storing the settings for specific environments and should be referenced 
when executing the Terraform.

### Backends Example

Here is a quick example on the backends folder usage.

```bash
terraform init -backend-config=./backends/prod.tfbackend
```

In a CI solution you can do something like this:

```bash
terraform init -backend-config=./backends/${MY_ENV}.tfbackend
```

### Envs Example

Here is a quick example on the envs folder usage.

```bash
terraform apply -var-file=./envs/prod.tfvars
```

In a CI solution you can do something like this:

```bash
terraform apply -var-file=./envs/${MY_ENV}.tfvars
```

## Quickstart

Install the latest Cookiecutter, I recommend using [pipx](https://github.com/pypa/pipx):

```bash
pipx cookiecutter
```

Now you can create your infrastructure in your existing project or use it to boostrap a repository.

```bash
cookiecutter https://github.com/phillipsj/cookiecutter-terraform.git
```