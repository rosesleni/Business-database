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

(https://user-images.githubusercontent.com/72918495/103279845-c67a5880-4a09-11eb-8baa-ea8bce14cfb7.png)
##1.QUERY 
       i. Description:Particular employee maximum salary details
       
   ii.Why is it important:This is the most important query that is shown because if you want to have specific output like salaries.
     
   iii: Sample output:
   SELECT sal1.* FROM salaries AS sal1 LEFT JOIN salaries AS sal2 ON (sal1.emp_no = sal2.emp_no AND sal1.from_date < sal2.from_date) WHERE sal2.from_date IS NULL and sal1.emp_no = 10001;
   
  (https://user-images.githubusercontent.com/72918495/103329073-1dc60a80-4a96-11eb-99bb-6dacff4f7e67.png) 
 ##2.QUERY 
       i. Description: This query show Employee and Salary table join to display the salary of the individual
       
   ii.Why is it important:It is important for me bacause its shows 
   
   iii: sample output:
   Select emp.emp_no, emp.first_name, emp.last_name, sal.salary, sal.from_date from employees emp inner join (select emp_no, MAX(salary) as salary, from_date from salaries group by emp_no) sal on (emp.emp_no = sal.emp_no) limit 10;
   
(https://user-images.githubusercontent.com/72918495/103330287-c460da00-4a9b-11eb-935f-0f3dafbf0553.png)
##3.QUERY 
       i. Description:It show here is the Second largest salary
      ii.Why is it important: It is important to have this because it shows who is the one of your employees with the highest salaries. 

   iii: sample output:
  
 SELECT MAX(salary) FROM salaries WHERE salary NOT IN ( SELECT Max(salary) FROM salaries);
 
 (https://user-images.githubusercontent.com/72918495/103330755-cb88e780-4a9d-11eb-97a0-5267194df575.png)
 
 ##4.QUERY 
     i. Description: In this output shows the details of salaries.
         
   ii.Why is it important: Important to have details to you Salaries also to all employees that you have.
   
   iii: sample output:
    Select emp.emp_no, emp.first_name, emp.last_name, sal.salary, sal.to_date from employees emp inner join (select emp_no, MAX(salary) as salary, to_date from salaries group by emp_no) sal on (emp.emp_no = sal.emp_no) limit 10;
   
(https://user-images.githubusercontent.com/72918495/103330760-cd52ab00-4a9d-11eb-84bf-2594359130bb.png)
##5.QUERY 
        i. Description:  show the details in your company work on date.

 ii.Why is it important: The importance of this showing how it simply shows all workers work in and out.
iii: sample output:
   SELECT first_name, hire_date 
FROM employees 
WHERE YEAR(hire_date)  LIKE '2018%';
![query8](https://user-images.githubusercontent.com/72918495/103330749-c9bf2400-4a9d-11eb-87be-cbdc616b13c1.png)
##6.QUERY 
   i. Description: In this query shows the list of the employee and the hired date.
ii.Why is it important: It is important to show all the list employees for you to have an idea to their details. 

iii: sample output:
   Select 
    first_name, last_name,hire_date
FROM
    employees
WHERE
    EXISTS( SELECT 
            1
        FROM
            employees
        WHERE
           employees.first_name = employees.first_name);
![query7](https://user-images.githubusercontent.com/72918495/103330747-c9bf2400-4a9d-11eb-93c7-5323a4ee14e2.png)
##7.QUERY 
  i. Description:In this query display all the information of the employees whose salary is within the range 3000..

   ii.Why is it important: The importance of this is to show salary like you want to direct to show your salaries
   
 iii: sample output:
   Select * from salaries  where salary> all(select salary  from salaries where salary<3000);
   
![query4](https://user-images.githubusercontent.com/72918495/103330744-c88df700-4a9d-11eb-9e9a-953cf108f379.png)
##8.QUERY 
  i. Description:this query showing list employee numbers and theirs who have  the biggest salary.
     
 ii.Why is it important: Importance of this is showing details to every employee.

iii: sample output:
   Select emp_no,max(salary) from salaries group by emp_no;
   
![query6](https://user-images.githubusercontent.com/72918495/103330746-c9268d80-4a9d-11eb-91fa-82b03d3ff90d.png)

##9.QUERY 
   i. Description: this query shows the employee personal details.
       
 ii.Why is it important: importance of this is to have a  list of your employees. 

iii: sample output:
   Select first_name,last_name FROM `employees` WHERE 1 
![query3](https://user-images.githubusercontent.com/72918495/103330743-c7f56080-4a9d-11eb-956e-e6bcf383e59a.png)

 ##10.QUERY 
  i. Description:This query shows how to count your employees. 
       
ii.Why is it important: This is Important because if you don't have an idea how to count your employee you can use this query to have your list.
      
iii: sample output:
   Select count(*) from employees;
   
![query14](https://user-images.githubusercontent.com/72918495/103330757-ccba1480-4a9d-11eb-9757-6be66f6e0583.png)

##11.QUERY
i. Description:This query shows employee  number and dates.
 ii.Why is it important:Need only the entry for the employees latest data.

iii: sample output:
    Select  dept_no,from_date 
FROM dept_manager; 

![query1](https://user-images.githubusercontent.com/72918495/103330741-c62b9d00-4a9d-11eb-9144-32073b5ebe73.png)

##12.QUERY 
        i. Description:This query shows employees gender,name.
        
  ii.Why is it important: this is important because if you want to know your employees gender and names.
  
iii: sample output:
   Select first_name,gender 
       FROM employees;
![1](https://user-images.githubusercontent.com/72918495/103336349-dd28ba00-4ab2-11eb-8349-c0466e116c23.png)

##13.QUERY 
      i. Description: this query shows direct details from employees this shows all lists of every department code number.
   ii.Why is it important: Is It important for you to show and to pick up all the details from said company.
   
  iii: sample output:
    Select dept_no,emp_no from dept_manager;
   
![2](https://user-images.githubusercontent.com/72918495/103337119-3b569c80-4ab5-11eb-9e57-ec5f6cc93028.png)

   
##14.QUERY 
        i. Description: This query shows a limited list of employees.
      ii.Why is it important: This query shows if you want to have a list and limit the name of employee list,details. 
      
   iii: sample output:
   select first_name from employees limit 5; 
   ![query15](https://user-images.githubusercontent.com/72918495/103330759-cd52ab00-4a9d-11eb-831b-a31ce67af81a.png)

##15.QUERY 
       i. Description: this query is Another example to show your details.
      ii.Why is it important: these examples, we can easily use sql limit clause. 
      
   iii: sample output:
   select * from employees limit 1;
   ![query13](https://user-images.githubusercontent.com/72918495/103330756-cc217e00-4a9d-11eb-89a1-10c5a9cb71c0.png)


##16.QUERY 
       i. Description:
       
   ii.Why is it important:
      
   iii: sample output:
   SELECT * FROM employees WHERE first_name LIKE 'A%'
   ![3](https://user-images.githubusercontent.com/72918495/103339056-56c4a600-4abb-11eb-9e2c-c1ff77f9716c.png)

##17.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:
##
18.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:
   
##19.QUERY 
       i. Description:
      ii.Why is it important:

   iii: sample output:
   
 ##20.QUERY 
       i. Description:
      ii.Why is it important:
      
   iii: sample output:


