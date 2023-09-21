
Conceptual E/R $\longrightarrow$ $\qquad \begin{array}{rcl} \text{Logical} \\ \text{Relational} \\ \text{Model}\end{array}$$\qquad\longrightarrow$ $\qquad \begin{array}{rcl} \text{Physical} \\ \text{SQL}\end{array}$


$R \subseteq A\times B$ $\qquad \qquad \begin{array}{rcl} A=\{3,5,8\} \\ B=\{b,d,w\} \end{array}$

$R=\{(3,b),(3,w),(5,w),(8,d)\}$

Databases: $R\subseteq D_1 \times D_2 \times D_3 \times \; ... \; \times D_n$

A relation: $R(f_1:D_1 , f_2:D_2 \; ... \; f_n:D_n)\; \leftarrow$ Schema of a relation (static)


![[Pasted image 20230921003251.png]]

### Common Domains

Basically the type of values you store.

- `int`
- `float, double`
- `char(n)` $\leftarrow$ n can not change. Good for instances of known char lengths (i.e. US phone numbers or SSNs)
- `varchar(n)` $\leftarrow$ Strings with a variable in length. For example, `varchar(5)` allows <u>up to</u> 5 characters.

- `date`
- `time`
- `datetime`
- `boolean`

Example: `Students(sid:int, name:varchar(50), dob:date, address:varchar(100))

<u>Properties</u>

- r-ity: number of fields
- cardinality: number of tuples
- relations are sets. No duplicates
	Results are relations to real life. Result sets might have duplicates. 

<u>Integrity Constraints</u> (keeps instances in a consistent state.)

- Domain constraints (Reject, Modified to satisfy the constraints)
- Primary Key Constraint (No Duplicates)
	Relational Model:
		Primary key(_ , _ , _ )

Example: 

`Enrolled_in(sid:int, courseid:char(10), grade:(varchar(2), primarykey(sid,cid))`