# Cookiecutter Terraform

A cookiecutter template for bootstrapping a Terraform project my way. It closely follows the recommendations in the
[HashiCorp docs](https://developer.hashicorp.com/terraform/language/style#file-names). I like putting my backends and
environment variable files in directories, then I reference then during execution. 

## Quickstart

Install the latest Cookiecutter, I recommend using [pipx](https://github.com/pypa/pipx):

```bash
pipx cookiecutter
```

Now you can create your infrastructure in your existing project or use it to boostrap a repository.

```bash
cookiecutter https://github.com/phillipsj/cookiecutter-terraform.git
```