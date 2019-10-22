# AzureCustomRBAC_DevOps

Organizations using custom RBAC roles in Azure will see that managing the custom role definitions is cumbersome and warrants using a software development/DevOps methedolgy for management. This solution shows how you can use Azure DevOps to setup a CI/CD pipeline for managing and deploying these custom definition files. Using this provides version control, enhanced security, and easier deployment and management of these roles. 

Overview: 
This solution relies on an administrator to author and upload Azure role definition files in JSON format to a repository thats referenced as part of an Azure DevOps pipeline. The build calls a single task for running an PowerShell script (ActionRole.ps1) against Azure resource manager. The script checks for new JSON (definition files) files in the repository, or changes to existing ones, and either creats the custom role or updates existing roles. 

![alt text](https://raw.githubusercontent.com/kylgrn/AzureCustomRBAC_DevOps/master/AzureRBACDevOps.png)

