In case that you have a lot of metadata in your organization (classes, pages, triggers, objects etc.) it is hard to select only few of them in Force IDE as it freeze for longer time on metadata list selection when you search for names. Therefore if you know already name of needed components it is possible to compose package.xml manually. 

This can be also useful if you are preparing package for deployment
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
	<version>29.0</version>
</Package>
```

2. Possible type names and members name format.
Based on force API version 33.

http://pawelwozniak.info/index.php/salesforce-com/deployments/132-preparing-package-xml-manually
