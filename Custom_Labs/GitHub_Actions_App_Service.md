---
lab:
    title: 'Lab: GitHub Actions for Azure App Service using DevOps Starter'
    module: 'Module 8: Implementing Continuous Integration with GitHub Actions'
---

# Lab: GitHub Actions for Azure App Service using DevOps Starter
# Student lab manual

## Lab overview

In this lab, you will how to create a simple GitHub Action workflow example using the helper "DevOps Starter" templates offered by Azure.

## Objectives

After you complete this lab, you will be able to:

-   Create and understand GitHub Action workflow basics. 

## Lab duration

-   Estimated time: **30 minutes**

## Instructions

### Before you start

#### Sign in to the lab virtual machine

Ensure that you're signed in to your Windows 10 virtual machine by using the following credentials:
    
-   Username: **Student**
-   Password: **Pa55w.rd**

#### Review applications required for this lab

Identify the applications that you'll use in this lab:
  
-   Microsoft Edge

#### Prepare an Azure subscription

-   Identify an existing Azure subscription or create a new one.
-   Verify that you have a Microsoft account or an Azure AD account with the Owner role in the Azure subscription and the Global Administrator role in the Azure AD tenant associated with the Azure subscription. For details, refer to [List Azure role assignments using the Azure portal](https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-list-portal) and [View and assign administrator roles in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/roles/manage-roles-portal#view-my-roles).

#### Prepare a Github account

-  Create a GitHub account with the **same Microsoft account** used for Azure Subscription: https://github.com/join 
  

### Exercise 1 : Create a DevOps starter template

In this exercise, you will create a DevOps Starter example that will:

-  Create an example Git repo in GitHub for us, composed of:
    -  A simple .net core website together with some test code.
    -  ARM templates to deploy the needed Azure resources for the website
    -  The workflow that will build, deploy and test the website. 


#### Task 1: Create DevOps Starter resource

1.  On your lab computer, start a web browser and navigate to [Azure Portal](https://portal.azure.com). On the search bar look for **DevOps Starter** and click on it.

1.  Click on **Create**. on the right side tehre is an option to **Try DevOps starter with Github**. Click on **Set up DevOps starter with GitHub**.

    > **Note**: The setting can be changed back to use Azure DevOps by click on the option shown below the language options. **Setting up DevOps starter with GitHub, change settings here**.

1.  Choose **.NET** for you application and click on **Next**.
1.  Choose **ASP .NET Core** and click on **Next**.
1.  Now we need to authorize azure to create the needed resources on our GitHub account. Click on **Authorize**.

    - Choose your GitHub organization (or leave default)
    - **Repository**: lets call it **az400module8GithubActions**
    - **Subscription**: choose your subscription.
    - **Web app name**: needs to be globally unique, you can choose **az400module8GithubActions[ALIAS]** (replace [ALIAS], including [] with your initials or any unique string )
    - **Location**: Choose the closest region.

1.  Click on **Done**.
1.  Click on **Go to Resource** when finished creating.
1.  Click on **Authorize to GitHub** > **Authorize**  to see the most recent GitHub Action workflow executions. From the **GitHub Workflow** pane we can see the progress and jump into GitHub resources by clicking the links provided.

1.  Take some time to understand and review what **DevOps Starter** tool created for us: 
    - Review the repo, composed of the app code, ARM templates for Azure infrastructure and the workflow folder.
    - Review the created workflow (yaml file), which defines 3 jobs (build, deploy and Functional Tests).
    - Review the progress of the workflow on the **Actions** section of the GitHub repository page.
    - Azure also created the needed credentials for us as GitHub Secrets. Go to **Settings** > **Secrets** to find the created Azure credentials used by the actions interacting with Azure. 
