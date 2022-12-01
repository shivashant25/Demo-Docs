# DevSecOps: L100

## Overview

Contoso Traders are one of the leading E-Commerce platforms with wide range of electronic products like Desktops and Laptops, Mobile Phones, Gaming console accessories and Monitors. This includes a wide range of international brands like Microsoft Surface, XBOX, Samsung, ASUS, DELL etc. Contoso Traders Organization is using Microsoft 365 for their collaboration works internally.

Contoso Traders has different departments like Marketing, Sales, Accounts, HR, IT. For internal communication they are using Microsoft Teams and Outlook. In Contoso Traders Organization, there are various functionalities with the Contoso Traders E-commerce platform like product approval, product price approval, Product price update approval etc. 

## Lab Context

In this lab, you will explore the Contoso traders code base present in a GitHub repository. The repository contains all the files related to the application’s UI, backend APIs, deployment files, GitHub workflows, and deployment guides.

## Hands-On Guide

1.	Open browser, using a new tab navigate to `https://github.com/CloudLabs-AI/ContosoTraders` GitHub repository. You’ll able to visualize multiple files and folders. 

    ![](media/ct1.png)

1.	Navigate to **github/workflows** folder, it contains the workflow files using which you can the deployment resources. Please find the details of the individual workflow.

    ![](media/ct2.png) 

1.	**Contoso-traders-infra-deployment.yml** will deploy the infrastructure into Azure which includes a resource groups, resources, sets access policies to key vaults, and seeds the database from storage accounts to Azure SQL database.

    ![](media/ct3.png) 

1.	**contoso-traders-app-deployment.yml** deploys the application to Azure cloud. The application is configured to use the pre-deployed resources.

    ![](media/ct4.png) 

1.	**contoso-traders-load-testing.yml** configures the load testing on the application.
  
    ![](media/ct5.png)

1.	The **docs** folder contains the deployment instruction files which guides you to deploy the infrastructure and application.

    ![](media/ct6.png)

1.	The **iac** folders contains the bicep templates which deploys the infrastructure needed for the application.

    ![](media/ct7.png) 

1.	The **src** folder contains all the source code files related to backend APIs, UI, and other parts of the application.

    ![](media/ct8.png)  

1.	The **tests** folder contains the files related load testing.

    ![](media/ct9.png)   

1.	From the **code** tab, scroll down a little and you’ll find the **links (1)** to access the application. There are different links for test, production UI. You also access the **deployment instructions (2)** files using the links provided in Documentation paragraph.

    ![](media/ct10.png)  

1.	If you scroll a little bit more, you’ll visualize the entire application infrastructure diagram. The diagram explains how different Azure resources are integrated together and runs in synchronized manner to ensure the working of the application.

    ![](media/ct11.png)  

1.	From the GitHub repository, navigate to **Actions (1)** tab. You’ll see the different **GitHub workflows (2)** in the Actions side blade.

    ![](media/ct12.png)  

1.	The **contoso-traders-infra-provisioning (1)** workflow is configured to deploy the bicep templates which will deploys the whole infrastructure to Azure. To run the workflow, click on **Run workflow (2)** and select **Run workflow (3)** to trigger the action.

    ![](media/ct13.png)  

1.	The **contoso-traders-app-deployment (1)** workflow is configured to deploy the application to Azure cloud. The workflow uses the resources which were deployed from contoso-traders-infra-provisioning workflow. To run the workflow, click on Run workflow (2) and select Run workflow (3) to trigger the action.
  
    ![](media/ct14.png)   

1.	The **contoso-traders-load-testing (1)** workflow will configure load testing on the application. To run the workflow, click on Run workflow (2) and select Run workflow (3) to trigger the action.

    ![](media/ct14.png)
   
1. Navigate to **Settings (1)** tab, select **Code security and analysis (2)** tab. Here, **Dependency graph**, and **Dependabots** are enabled. 

   - **The dependency graph** includes all the dependencies of a repository that are detailed in the manifest and lock files, or their equivalent, for supported ecosystems, as well as any dependencies that are submitted using the Dependency submission API.
   
   - **Dependabot alerts** tell you that your code depends on a package that is insecure or malicious.   

   - **Dependabot security updates** creates  alert for every vulnerable dependency identified in your full dependency graph. However, security updates are triggered only for dependencies that are specified in a manifest or lock file.
   
   ![](media/ct16.png)
   
1. Now, login into your Azure account where the contoso traders infrastructure is deployed. If the infrastructure is not deployed, please follow the **Deployment setup** documentation.

1. From the Azure portal, search for **Microsoft Defender for cloud (1)** from the search and select **Microsoft Defender for cloud (2)**.

   ![](media/ct17.png)
   
1. From Microsoft Defender for cloud page, select **Environment settings (1)** tab from the side blade and click on your **subcription (2)**      
      
   ![](media/ct18.png)
   
1. In the Settings | Defenders page, you'll be able to see all the resources for which Azure Defender plan is enabled. These are resources are protected and Azure Defender for cloud finds weak spots across your cloud configuration, helps strengthen the overall security posture of your environment.
   
   ![](media/ct19.png)   
   
1. Navigate back to Microsoft Defender for cloud page, select **Recommendations** from the side blade.

   ![](media/ct20.png)
   
1. In the Recommendations page, select the **All recommendations (1)** tab. You'll be able to see a bunch of recommendations based on the severity. Using the policies, Defender for Cloud periodically analyzes the compliance status of your resources to identify potential security misconfigurations and weaknesses. It then provides you with recommendations on how to remediate those issues. Recommendations are the result of assessing your resources against the relevant policies and identifying resources that aren't meeting your defined requirements.

   ![](media/ct20.png)
  
1. In the Recommendations page, scroll down a bit and you'll be able to see a set of recommendations for the protected resources and click on any of the recommendation to see the details

   ![](media/ct21.png)
  
1. Here, you'll be able to see the **Description** of the recommendation, **Remidiation steps** using which you can fix the vulnerability , and **Affected resources**.

   ![](media/ct21.png)  

    
