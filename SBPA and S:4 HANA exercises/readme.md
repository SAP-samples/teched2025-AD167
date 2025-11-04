## Scenario Introduction

**Billing block** is applied in Sales Order by internal sales representatives to prevent invoice being created in case of sales returns. These billing blocks need to be updated or deleted in random or on-demand fashion and is time critical activity in Order-to-Cash process. In many organisation this process is still manual where internal sales representatives get billing block change requests in form of Excel or Email attachment. Sales representatives download these attachments and then sales orders are manually updated in the S/4HANA system based on data in the excel files or attachments.


## Overview

This session introduces attendees how to modify or extend standard business processes from SAP S/4HANA. Leveraging SAP Build Process Automation and SAP Build Work Zone, advanced edition services of SAP Build solutions to enhance the experience of managing billing block status change in SAP S/4HANA cloud.

In this scenario: <br>
- Sales order is created in SAP S/4HANA
- Billing block is updated in the sales order
- Billing Block Status Changed event is thrown by SAP S/4HANA
- SAP Event Mesh is configured to listen and communicate events
- Process is triggered to approve the changes in SAP Build Process Automation
- Sales Order (A2X) API is used to get and patch sales order details in the backend system
- Finally, sales representative is informed once the sales orders are updated


## Solution Architecture
 ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20S%3A4%20HANA%20exercises/ex1/images/S4HANAArchitecture.png)
