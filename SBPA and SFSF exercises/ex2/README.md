# Exercise 2 - Add a New Employee in SAP SuccessFactors

In this exercise, you will test the integration scenario by adding a new employee in the SAP SuccessFactors application.

## Exercise

Run through the following steps:
1.	Logon to the [SAP SuccessFactors](https://hcm-us10-sales.hr.cloud.sap/login?company=SFEDU033158) application using the user ID and password provided to you by the instructors. Example user id is AD167-XXX@education.cloud.sap, where XXX is your user ID.


2.	Search for Add New Employee and select Add New Employee list entry and this would bring us to the Add New Employee Wizard.
<br>![](/exercises/ex1/images/sfstep2.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```



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
