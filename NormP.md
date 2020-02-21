# MWex02b
Normalization Process
1. Identify all the candidate keys of the relation
2. Identify all the functional dependencies in the relation
3. Examine the determinants of the functional dependencies. If any determinant is not a candidate key, the relation is not well formed. In this case:
    
    a.Place the columns of the functional dependency in a new relation of their own.
    
    b. Make the determinant of the functional dependency the primary key of the new relation.
    
    c. Leave a copy of the determinant as a foreign key in the original relation.
    
    d. Create a referential integrity constraint between the original relation and the new relation
4. Repeat step 3 as many times as necessary until every determinant of every relation is a candidate key. 

1. Candidate Keys
    1. PetName
    1. OwnerEmail
2. Functional Dependencies
    1. PetName -> (PetType, PetBreed, PetDOB, Service, Date, Charge, OwnerEmail)
    1. OwnerEmail -> (OwnerFirstName, OwnerLastName, OwnerPhone)
    
PetName | OwnerEmail | PetType | PetBreed | PetDOB | Service | Date | Charge | OwnerID
---------- | ------- | ------- | -------- | ------ | ------- | ---- | ------ | -------
King | Marsha.Downs@somewhere.com | Dog | Std. Poodle | 02/27/14 | Ear Infection | 08/17/16  | $65 | 2
Teddy |Richard.James@somewhere.com |  Cat | Cashmier | 02/01/13 | Nail Clip | 09/05/16 | $27.5 | 1
Filo |Marsha.Downs@somewhere.com |  Dog | Std. Poodle | 07/17/15 | ------- | ----- | ------ 
AJ |Liz.Frier@somewhere.com |  Dog | Collie Mix | 05/05/15 | One Year Shots | 05/05/16 | $42.5 | 3
Cedro |Richard.James@somewhere.com |  Cat | Unknown | 06/06/12 | Nail Clip | 09/05/16 | $27.5 |1
Woolley |Richard.James@somewhere.com |  Cat | Unknown | Unknown | Skin Infection | 10/03/16 | $35 | 1
Buster | Miles.Trent@somewhere.com | Dog | Border Collie | Laceration Repair | 10/05/16 | $127 | 4
Jiddah | Hilary.Evans@somewhere.com | Cat | Abyssinian | 07/01/08 | Booster Shots | 11/04/16 | $111 | 5

OwnerID | OwnerEmail | OwnerLastName | OwnerFirstName | OwnerPhone 
------- | ---------- | ------------- | -------------- | ----------
1 | Richard.James@somewhere.com | James | Richard | 201-735-9812 
2 | Marsha.Downs@somewhere.com | Downs | Marsha | 201-823-5467 
3 | Liz.Frier@somewhere.com | Frier | Liz | 201-823-6578 
4 | Miles.Trent@somewhere.com | Trent | Miles | 201-634-7865 
5 | Hilary.Evans@somewhere.com | Evans | Hilary | 201-634-2345 

PetName | Service | Date | Charge | OwnerID	
King | Ear Infection | 17-Aug-16 | $65.00 | 2
Teddy | Nail Clip | 5-Sep-16 | $27.50 | 1
AJ	| One Year Shots | 5-May-16 | $42.50 | 3
Cedro | Nail Clip | 5-Sep-16 | $27.50 | 1
Woolley	| Skin Infection | 3-Oct-16 | $35.00 | 1
Buster | Laceration Repair | 5-Oct-16 | $127.00 | 4
Jiddah | Booster Shots | 4-Nov-16 | $111.00 | 5

Since an owner may have more than one pet, we added a more simplistic primary than OwnerEmail, OwnerID. A corresponding Surrogate key was added to the pet services table as well to link the two to the owner table

