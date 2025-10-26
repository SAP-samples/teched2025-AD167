# Exercise 1 - Create and Configure the SAP Build Process Automation Project for Equipment and Training Approval Workflow

## Overview
In this exercise, you will be setting up a SAP Build Process Automation (SBPA) project to manage the approval workflow for equipment and training of newly hired employees in SuccessFactors. This workflow will be initiated directly by SuccessFactors Integration once a new hire record is created. For the sake of that exercise you will be working with a predefined project where you would need to add additional steps and mapping. 

1) [Create a new project based on the given "New Hire Onboarding Experience – Template" project and save it](#1create-a-new-project-based-on-the-given-new-hire-onboarding-experience--template-project-and-save-it)<br>
2) [Add parallel branches to add new Equipment and Training determination rules](#2add-parallel-branches-to-add-new-equipment-and-training-determination-rules)<br>
3) [View the Equipment Determination decision for the newly hired employee](#3view-the-equipment-determination-decision-for-the-newly-hired-employee)<br>
4) [View the Training Determination decision for the newly hired employee](#4view-the-training-determination-decision-for-the-newly-hired-employee)<br>
5) [Configure approval form inputs to the data from equipment and training decisions](#5-configure-approval-form-inputs-to-the-data-from-equipment-and-training-decisions) <br>
6) [Consume Actions project to publish the approval event to Advanced Event Mesh(AEM)](#6consume-actions-project-to-publish-the-approval-event-to-advanced-event-meshaem) <br>
7) [Release and Deploy](#7release-and-deploy)<br>
8) [Get the Process Instance ID](#8get-the-process-instance-id)<br>

### 1)	Create a new project based on the given "New Hire Onboarding Process TEMPLATE" project and save it. 

1.	First you need to copy a template project that have some predefined steps. Go to the Lobby and find New Hire Onboarding Process TEMPLATE. From the tree dot button Options select Save as New Project. Copy the editable version of the project (New Hire Onboarding Process TEMPLATE) from lobby by adding your username at the end - DO NOT USE THIS PROJECT OR EDIT THIS, please copy and change the 
description

2.	Once copied, open the project and find the New Employee Equipment and Training Approval Process in the Artifacts list. Open the process. 

![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/Choose%20event%20collection.png)

### 2)	Add event trigger as a starting point of your process

1. In the process builder canvas click on Add a Trigger.

2. Select Wait for an Event.

3. Type New Hire Data Review Initiated in the search field of the library. Once listed, you can click on Add.

4. In the trigger editor add you session ID and user ID the to the suggested trigger’s name and then click on Create. 

>  Note: Now, you have your trigger created. 

### 3)	Map process inputs



### 4)	View the Training Determination decision for the newly hired employee


### 5)	 Configure approval form inputs to the data from equipment and training decisions

 

### 6)	Consume Actions project to publish the approval event to Advanced Event Mesh(AEM)


### 7)	Release and Deploy


### 8)	Get the Process Instance ID

## Summary

At the end of this exercise, you should have configured, released and deployed the SAP Build Process Automation (SBPA) project to manage the approval workflow for equipment and training of newly hired employee.

Continue to -

