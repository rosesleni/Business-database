# Business-database
Business database
![dd](https://user-images.githubusercontent.com/72918495/103275341-f07a4d80-49fe-11eb-8a83-46f0d19edf5e.png)

This Database is all about creating business records for all your employees. From this you are able to create,or to see all the records of your company and also in your employees you can easily record and add all the personal things about your employee.The data collected on your business acts as a check up, alerting you to what needs to be tended to immediately.Consistent data collection is vital to a business because it communicates the ongoing performances of that business. The performances being tracked help to demonstrate where a business is currently at and where the business will be positioned in the future, based on information being gathered. 


Table name and Description:
   i.Employee-This table shows all the personal details and information  of all workers.

   ii.Department - This table shows every department details.

  iii.department-manager- This table shows all records of employees where they started work.

 iv. -Salary- showing all records and details of their salaries.
 
Database Dependency Diagram

![ERD image](https://user-images.githubusercontent.com/72918495/103279845-c67a5880-4a09-11eb-8baa-ea8bce14cfb7.png)

1.QUERY 
       i. Description:Particular employee maximum salary details
       
   ii.Why is it important:This is the of of the important query that is show becuse if you want to have specifect output like salries.
     
   Sample output:
  ** 
   SELECT sal1.* FROM salaries AS sal1 LEFT JOIN salaries AS sal2 ON (sal1.emp_no = sal2.emp_no AND sal1.from_date < sal2.from_date) WHERE sal2.from_date IS NULL and sal1.emp_no = 10001;
   
   ![query10](https://user-images.githubusercontent.com/72918495/103329073-1dc60a80-4a96-11eb-99bb-6dacff4f7e67.png)

2.QUERY 
       i. Description:
       
   ii.Why is it important:
   
   
   iii: sample output:
   
   Select emp.emp_no, emp.first_name, emp.last_name, sal.salary, sal.from_date from employees emp inner join (select emp_no, MAX(salary) as salary, from_date from salaries group by emp_no) sal on (emp.emp_no = sal.emp_no) limit 10;
   
   ![query11](https://user-images.githubusercontent.com/72918495/103330287-c460da00-4a9b-11eb-935f-0f3dafbf0553.png)


3.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:
  
 SELECT MAX(salary) FROM salaries WHERE salary NOT IN ( SELECT Max(salary) FROM salaries);
 
4.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:
   Select emp.emp_no, emp.first_name, emp.last_name, sal.salary, sal.to_date from employees emp inner join (select emp_no, MAX(salary) as salary, to_date from salaries group by emp_no) sal on (emp.emp_no = sal.emp_no) limit 10;

5.QUERY 
       i. Description:
      ii.Why is it important:

   iii: sample output:
   
   SELECT first_name, hire_date 
FROM employees 
WHERE YEAR(hire_date)  LIKE '2018%';

   
6.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

7.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

8.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

9.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

10.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

11.QUERY 
       i. Description:
      ii.Why is it important:

   iii: sample output:
12.QUERY 
       i. Description:
      ii.Why is it important:

   iii: sample output:
13.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

14.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

15.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

16.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

17.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

18.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:

19.QUERY 
       i. Description:
      ii.Why is it important:

   iii: sample output:
   
20.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:


