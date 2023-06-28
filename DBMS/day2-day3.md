# 2.0 E-R Diagram

### topics to study
- Introduction ans Basics
- Entity and entity list
- attributes and types
- relationship
- strong and weak entity set
- traps
- conversion

## 2.1 Introduction and basics

--> E-R Diagrams were introduced by Peter Chen in 1976. <br>
--> A non-technical design method works on conceptual level based on the perception
of real world. <br>
--> Consists of collection of basic objects called entities and of relationships 
among these objects and attributes which defines their properties. <br>
--> Free from attributes and provides a standard and logical way of visualizing
data. <br>
--> Basically it is a diagrammatic representation easy to understand even by non-technical users. <br>
--> e.g
![Screenshot 2023-06-26 115927](https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/1c9260b5-71b4-4964-a81c-bd23381127b6)

## 2.2 Entity and entity list

- Entity : <br>
  An entity is a thing or an object in the real world that is distinguishable from other objects based on the values
  of the attributes is possess. <br>
- Types of Entities :
  1. Tangible --> Entities which physically exist in real world. <br>
     e.g car, pen, bank_locker. <br>

  2. Non-tangible --> Entities which exists logically <br>
     e.g bank account. <br>
     
- Entity set : <br>
  Collection/set of same types of entities i.e. that share same properties or attributes called entity set.

- Example explanation

--> Entity can not be represented in an E-R diagram as it is instance/data ( understand carefully ) <br>
--> Entity is represented by rectangel in E-R diagram. <br>
--> If you carefully see student is not the entity ( see sentence no 1. ) <br>

![Screenshot 2023-06-26 122841](https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/9fcf7e94-6f65-4daa-9f4c-4045094a5e08)

--> Entity can be represented in an relational model by row, tuple, record. <br>
--> Entity set is represented by table in relational model. <br>
--> Actually if we understand carefully entity set is like schema or structure and entity is the instance of schema. <br>

`Studet` entity set. 

| Roll No. | name | age |
|----------|------|-----|
| 1 | mahesh | 20 |
| 2 | pavan | 21 |
| 3 | shree | 22 |

--> Here student is entity set which is like schema and each instance is a entity.

## 2.3 Types of Attributes

--> Attributes are the units that describe the characteristics of the entities. <br>
--> For each attribute there is set of permitted values called domains. <br>
--> In E-R diagram they are represented by oval or ellipse and in relational model by seperate column. <br>

` Types `

| simple-composite | single-multivalued | stored-derived |
|------------------|--------------------|----------------|
|--> simple : can not be divided further. e.g roll number <br> --> composite : can be further divided. e.g name into first name, last name. <br> --> simple is represented by simple oval connected to rectangle but composite is represented as oval connected to oval. |--> single valued can have only one value at a instance of time <br>--> multivalued can have more than one value <br>--> e.g : roll number is single valued but phone number is multivalued. <br>--> multivalued is represented as oval in oval in E-R diagram and as a seperate table in relational model using primary key. |--> stored : value is stored in database e.g date of birth. <br>--> derived : value is computed at runtime using the stored attribute. <br>--> derived is shown by dotted oval in E-R diagram and as a normal column in reational model. |

## 2.4 Relationship in an ER Diagram

- Relationship : <br>
  It is an association between two or more entities of same or different entity set <br>
  --> no representation in E-R diagram as it is an instance or data. <br>
  --> In relational model represented either using a row in a table. <br>

- Relationship type/set : <br>
  a set of similar type of relationship <br>
  --> In E-R diagram it is represented using diamond.<br>
  --> In relational model either by a seperate table or by seperate column (foreign key) <br>

- Every relationship type has three components <br>

  - Name
  - Degree
  - Cardinality ratio / Participation constraints

<img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/6b1190c2-fd81-4356-8bac-cd810f4982fa"  width="600" >

## 2.5 Degree of a Relationship in a ER Diagram

   Means number of entity set associated (participated) in the relationship set. <br>
   --> Most of relationship sets in the E-R diagram are binary (industry). Occasionally however relationship sets involve more than two entity sets. <br> 
   
   - Unary : <br>
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/f326b6d8-4050-4e13-9424-d51ce4331c88"  width="600" >
   
   - Binary : <br>
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/55dddfbd-1791-4ed2-9186-32fe6424c229"  width="600" >
  
   - Tertiary : <br>
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/055331c6-e61d-4fbe-9b79-651dcf5b166a"  width="600" >
 
   - Quaternary : <br>
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/e3beb8a6-7add-4b38-81c8-3acdde8563ae"  width="600" >

   - N-ary : <br>
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/59b83fa3-b555-4455-ac49-f66d2fe5c510"  width="600" >
   
## 2.6 Mapping Cardinalities and Cardinality Ratio in ER diagram

   Express the numebr of entities to which often entity can be related vai a relationship. <br>
   --> can be used in describing relationship set of any degree but is most useful in binary relationship

   - 1:1 (one to one)
   - 1:N (one to many)
   - N:1 (many to one)
   - M:N (many to many)

     NOTE : Here one means not exactly one it means at most one and n means at most n (think carefully so if no one is related to no one it is okay)
   
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/9f4755f3-02e5-4979-bbdf-5e02f674c594"  width="400" height="300">
   
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/71117ede-0041-4154-b6ae-662675accbaf"  width="400" height="300">
   
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/7cf4cb08-4109-40d4-901a-a533e024e5d0"  width="400" height="300">
   
   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/12e06ace-0451-4227-9d95-fed85dc887b7"  width="400" height="300">

   <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/4d3b5ec2-cae9-432b-928f-dc4ce1a09c12"  width="400" height="300">
   
   
## 2.7 Participation Constraints in E-R Diagram

   Specifies whether the existance of an entity depends on its being related to another entity via a relationship type. <br>
   These constraints specify the minimum and maximum number of relationship instances that each entity can or must participate in. <br>

   - Maximum cardinality : <br>
     It defines the maximum number of times an entity occurance participating in a relationship. <br>

   - Minimum cardinality : <br>
     It defines the minimum number of times an entity occurance participating in a relationship. <br>

   - Partial participation : if the minimum cardinality is 0 then there may be someone who is not participating so it means partial participation. <br>

   - Total participation : if the minimum cardinality is > 0 then all have to participate at least once so it means total participation. <br>

   - different representations : <br>
     e.g project has min cardinality of 3 and maximum of 15 and employee has min 0 and max 2. <br>
     
     ![Screenshot 2023-06-28 095311](https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/d591eab8-2473-4d45-bf8c-846855a52c16)
