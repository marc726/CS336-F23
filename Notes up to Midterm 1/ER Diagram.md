### Diagram

![[Pasted image 20230920205512.png]]

set = no dups

![[Pasted image 20230920205734.png]]
Primary keys are used as a unique identifier for each entity in a set. 

### Cardinality

![[Pasted image 20230920211318.png]]

"One course is taught by many professors."
### ISA Relationships


![[Pasted image 20230920211848.png]]



![[Pasted image 20230920212634.png]]

### Weak Entity Sets

- Does not have own primary key
- Gets primary key from an identifying relation

Denoted by: 
![[Pasted image 20230920213006.png]]

Example of weak entity set in ER:

![[Pasted image 20230920213608.png]]

Weak Entity sets also have relationship entries which are noted by: 

![[Pasted image 20230921005607.png]]



![[Pasted image 20230920214432.png]]

![[Pasted image 20230920215117.png]]

### Reification

Reification refers to the process of turning a relationship into an entity.

Example:

We will turn "enrolled in" from the relationship into an entity. 

![[Pasted image 20230920220949.png]]

Enrollment is a weak entity and therefore the relationships "enrolls thru" & "is for" are also weak because they involve the weak entity "Enrollment."

This is typically used when you want to add attributes to the relationship. For example: Grade or Enrollment date. 

### Participation 

A bolded line connecting an entity set to a relationship set indicates <u>total participation</u>. This means that every instance of that entity <u>must</u> participate in the relationship.

![[Pasted image 20230920222618.png]]

**Example w/ Reification:**

![[Pasted image 20230920222300.png]]

![[Pasted image 20230920222528.png]]

### Hierarchy 


![[Pasted image 20230920235532.png]]



![[Pasted image 20230921001046.png]]


* No isbn because we went from relationship to weak entity. A weak entity has what’s called a “partial key”. It’s one or more attributes that uniquely identify a weak entity for a given owner entity.
* Book can have two primary keys to help uniquely identify it. 