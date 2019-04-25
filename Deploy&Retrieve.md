# Retrieve des composants d'un organisation
Si vous avez beaucoup de métadonnées dans votre organisation (classes, pages, déclencheurs, objets, etc.), il est difficile de n'en sélectionner que quelques-unes car elles sont figées plus longtemps dans la sélection des listes de métadonnées lorsque vous cherchez des noms. Par conséquent, si vous connaissez déjà le nom des composants nécessaires, il est possible de composer package.xml manuellement. 

##Package.xml file structure.
```
<?xml version="1.0" encoding="UTF-8"?>
<Package xmlns="http://soap.sforce.com/2006/04/metadata">
	<types>
		<members>Class_name_controller</members>
		<name>ApexClass</name>
	</types>
	<types>
		<members>*</members>
		<name>ApexComponent</name>
	</types>
	<version>42.0</version>
</Package>
```
## Noms de type possibles et format de nom de membre.
http://pawelwozniak.info/index.php/salesforce-com/deployments/132-preparing-package-xml-manually

# Suppression de composants d'une organisation
Pour supprimer des composants, effectuez un déploiement avec le déployer()appel en utilisant un fichier manifeste de modifications destructives qui répertorie les composants à supprimer de votre organisation. 

Vous pouvez effectuer un déploiement qui ne supprime que des composants, ou un déploiement qui supprime et ajoute des composants. 

Dans l'API version 33.0 et ultérieure, vous pouvez spécifier les composants à supprimer avant et après l'ajout ou la mise à jour d'autres composants. 

Dans les versions antérieures de l’API, si des suppressions et des ajouts sont spécifiés pour le même déploiement, la déployer() L’appel effectue d’abord les suppressions.

Pour supprimer des composants, utilisez la même procédure que pour le déploiement de composants, mais incluez également un fichier de manifeste de suppression nommé destructiveChanges.xml et répertoriez les composants à supprimer dans ce manifeste. Le format de ce manifeste est identique à package.xml, sauf que les caractères génériques ne sont pas pris en charge.

Vous pouvez effectuer un déploiement qui spécifie les composants à supprimer dans destructiveChanges.xml et les composants à ajouter ou à mettre à jour dans package.xml:
* Pour supprimer des composants avant d' ajouter ou de mettre à jour d'autres composants, créez un fichier manifeste nommé destructiveChangesPre.xml et incluez les composants à supprimer.
* Pour supprimer des composants après avoir ajouté ou mis à jour d'autres composants, créez un fichier manifeste nommé destructiveChangesPost.xml et incluez les composants à supprimer.
```
<?xml version="1.0" encoding="UTF-8"?>
<Package xmlns="http://soap.sforce.com/2006/04/metadata">
    <types>
        <members>MyCustomObject__c</members>
        <name>CustomObject</name>
    </types>
</Package>
```








