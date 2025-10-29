# Exercise 1 - Create and Configure the SAP Build Process Automation Project for Equipment and Training Approval Workflow

## Overview
In this exercise, you will be setting up a SAP Build Process Automation (SBPA) project to manage the approval workflow for equipment and training of newly hired employees in SuccessFactors. This workflow will be initiated directly by SuccessFactors Integration once a new hire record is created. For the sake of that exercise you will be working with a predefined project where you would need to add additional steps and mapping. 

1) [Create a new project based on the given "New Hire Onboarding Experience – Template" project and save it](#1create-a-new-project-based-on-the-given-new-hire-onboarding-experience--template-project-and-save-it)<br>
2) [Add event trigger as starting point of your process](#2Add-event-trigger-as-a-starting-point-of-your-process)<br>
3) [Define Condition](#3Dedine-Condition)<br>
4) [Map process inputs](#4Map-process-inputs)<br>
5) [Release and Deploy](#4Release-and-Deploye)<br>

### 1)	Create a new project based on the given "New Hire Onboarding Process TEMPLATE" project and save it. 

1.	Login to [SAP Build Process Automation](https://ad167-us-wpjiqpp4.us10.build.cloud.sap/lobby) by using custom identity provider and your TechEd username and password. 

2. Now, you need to copy a template project that have some predefined steps. Go to the Lobby and find **New Hire Onboarding Process TEMPLATE**. From the tree dot button **Options** select **Save as New Project**. Copy the editable version of the project (New Hire Onboarding Process TEMPLATE) from lobby by adding your username at the end - DO NOT USE THIS PROJECT OR EDIT THIS, please copy and change the description.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/tree%20dots%20menu.png)

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/save%20as%20new%20project.png)

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/save%20as%20new%20projec%20name%20and%20description.png)

3.	Once copied, open the project and find the New Employee Equipment and Training Approval Process in the Artifacts list. Open the process. 

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/openprocess.png)

### 2)	Add event trigger as a starting point of your process

1. In the process builder canvas click on **Add a Trigger**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/addtrigger.png)

3. Select **Wait for an Event**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/waitforevent.png)

4. Type **New Hire Data Review Initiated** in the search field of the library. Once listed, you can click on **Add**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/Selectevent.png)

5. In the trigger editor add you session ID and user ID the to the suggested trigger’s name and then click on **Create**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/Seteventtriggername.png)

>  Note: Now, you have your trigger created. 

### 3)	Define Condition

1. Click on the Condition step, a right side menu should be opened. Click on the three dots button in the Branch Condition. Condition Editor is opened.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/SFSFCondition.png)

2. Select in the left field "**personIdExternal**" from the process inputs, **"contains"** in the middle field and AD167-XXX in the right field by replacing the XXX with your user ID (e.g AD167-001. AD167-002), etc. Click **"Apply"** 

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/SFSFConditionEditor.png)

>  Note: Now, you have configured your condition.

### 4) Map process inputs

1. Map the Process Inputs in Inputs tab for the step **“Get entity from EmpEmployment by key”** for files personIdExternal and userId and **Save**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/PersonaldExternal.png)

3. In General tab check if the destination is set, if not then Add **SFSFDestination** and **Save**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/SFSFDEstinationonGetEntity.png)

4. Enter the mapping for the next action field and **Save**. Add **emailNav,phoneNav,personalInfoNav,socialAccountNav** in **$expand** field. Check the destination and use the previous destination if it does not exist and **Save**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/PersonalIdonGetEntityfromPerPorson.png)

5. For Equipment Determination Decision, map the **Job Title** from the output of the step “Get entity from EmpEmployment by key” and **Save**. Do the same for **Training determination**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/JobTitle.png)

6. For “Equipment and Training Request Approval Form” , add the **personIdExternal** from Process Inputs to the Subject and also update the users to receive the task in my inbox by using ad167-XXX@education.cloud.sap (replace XXX with your ID). Click **Save**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/SBPAStep11.png)

7. For the Create Purchase Order for Laptop, check the destination is set as for **S4HANADestination**.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/SBPAStep12.png)

8. For approved and rejected email notifications, please enter your email id to receive the email.

>  Note: Now, your project inputs are mapped. 

### 5)	Release and Deploy

Check the final project looks like following and has no errors. Release and Deploy the project to an environment name **AD167_SFSF**. Note that the deployment is successful.

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/FullProcessRelease.png)

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/release.png)

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/deploy.png)

## Summary

At the end of this exercise, you should have configured, released and deployed the SAP Build Process Automation (SBPA) project to manage the approval workflow for equipment and training of newly hired employee.

Continue to [Exercise 2 - Add a New Employee in SAP SuccessFactors](../ex2/README.md)

