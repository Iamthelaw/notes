# Graduation FAQ

## SQL / Postgresql
1. DBA1/DBA2 Postgres
2. Transactions & [ACID](https://en.wikipedia.org/wiki/ACID)
3. Transaction isolation levels

## Python
1. Internals of Context Manager
2. Abstract class vs Interface
3. Hashable objects and hash function
4. Descriptors with practical examples

## Django
1. QuerySet internal api
2. `iterator()` method
3. [Caching QuerySets](https://docs.djangoproject.com/en/1.11/topics/db/queries/#caching-and-querysets)
3. [When querysets are not cached](https://docs.djangoproject.com/en/1.11/topics/db/queries/#when-querysets-are-not-cached)
4. Composing QuerySets for sub-query
5. Select related vs Prefetch related
6. When querysets are evaluated:
	* __Iteration__. A QuerySet is iterable, and it executes its database query the first time you iterate over it.
	* __Slicing__. Slicing an unevaluated QuerySet usually returns another unevaluated QuerySet, but Django will execute the database query if you use the “step” parameter of slice syntax, and will return a list.
	* __Pickling/Caching__
	* __repr()__
	* __len()__
	* __list()__
	* __bool()__
7. F-expressions:
	* in filters
	* in annotations
	* race conditions
8. Examples of Q-expressions
9. Func / Aggregate expressions
10. RawSQL expressions | extra
11. `update()`, `select_for_update()`, `in_bulk()`
12. `django.db.connections`
13. Reusable django applications

## ExtJS, JavaScript
1. Form layouts in ExtJs
2. Context stack of call / apply / bind

## OOP
1. Detailed examples of S.O.L.I.D. principles in Python
2. Internals of `_protected` and `__private` in Python
3. OOP patterns:
	* Strategy
	* Template
	* Fabric
	* Singleton
	* Observer
	* Adapter

## Algorithms
1. Calculating complexity of algorithm
2. Algorithm complexity
3. Basic algorithm complexities with examples in Python
4. Algorithms comparision by complexity
5. Add / substract algorithm complexity
