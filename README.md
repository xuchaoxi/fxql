# X Database

## reference
---
* [CS346 Spring 2015](https://web.stanford.edu/class/cs346/2015/)

## fxql commands
---
* help;                         --> show fxql commands
* create database test;         --> create a database named test
* drop database test;           --> drop a database named test
* cd database;                  --> select(change) a database
* create table test(attr int);  --> create a table name test has attr type int
* drop table test;              --> drop a table named test
* create index table(attr);     --> create index on table attr
* drop index table(attr);       --> drop index on table attr
* show;                         --> show relations
* show table;                   --> show attributes
* load test("filename");        --> load data from filename to table test
* dump test("filename");        --> dump data to filename from table test
* print test;                   --> print all tuples of table test
* ls;                           --> list databases
* ls database;                  --> list tables

## SQL
---
### CREATE

* create table nation(n\_nationkey i, n\_name c25);
* create index nation(n\_nationkey);

## DROP

* drop index nation(n\_nationkey);

## SELECT

* select * from nation;
* select * from nation where n\_nationkey < 10;
* select * from nation, region where n\_regionkey = r\_regionkey and r\_regionkey=1;
* select n\_nationkey, n\_name, n\_regionkey, r\_regionkey from nation, region where n\_regionkey=r\_regionkey;
* select * from nation limit 5;
### Aggregation
* select min(n\_nationkey) from nation;
* select max(n\_nationkey) from nation;
* select count(n\_nationkey) from nation;
* select avg(n\_nationkey) from nation;

## DELETE & UPDATE

* delete from nation where n\_nationkey=1;
* insert into nation values(25, "CHINA", 0, "hasjxbsbcsdbc ibnsdjcbjdf");
* update nation set n\_nationkey=26 where n\_nationkey=25;
