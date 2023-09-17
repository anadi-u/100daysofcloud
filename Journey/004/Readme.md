# Day 4: Deeper dive into Azure Bicep

## Introduction
To learn more about different concepts in writing an Azure Bicep template such as conditions, loops and modules

## Prerequisites
- Basic knowledge of ARM templates, Azure Bicep and how these two work in Azure for resource deployment.
- Using Visual Studio Code for writing Bicep templates and use the same for deploying the required resources.


## Cloud Research
- `if` condition can be used in Azure Bicep. It resolves in a boolean value **(True/False)**.
-  If value is true, resource is deployed, if not, resource deployment does not take place. Example:


```
  resource stAccount 'Microsoft.storage/storageAccounts@2021-09-01' = if(deploystroageaccount){
  //...
  }
```

> In the above code, a storage account is only deployed if 'deploystorageaccount' is set to true. The 'if' condition comes with the resource definition.

  - If condition can also be used for use cases or options. Example:
    ```
    resource stAccount 'Micorsoft.storage/storageAccounts@2021-09-01' = if(envName=='Production) {
    //...
    }
    ```
    
  - Loops can used to deploy multiple identical resources together. Similar to loops used in programming languages like C++ and Python.
  - An example code:
```
    param storageAccountNames array = [
    'bulbasaur'
    'charmander'
    'squirtle'
]
resouce storageAccountResources 'Microsoft.storage/storageAccounts@2021-09-01' = [for storagAccountName in storageAccountNames:
{
    name: storageAccountName
    location: resourceGroup().location
    kind: 'storageV2'
    sku:
    {
        name: 'Standard_LRS'
 
    }
}]
  ```

> The above loop deploys three storage accounts at once following the loop conditions/iterations.  

- For loop starts with a square bracket `[]`
- Similar to if condition, loop condition is also written along with the resource definition.
- Count based loops can also be used in Azure Bicep via range function. *Range(x,y) where x= starting value and y=Number of values you count*.
- Example range(3,4) = 3,4,5,6
- `@desciption` can be used to add comments in the Bicep template.
- `@secure` is used to secure the private information such as usernames, passwords and secrets to show in the deployment history logs.

## ☁️ Cloud Outcome

With this exercise, I was able to learn more about different concepts involved in creating a more versetalie Bicep template. 

## Next Steps

Create more Bicep templates using more advanced concepts on Visual Studio Code.
