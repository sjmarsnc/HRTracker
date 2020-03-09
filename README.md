# Employee Manager

## Useage 

This application uses data in a mySQL server to store employee information and allows
the user to perform common Human Resources tasks such as adding and removing an employee, setting up new departments and job roles, changing salaries, etc.  

List of tasks you can do: 
* Display all employees in a table 
* Display all employees sorted by department
* Display all employees sorted by manager 
* Display all departments
* Display all roles 
* Display the sum of all salaries in all departments 
* Add an employee
* Add a department
* Add a role 
* Remove an employee
* Remove a role
* Remove a Department 
* Update the role of an employee
* Update the manager of an employee
* Update the salary associated with a role 

The data is stored in tables with keys linking them as shown below:  

![](/schema.png)


## Implementation 

This version uses async / await extensively to avoid nested calls, based on review in class.  I modified it more to avoid calls to the database every time I need to list roles, people, or department.  I build that array at startup, and then rebuild any time an item is added or deleted from one of those types.   

It could still use a few enhancements like checking for duplicate names of roles and departments and catching those errors.  

