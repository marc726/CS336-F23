Marc Rizzolo
mtr120
### Employee 

`Employee(Ssn:char(11), Bdate:date, Fname:varchar(20), MInit:char(1), Lname:varchar(20), sex:varchar(6), Address:varchar(100), salary:integer, primary key(Ssn))`

`Supervision(supervisorSsn:char(11), employeeSsn:char(11), primary key(supervisorSsn,employeeSsn), foreign key(employeeSsn) references Employee)`

`Dependent(Ssn:char(11), Name:varchar(50), Sex:varchar(6), BirthDate:date, Relationship:varchar(20), primary key(Ssn, Name), foreign key(Ssn) references Employee)`

We then combine `Employee` and `Supervision` because of the one to many relationship

`EmployeeWithSupervision(Ssn:char(11), SupervisorSsn:char(11), Bdate:date, Fname:varchar(20), MInit:char(1), Lname:varchar(20), sex:varchar(6), Address:varchar(100), salary:integer, primary key(Ssn), foreign key(Ssn) references employee)`

We will then combine `Dependent` to `Employee` because of the one to many relationship

`EmployeeWithDependent(Ssn:char(11), DependentName:varchar(50), Bdate:date, Fname:varchar(20), MInit:char(1), Lname:varchar(20), sex:varchar(6), Address:varchar(100), salary:integer, DependentSex:varchar(6), DependentBirthDate:date, DependentRelationship:varchar(20), primary key(Ssn, DependentName))`

---

<div style="page-break-after: always;"></div>

### Department

`Department(Name:varchar(50), Number:integer, Locations:varchar(50), primary key(Name,Number))`

`Controls(ProjName:varchar(50), ProjNumber:integer, DeptName:varchar(50), DeptNumber:integer, primary key(ProjName, DeptName, ProjNumber, DeptNumber) foreign key(ProjName, ProjNumber) references Project)`

We will then combine `Department` and `Controls` because of the one to many relationship.

`DepartmentControl(ProjName:varchar(50), ProjNumber:integer, DeptName:varchar(50), DeptNumber:integer, Locations:varchar(50), primary key(ProjName, ProjNumber, DeptName, DeptNumber), foreign key(ProjName, ProjNumber) references Project)`

##### Next, we look at the relations `Manages` and `Works_For`

###### `Manages`:
We will combine the relation `Manages` with entity `Department` due to the total participation on the one-to-one. 

`DepartmentManages(DeptName:varchar(50), DeptNumber:integer, Ssn:char(11), StartDate:date, primary key(DeptName, DeptNumber), foreign key(Ssn) references Employee)`

###### `Works_For`:

`Works_For(DeptName:varchar(50), DeptNumber:integer, Ssn:char(11), primary key(DeptName,DeptNumber), foreign key(Ssn) reference Employee)`

We will combine the relation `Works_For` with entity `Department` due to the total participation on the one-to-many. 

`DepartmentEmployee(Name:varchar(50), Number:integer, Locations:varchar(50), Ssn:char(11), primary key(Name, Number, Ssn), foreign key(Ssn) references Employee)`



---

<div style="page-break-after: always;"></div>

Thus the Relational Model using the merge rule is simplified to the below:

`Project(Name:varchar(20), Number:integer, Location:varchar(50), primary key(Name, Number))`

`SupervisorToEmployee(SupervisorSsn:char(11), EmployeeSsn:char(11), Bdate:date, Fname:varchar(20), MInit:char(1), Lname:varchar(20), sex:varchar(6), Address:varchar(100), salary:integer, primary key(SupervisorSsn), foreign key(EmployeeSsn) references employee)`

`EmployeeWithDependent(Ssn:char(11), DependentName:varchar(50), Bdate:date, Fname:varchar(20), MInit:char(1), Lname:varchar(20), sex:varchar(6), Address:varchar(100), salary:integer, DependentSex:varchar(6), DependentBirthDate:date, DependentRelationship:varchar(20), primary key(Ssn, DependentName))`

`DepartmentProjectControl(ProjName:varchar(50), ProjNumber:integer, DeptName:varchar(50), DeptNumber:integer, Locations:varchar(50), primary key(ProjName, ProjNumber, DeptName, DeptNumber), foreign key(ProjName, ProjNumber) references Project)`

`DepartmentManages(DeptName:varchar(50), DeptNumber:integer, Ssn:char(11), StartDate:date, primary key(DeptName, DeptNumber), foreign key(Ssn) references Employee)`

`DepartmentEmployee(Name:varchar(50), Number:integer, Locations:varchar(50), Ssn:char(11), primary key(Name, Number, Ssn), foreign key(Ssn) references Employee)`

`Works_On(Ssn:char(11), Name:varchar(20), Hours:float, primary key(Ssn), foreign key(Name) references Project)`