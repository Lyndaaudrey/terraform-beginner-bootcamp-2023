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

## Working with Env Vars 

List all env vars usint 'env' command
We can also filter by using 'env| grep AWS_'

## Setting and Unsetting Env Vars 

In the terminal we can set using 'export HELLO ='world''
In the terminal we can unset using 'unset HELLO' 

