# 1.0 INTRODUCTION TO DBMS

`Topics To Study`

- E-R Diagram
- Conversion of E-R diagram into relational model
- Basics of relational model and functional dependency
- Idea about keys/types
- Normalization ( INF - BCNF )
- Lossless decomposition and dependency preserving
- Indexing and Physical Structures
- SQL , RA , RC
- Transaction
- concurrency control

# 1.1 Difference between Data, Information, DB, DBMS

`DATA`
Raw and isolated facts about an entity(recorded) e.g text, music, video, etc.

`Information`
Processed, meaningful, usable data is information. It also depends on users perspective. 

`DataBase`
collection of similar/related data

`DBMS`
software or tool used to create, manipulate and delete database.

# 1.2 Disadvantages Of File Processing System

- Data Redundancy <br>
  same data may be stored in multiple locations

- Data Inconsistency <br>
  if same data is present at many locations if something happens such that at one location the data is changed but at other it is not it leads to data inconsistency.

- Difficulty in accessing data <br>
  in normal file structures it is hard to access data if the data is large

- Data isolation <br>
  means if you require some specific data for e.g names of people having account balance less than 10000 how will you find in folder structure it is hard.
- Security Problem <br>
- Atomicity Problem <br>
  Problem of inconsistent transaction means either all the instructions should be executed or neither e.g your money is debited but recharge is not done. so to avoid 
  this dbms is used
- Concurrent-users anomalies <br>
  if many users have to use data at same time e.g bank, railway booking, etc.
- Integrity <br>
  some triggers like if account balance is less than 1000 cut 100 rupees , maximmum 4 daily transactions such complex functions are possible only with dbms.
  
# 1.3 OLAP Vs OLTP
Historical data is also useful for us to predict and design something to know the behaviour from past data.But if we put current operational data and historical data in same database it will become slow and no one wants that. So it is important to put OLAP and OLTP seperate and here are some of the differences.

| OLAP <br> ( online analytical processing ) | OLTP  <br> ( online transaction processing ) |
|---|---|
| Historical data  | current data   |
| Subject oriented | application oriented   |
| decision making  | day to day operations   |
|general size (TB , PB)   | general size (MB , GB)   |
|CEO , MD ,GM   | clerks, managers   |
| R  | R/W  |


