
<u>Draw an E-R Diagram for:</u> 

Employees work for departments
	- Departments have an id, address, name, phone.
	- Employees have a ssn, name, phone, dob
	- Each employee cannot work for more than one department
	- Each department can have many employees. 


![[Pasted image 20230921131853.png]]



The arrow points from "Employee" to "works_for," indicating each Employee works for one Department (cardinality of 1 on the Employee side).