## Get case information:
```
SELECT id, 
casenumber, 
account.Num_abonne__c, 
ownerid, owner.name, 
createddate from case 
where owner.profile.name = 'Interface' 
and account.entiteVisibilite__c = 'APA' 
and owner.name != 'InterfaceSINIARD' limit 50
```

### get information from  Account:
```
select id, entiteVisibilite__c, Profile__c  from Account where Num_abonne__c = '0018111948'
```

### Recupérer un poin de vente
```
select id, horairesOuverture__c  from Point_de_vente__c where LastModifiedDate >= 2019-03-01T00:00:00+00:00
```
```
select count(id), CreatedBy.Username from RaffraichementEnCours__c where Service_name__c= 'EDA'  AND CreatedDate>= 2019-04-11T00:00:00-00:00 AND CreatedDate <= 2019-04-12T00:00:00-00:00 group by  CreatedBy.Username
```
```
SELECT DeveloperName,Id,Name,OwnerId FROM Report WHERE CreatedDate > 2019-04-01T23:01:01-08:00
```
```
SELECT Id,Name, Owner.Name, CreatedBy.UserRole.Name FROM Report WHERE CreatedBy.UserRole.Name = 'AGA_DIR'
```
