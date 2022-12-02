## In this documentation, we will learn how to deploy the Machine Learning Model Using Azure Devops!

![image](https://user-images.githubusercontent.com/92631457/204377265-80be9fff-184f-47e4-94f9-caa036d611c3.png)



### Pre-Requisites:

 - AKS cluster needs to be up running. You can set up aks cluster using CLI, GUI or terraform script.
 - ACR is also setup in Azure cloud.
 - Already created Azure DevOps dashboard in https://dev.azure.com
 - Dockerfile created along with the application source code in the same directory.
 - Make sure AKS has pull access from ACR. You can do so by running the following command using azure CLI
```sh
 az aks update -n myAKSCluster -g myResourceGroup --attach-acr <repo-name>
 az aks update -n myAKSCluster -g myResourceGroup --detach-acr <repo-name>
```

### Implementation Steps:
  1. Create Azure Build pipeline for building Docker images and uploading into ACR.
  2. Create Azure Release pipeline for deploying Docker containers into AKS.
