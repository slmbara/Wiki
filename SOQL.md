## Get case information:
```
SELECT id, casenumber, account.Num_abonne__c, ownerid, owner.name, createddate from case where owner.profile.name = 'Interface' and account.entiteVisibilite__c = 'APA' and owner.name != 'InterfaceSINIARD' limit 50
```

### get information from  Account:
```
select id, entiteVisibilite__c, Profile__c  from Account where Num_abonne__c = '0018111948'
```
