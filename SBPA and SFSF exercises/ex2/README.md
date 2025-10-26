# Exercise 2 - Add a New Employee in SAP SuccessFactors

In this exercise, you will test the integration scenario by adding a new employee in the SAP SuccessFactors application.

## Exercise

Run through the following steps:
1.	Logon to the [SAP SuccessFactors](https://hcm-us10-sales.hr.cloud.sap/login?company=SFEDU033158) application using the user ID and password provided to you by the instructors. Example user id is AD167-XXX@education.cloud.sap, where XXX is your user ID.


2.	Search for Add New Employee and select Add New Employee list entry and this would bring us to the Add New Employee Wizard.
   ![alt text](https://github.com/SAP-samples/teched2025-AD167/blob/main/SBPA%20and%20SFSF%20exercises/ex1/images/sfstep2.png)

3.	In the Identity section, enter the following details:
**[!IMPORTANT] ** Replace XXX with the participant number that is assigned to you.
   3.1 Hire Date: Keep the default current date
   3.2 Company: From the drop down list - Ace India (ACE_IND) 
Event Reason: From the drop down list - New Hire (HIRNEW)
First Name: Any name of your choice
Last Name: Any name of your choice
Date Of Birth: Select any date, e.g.: Oct 18, 2000
Country Of Birth: Select any country, e.g.: India
Person Id: IN264-XXX
User Name: IN264-XXX




## Exercise 2.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex2/images/02_02_0010.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
