# ex02b
1. Candidate Keys
    1. PetName
    1. OwnerEmail
1. Functional Dependencies
    1. PetName -> (PetType, PetBreed, PetDOB, Service, Date, Charge, OwnerEmail)
    1. OwnerEmail -> (OwnerFirstName, OwnerLastName, OwnerPhone)
    
OwnerEmail | PetName | PetType | PetBreed | PetDOB | Service | Date | Charge
---------- | ------- | ------- | -------- | ------ | ------- | ---- | ------
Marsha.Downs@somewhere.com | King | Dog | Std. Poodle | 02/27/14 | Ear Infection | 08/17/16 | $65 
Richard.James@somewhere.com | Teddy |Cat | Cashmier | 02/01/13 | Nail Clip | 09/05/16 | $27.5 
Marsha.Downs@somewhere.com | Filo | Dog | Std. Poodle | 07/17/15 | ------- | ----- | ------ 
Liz.Frier@somewhere.com | AJ | Dog | Collie Mix | 05/05/15 | One Year Shots | 05/05/16 | $42.5
Richard.James@somewhere.com | Cedro | Cat | Unknown | 06/06/12 | Nail Clip | 09/05/16 | $27.5
Richard.James@somewhere.com | Woolley | Cat | Unknown | Unknown | Skin Infection | 10/03/16 | $35
Miles.Trent@somewhere.com |Buster | Dog | Border Collie | Laceration Repair | 10/05/16 | $127
Hilary.Evans@somewhere.com | Jiddah | Cat | Abyssinian | 07/01/08 | Booster Shots | 11/04/16 | $111

OwnerEmail | OwnerLastName | OwnerFirstName | OwnerPhone  
---------- | ------------- | -------------- | ---------- 
Marsha.Downs@somewhere.com | Downs | Marsha | 201-823-5467 
Richard.James@somewhere.com | James | Richard | 201-735-9812 
Liz.Frier@somewhere.com | Frier | Liz | 201-823-6578 
Miles.Trent@somewhere.com | Trent | Miles | 201-634-7865 
Hilary.Evans@somewhere.com | Evans | Hilary | 201-634-2345 
