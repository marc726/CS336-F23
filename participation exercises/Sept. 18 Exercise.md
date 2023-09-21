
![[Pasted image 20230921132602.png]]

1) Add Attributes 
2) Argue why it is not ill-conceived 
3) Use reification to transform it into binary relationships.

##### 1) Add Attributes 

**Parts**
	-pID (PK)
	-name
	-material

**Maker**
	-mID (PK)
	-Name
	-Location

**Project**
	pID(PK)
	Name
	Budget

(*This isn't a one size fits all. There can be additional or different attributes, however, must have PK*)

##### 2) Argue why it is not ill-conceived 

The ER diagram provides a structured and logical representation of a supply chain system, involving entities like "Parts," "Makers," and "Projects," along with their relevant attributes. The "Supplies" relationship effectively captures the dynamic interactions between parts and makers, supporting tracking and auditing. The design is both scalable and flexible, allowing for easy extensions or modifications to meet evolving requirements. Overall, it serves as a well-conceived foundation for database implementation and is understandable to both technical and non-technical stakeholders.

##### 3) Use reification to transform it into binary relationships.


Without attributes:

![[Pasted image 20230921135557.png]]

With attributes:

![[Pasted image 20230921135423.png]]

