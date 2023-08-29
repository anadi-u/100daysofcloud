# Infrastructure as code

## Introduction

Infrastructure as code enables you to describe the infrastructure and configuration you want to deploy to the cloud through code. With IaC, application code and templates can be maintained together in a central code repository. I worked on ARM and Azure Bicep templates to deploy resources in Azure.

## Prerequisite

JSON, Visual Studio Code, Azure CLI

## Cloud Research

ARM (Azure Resource Manager) templates define the infrastructure and config for your deployment using JSON. 
It follows decalrative syntax. Declarative syntax is a way of building strcuture and elements without the use of progrmmaing commands to create it.
ARM templates are idempotent, which means you can deploy the same templte multiple times and get the same types of resources in th same state.
A regular ARM template will have the following elements:

-schema: 
Required section that defines the location of the JSON schema file that describes the strcutre of JSON data.

-content version:
Section defines the version of the template

-resources:
Defines the actual items or resources you want to deploy or update in a resource group or subscription

You can deploy an ARM template via these ways:
1. Deploying the template locally
2. Deploy using a linked template
3. Deploy in Continous Deployment pipeline

You can edit the ARM template using a code editor like Visual Studio code. The template can be deployed from Visual Studio code itself, but you have to login to the required Azure account.

Command required to deploy ARM templates:
az deployment group create \
--name <Name of the template>
--group <Resource group you want to deploy to>
--template-file <template file used>

Bicep is an Azure native language used for deploying resources. Follows a simpler syntax than JSON based-templates. 

How does Bicep exactly work?
WHen you submit a Bicep template to deploy resources in Azure, it goes to the Azure Resource Manager. A tooling built into Bicpe converts the Bicep into JSON template. This process is known as transpilation. 

Bicep has 2 main componenets:
1. Parameters:
   Lets you bring values inside the Bicep Template
   When deploying the template, you will be asked to provide the values of the parameters defined.
   To add a parameter, param <paramater name> <paramater type>

2. Variables:
   Defined and set within a template.
   Can be used when you want to store information in one place and refer to it multiple times in the template.
   To add a variable, var <variable name> <variable type>

Type can be of different types like string, int, boolean, object, etc.

## ☁️ Cloud Outcome

This exercise gave me some hands-on experience on deploying ARM and Bicep templates and use visual studio code.
Lessons learnt:
Bicep and ARM templates have different use case scenarios.
While Bicep is easier and less verbose, it cannot be used in different cloud providers, as its an Azure Native language.
ARM tmeplates being JSON based can be used in different cloud providers as well. Terraform is also used to deploy resources in different cloud providers.

