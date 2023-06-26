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

