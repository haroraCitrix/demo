Get Citrix Ingress Controller Image URL on Azure Marketplace

This guide explains the steps to create the URL for CIC image on Azure Markerplace.

#### Prerequisites:

- Valid Azure Marketplace account and Subscription


## Steps:

1. Login to your Azure Marketplace Account.
2. Create a Resource Group under your subscription if the kubernetes cluster has not been created yet. Please note that the      resouce group of the cluster and the CIC registry must be same. So, if the kubernetes cluster where the CIC is to deployed    already exists, then, same resource group should be used for CIC registry. If not, then create a new resouce group and then    create cluster with this new resource group. 

   - Enter any name in Resource group Textbox and set a region.
     <img src="images/image_1.png" width="500">
   - Click on Review+create   
   - Review the details and click on Create.
   
     <img src="images/image_2.png" width="500">
      
3. Select "Citrix Ingress Controller" on Azure Marketplace
   <img src="images/image_3.png" width="500">
   - Click on "GET IT NOW"
   - Verify the details on pop-up and Click on "Continue"
     <img src="images/image_4.png" width="500">

4. Create CIC Image registry with the Resource Group created in step 2
   <img src="images/image_5.png" width="500">
   - Click on "Create new" for new Azure CIC Registry
   - Enter a Registry name
   - Select the Resource group name from Step 2 in Resource group dropdown
   - Set location
   - Keep the tag latest and selece auto update.
   - Verify your account details and click on "Subscribe"
     

5. Get the Repository Image URL
   - Go to Resouce Groups page and select the resource group created in Step 2.
   - From the right side column, select the registry created in Step 4.
     <img src="images/image_6.png" width="500">
   - Under "services" on Left column, click on "Repositories"
     <img src="images/image_8.png" width="500">
   - Find the "citrix/citrix-k8s-ingess-controller" under repositories and select it.
     <img src="images/image_9.png" width="500">
   - Now, select "latest" in the new right column.
   
     <img src="images/image_10.png" width="500">
   - Here, image URL is shared in "Docker pull command" text. Copy the same and replace as image in CIC yaml.
   

