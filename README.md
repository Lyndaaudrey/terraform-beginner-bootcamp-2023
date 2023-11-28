# Terraform Beginner Bootcamp 2023

## Semantic versionning 

This project is going to utilize semantic versioning for its tagging.
[semver.org] 

The general format:

Given a version number **MAJOR.MINOR.PATCH**, increment the:

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes
Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

## Install Terraform CLI

The terraform CLI installation instruction

[Install Terraform CLI] (https://developer.hashicorp.com/terraform/install)

## Considerations for Linux Distribution

This project is buit against Ubuntu. Check your Linux Distribution by typing [cat /etc/os-release] in the terminal.

## Refactoring into Bash Scripts

Whilte fixing the terraforM CLI we notice that the scripts (.gitpod.yml) steps were shorter so we created a new installation bash script. 

## Shebang

Don't forget to put shebang (#!/bin/bash) at the beginning of the file to run the script.

## Linux Permissions Considerations

To execute our bash script we need eto change permissions as follow in the terminal :
chmod u+x ./bin/install_terraform_cli 

## Github Lifecycle

Change init with before in the gitpod.yaml file to re-run when restarting a workspace

## Issues with terraform Cloud Login and Gitpod Workspace
Probleme when trying to run terraform login.
To fix this you have manually generate the token in terraformc cloud at this address:
```
https://app.terraform.io/app/settings/tokens?source=terraform-login
```

 Then create and open the file manually here :
```sh
 touch /home/gitpod/.terraform.d/credentials.tfrc.json 
 open /home/gitpod/.terraform.d/credentials.tfrc.json
```
 Provide the following code (replace your token in the file):
 
 ```json
 {
    "credentials":{
        "app.terraform.io":{
            "token": "Your-terraform-cloud-token"

        }
    }
 }
 ```
