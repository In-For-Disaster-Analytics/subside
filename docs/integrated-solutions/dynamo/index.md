---
title: DYNAMO - DYnamic Analysis and MOdeling
---

## DYNAMO: DYnamic Analysis and MOdeling

## AI approaches to dynamic analysis, modeling, and information management for groundwater, rivers, and coasts

### Abstract 
The DYNAMO allocation supports dynamic analysis and modeling workflows for physics-based systems with the goal of modernizing existing simulation tools and adding to the existing collection of models for the state of Texas. The DYNAMO compute allocations support testing and management of modeled information at scale for simulations data and tools. Modeling domains will include groundwater aquifers, fluvial and riverine surface water systems, and coastal systems. Additional domains of interest, such as subsidence and coastal spill conditions ,may be incorporated into DYNAMO applications and test cases.

### Description
As part of the DYNAMO effort, storage and applications are in development to support big data collections composed of modeled outputs and ancillary or complementary datasets. The DYNAMO data collections need to follow FAIR principles for findable, accessible, interoperable, and reusable tools and collections.

In addition to compute resources on Lonestar6 and Stampede3 on premise at TACC, the DYNAMO activities include the use of Microsoft Azure services for the AIM Flagship team of PT2050 . The Microsoft credits and funding have been pivotal for joint research applications with partners in the state of Texas. Over time we have developed a few approaches that leverage our on premise HPC systems with Azure. The resources complement each other and have helped us expand partnerships and research projects.

The additional credits will help us continue supporting the Water Science Program at the Texas Water Development Board (TWDB). Project DYNAMO is a joint effort between PT2050 researchers and TWDB water science to scale physics-based modeling capabilities in Texas. The agency has been running flood simulation tests on the existing Azure credits resulting in a 20 - 50% speed up in model run times. Importantly, the services are highly valued because teams can share large models (>120GB) for peer review more easily. Before using Azure teams were mailing hard drives across the state and between organizations. Azure has been key to the success of tests to date and with the latest gift credits we will continue providing access to our testbed Kubernetes on the cloud services to the agency.

## Model Evaluation Environment

### Access Instructions

The Decision Support Office at TACC created the Model Execution and Evaluation Platform (MEEP) as an environment that supports modeling tasks. The MEEP system provides a Windows Virtual Machines (VMs) with common flood modeling applications.  Follow these steps to access your MEEP Environment via Microsoft’s Azure.

#### 1. Create a Microsoft Azure account.

Navigate to the [Azure Create Account](https://signup.live.com/signup) page. Register with the email address you want to use for your MEEP user account. **You may use your TACC user account and email address.**

#### 2. Log in to Azure

Once you’ve confirmed registration, notify the DSO team and TACC will set up your environment.  Go to: https://portal.azure.com/#@utexas.onmicrosoft.com/resource/subscriptions/25ddd913-58be-4c11-bde5-3ab19b3f6097/resourceGroups/hecras/providers/Microsoft.Compute/virtualMachines/Model-Evaluation-{LASTNAME}/overview 

Change **********{LASTNAME}**********  to your last name

#### 3. Start up and Connect to the Virtual Machine

Once you’ve logged into your VM, you’ll see your landing page entitled  “Model-Evaluation-*YourLastName*” as demonstrated in Image 1. below. 

- Click the Start button located below the Resource Name.
- Scroll down on the left column until you see “Bastion”. Click the “Bastion” button.
    
    ![Image 1. ](/Dynamo%20MEEP%20Upload%20Model%20Data%202b24345371794c7b843b0fd144253539/Cyberduck%20-%20new%20profile.png)
    
    Image 1. 
    

#### 4. Continue with Authorization

Fill in the following fields as shown in Image 2 below.  Do not edit other fields.

- Authorization Type to: **Password from Azure Key Vault.**
- Username: **evaluator**
- Subscription: TACC-MEEP
- Key vault: **usacekeys**
- Azure Key Vault Secret: **evaluator**
- **Click Connect. 

You should now have access to your VM!**

![Screenshot 2023-04-06 at 3.51.41 PM.png](/Dynamo%20MEEP%20environment%201cb92cec96e143408bcbd296f5423205/Screenshot_2023-04-06_at_3.51.41_PM.png)

### Accessing a Model

Once you’ve connected to your VM, you can use this machine like any Windows PC. The VM comes with Libre Office for word docs and excel files, and Microsoft Edge will allow you to read PDFs. You will find the files you need in the E: Drive. Please copy them over to the F: Drive while you are working on them.  Proceed with your model evaluation.

Software is installed for the following models:

- HEC-RAS
- HEC-HMS
- HEC-SSP
- HEC-MetVue

#### Model Structure

The Army Corps Evaluators will follow the SOP’s to evaluate models. 
Click to expand/collapse 

- Region
    - Study Area
        - 25Percent
            - Hydrologic Products
                - GIS
            - Hydrologic Features
            - Hydrologic Losses
                - Land Cover
                - Terrain
                - Gauge Locations
            - Calculations and Supporting Data
                - Hydrologic Transform Calculations
                - Hydrologic Loss Calculations
                - Calibration and Validation
                - Gage Data
                - Statistical Hydrology
                - Reservoir Data
                - Elliptical Storm Data
                - Final Hydrologic Results
                    - Hydraulic Products
                - GIS
                - HYDRAULICS
                - FEATURES
                - Final_files
                    - Coastal Products
                - GIS
                - HYDRAULICS
                - FEATURES
                - Final_files
        - 50Percent
        - 75Percent
        - **100Percent**

### Help

Contact DSO for your administrative needs and for technical issues with Azure. 

DSO POC: Tabish Khan [tkhan@tacc.utexas.edu](mailto:tkhan@tacc.utexas.edu)

Secondary POCs: William Mobley [wmobley@tacc.utexas.edu](mailto:wmobley@tacc.utexas.edu) and Suzanne Pierce [spiercey@tacc.utexas.edu](mailto:spierce@tacc.utexas.edu)

### **Issues**

- Getting a limited connection issue.
    
    Go back to the VM overview page. Confirm the Machine is “on” if not press start. 
    

![Untitled](/Dynamo%20MEEP%20environment%201cb92cec96e143408bcbd296f5423205/Untitled.png)

- Header Connection Error
    
    Go back to the VM overview page. Press the restart button try to relogin. 
    
    ![Screenshot 2022-12-12 at 3.23.53 PM.png](/Dynamo%20MEEP%20environment%201cb92cec96e143408bcbd296f5423205/Screenshot_2022-12-12_at_3.23.53_PM.png)
    
- Connection error expired credentials
    - Email wmobley@tacc.utexas.edu with a screenshot he will update the os to fix this issue.

![Screenshot 2022-12-12 at 3.31.16 PM.png](/Dynamo%20MEEP%20environment%201cb92cec96e143408bcbd296f5423205/Screenshot_2022-12-12_at_3.31.16_PM.png)
