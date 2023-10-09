
![[Pasted image 20231009123615.png]]


`Employee(eID:int, name:varchar(20), primary key (eID))`

`manages(mgr_eID:int, suboord_eID:int, from:date, till:date, primary key(mgr_eID, subord_eID), foreign key (mgr_eID, subord_eID) references Employee)`