# Xdb

## reference
* https://web.stanford.edu/class/cs346/2015/#

## fxql commands

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

## query

* create table nation(n_nationkey i, n_name c25
* select * from nation;
* select * from nation where n_nationkey < 10;
* select * from nation, region where n_regionkey = r_regionkey and r_regionkey=1;
* select n_nationkey, n_name, n_regionkey, r_regionkey from nation, region where n_regionkey=r_regionkey;
* create index nation(n_nationkey);
* drop index nation(n_nationkey);
* delete from nation where n_nationkey=1;
* insert into nation values(25, "CHINA", 0, "hasjxbsbcsdbc ibnsdjcbjdf");
* update nation set n_nationkey=26 where n_nationkey=25;

## newly increased function

* select min(n_nationkey) from nation;
* select max(n_nationkey) from nation;
* select count(n_nationkey) from nation;
* select avg(n_nationkey) from nation;
* select * from nation limit 5;
