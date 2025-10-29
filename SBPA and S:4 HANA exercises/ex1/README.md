# Exercise 1 - Create Sales Order

In this exercise, you will create a Sales Order by referring to an existing Sales Order. This Sales Order will not have a billing block. Please note down the Sales Order number generated at the end of the exercise. This is needed later for designing the process and end-to-end testing.

## Exercise

After completing these steps you will have a Sales Order number created without a billing block.

1.	Logon to the S/4HANA system
   S/4HANA Cloud URL: https://my427029.s4hana.cloud.sap/ui
  	Username / Password: Login with your user id AD167-XXX@education.cloud.sap where XXX is your assigned user like 001 or 002 and so on and the password will be Acce$$teched25.
  	
2. Search for va01 and click **"Create Sales Order - VA01"**.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20S%3A4%20HANA%20exercises/ex1/images/S4step2.png)

3. Enter Order Type as **“OR”** and click on **“Create with Reference”**.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20S%3A4%20HANA%20exercises/ex1/images/S4step3.png)

4.	Click **"Order"** tab and enter **86612** in the dedicated Order field. Afterwards click on **"Copy"**.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20S%3A4%20HANA%20exercises/ex1/images/S4step4.png)

5.	Sales Order record will be opened. Type **“ref”** in the **Cust. Reference** field and click on **"Save"**. **Important** Please, note down the Sales Order number. We will use this later while designing and executing the end-to-end process..
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20S%3A4%20HANA%20exercises/ex1/images/S4step5.png) 

## Summary

Now that you have created the Sales Order, Continue to [Exercise 2 - Create Process](../ex2/README.md)

