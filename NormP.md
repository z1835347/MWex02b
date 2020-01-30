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

# ex02b
1. Candidate Keys
    1. PetName
    1. OwnerEmail
2. Functional Dependencies
    1. PetName -> (PetType, PetBreed, PetDOB, Service, Date, Charge, OwnerEmail)
    1. OwnerEmail -> (OwnerFirstName, OwnerLastName, OwnerPhone)
    
PetName | OwnerEmail | PetType | PetBreed | PetDOB | Service | Date | Charge
---------- | ------- | ------- | -------- | ------ | ------- | ---- | ------
King | Marsha.Downs@somewhere.com | Dog | Std. Poodle | 02/27/14 | Ear Infection | 08/17/16 | $65 
Teddy |Richard.James@somewhere.com |  Cat | Cashmier | 02/01/13 | Nail Clip | 09/05/16 | $27.5 
Filo |Marsha.Downs@somewhere.com |  Dog | Std. Poodle | 07/17/15 | ------- | ----- | ------ 
AJ |Liz.Frier@somewhere.com |  Dog | Collie Mix | 05/05/15 | One Year Shots | 05/05/16 | $42.5
Cedro |Richard.James@somewhere.com |  Cat | Unknown | 06/06/12 | Nail Clip | 09/05/16 | $27.5
Woolley |Richard.James@somewhere.com |  Cat | Unknown | Unknown | Skin Infection | 10/03/16 | $35
Buster | Miles.Trent@somewhere.com | Dog | Border Collie | Laceration Repair | 10/05/16 | $127
Jiddah | Hilary.Evans@somewhere.com | Cat | Abyssinian | 07/01/08 | Booster Shots | 11/04/16 | $111

OwnerEmail | OwnerLastName | OwnerFirstName | OwnerPhone 
---------- | ------------- | -------------- | ---------- 
Marsha.Downs@somewhere.com | Downs | Marsha | 201-823-5467 
Richard.James@somewhere.com | James | Richard | 201-735-9812 
Liz.Frier@somewhere.com | Frier | Liz | 201-823-6578 
Miles.Trent@somewhere.com | Trent | Miles | 201-634-7865 
Hilary.Evans@somewhere.com | Evans | Hilary | 201-634-2345 
