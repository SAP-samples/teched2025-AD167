# Exercise 1 - Create Sales Order

In this exercise, you will create a Sales Order by referring to an existing Sales Order. This Sales Order will not have a billing block. Please note down the Sales Order number generated at the end of the exercise. This is needed later for designing the process and end-to-end testing.

## Level 2 Heading

After completing these steps you will have a Sales Order number created without a billing block.

1.	Logon to the S/4HANA system
   S/4HANA Cloud URL: https://my427029.s4hana.cloud.sap/ui
  	Username / Password: Login with your user id AD167-XXX@education.cloud.sap where XXX is your assigned user like 001 or 002 and so on and the password will be Acce$$teched25
  	
2. Search for va01 and click "Create Sales Order - VA01"
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/exercises/ex0/images/VA01.png)

3. Enter Order Type as “OR” and click on “Create with Reference”.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/exercises/ex0/images/EnterOR.png)

4. In the “Order” tab, enter Order as 3 and click on “Copy”.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/exercises/ex0/images/EnterSalesOrder.png)

5. In the “Review Availability Check” page, click “Apply”.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/exercises/ex0/images/ReviewAndApply.png)   

6. In “Create Standard Order:Overview” page enter a customer reference text and note that the “Billing Block” is blank.
This means there is no billing block on the Sales Order.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/exercises/ex0/images/EnterCustomerReference.png)

7. Click “Save” and note down the Sales Order number. We will use this later while designing and executing the end-to-end process.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/exercises/ex0/images/SaveSalesOrder.png)
   
## Summary

Now that you have created the Sales Order, Continue to - [Exercise 2 - Exercise 2 Description](../ex1/README.md)
