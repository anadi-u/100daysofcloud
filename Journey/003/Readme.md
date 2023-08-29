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




## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 3 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.

## Next Steps

✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
