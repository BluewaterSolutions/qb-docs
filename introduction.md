
## Introduction

Quick's database query builder provides a convenient, fluent interface to creating and running database queries. It can be used to perform most database operations in your application and works on all supported database systems.

The Quick query builder uses PDO parameter binding to protect your application against SQL injection attacks. There is no need to clean strings being passed as bindings.

In order to use `qb` you will need to import the component or use wirebox to make it accessible.


```
// WireBox Directly
query = wirebox.getInstance('Builder@qb');
var getAllResults = query.from('users').get();


// Coldbox
component {
	property name="query" inject="id:Builder@qb";
	function demo(event,rc,prc){
		var getResults = query.from('users').get();
	}
}
```


