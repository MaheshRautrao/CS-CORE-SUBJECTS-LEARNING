# Functional Dependancy

  fd : x -> y 

  this is not a mathematical functional dependancy means here for x we are not 
  computing y. <br>
  Here functional dependancy means for x we are searching y in relational table <br>

  | x | y|
  |---|--|
  |   |   |
  |    |   |

  Like mathematical functional dependancy for x only one value of y is there
  but for same value of y there may be multiple values of x <br>

  like f(x1) = y <br>
       f(x2) = y <br>
  but this is not possible <br>
       f(x) = y1 <br>
       f(x) = y2 <br>  

  More formal and mathematical defination :

for a relation R there are two attributes <br>

  | x | y|
  |---|--|
  |   |   |
  |    |   |
         
  x ⊆ R , y ⊆ R   <br> 
  x --> y <br>
  Lets consider two tuples t1 and t2 in relation R <br>
  t1[x] = t2[x] <br>
  t1[y] = t2[y] <br>
  
  ## Types 

   x --> y

   |trivial | non-trivial |
   |--------|-------------|
   |AB --> A  |     y ⊆/ x  |
   |y ⊆ x|   |
   
   here ⊆/ means is not subset of

 - example 1 : <br>

   there is a relation R

    |A|B|C|D|E|
    |-|-|-|-|-|
    |a|2|3|4|5|
    |2|a|3|4|5|
    |a|2|3|6|5|
    |a|2|3|6|6|

   a) A  --> BC ✔ <br>
   b) DE --> C ✔ <br>
   c) C  --> DE ❌ <br>
   d) BC --> A ✔ <br>

- example 2 : <br>

    |A|B|C|
    |-|-|-|
    |1|2|4|
    |3|5|4|
    |3|7|2|
    |1|4|2|

   ❌ a) A  --> B ❌ && BC --> A ✔<br>
   ❌ b) C --> B ❌  && CA --> B ✔<br>
   ✔  c) B --> C  ✔  && AB --> C ✔ <br>
   ❌ d) A --> C ❌  && BC --> A ✔<br>

- example 3 : <br>

    |X|Y|Z|
    |-|-|-|
    |1|4|2|
    |1|5|3|
    |1|6|3|
    |3|2|2|

   ❌ a) XY  --> Z ✔  && Z --> Y ❌ <br>
   ✔  b) YZ --> X  ✔  && Y --> Z ✔  <br>
   ❌ c) YZ --> X  ✔  && X --> Z ❌ <br>
   ❌ d) XZ --> Y ❌  && Y --> Z ✔  <br>

## Attribute closure / closure on attribute set / closure of attribute set

  Attribute closure of an attribute set 'A' can be defined as a set of attributes which can be functionally determined from it. Denoted by F^+ <br>
  example 1 : <br>

  R(ABC) <br>
  A --> B <br>
  B --> C <br>

  this means A --> BC <br>

  (A)<sup>+</sup> = A  = AB  = ABC <br>
      
  (A)<sup>+</sup> = ABC <br>
  
  example 2 : <br>
  
  R(ABCDEF) <br>
  A --> B <br>
  C --> DE <br>
  AC --> F <br>
  D --> AF <br>
  E --> CF <br>

  (D)<sup>+</sup> = D = ADF = ABDF <br>
        
  (D)<sup>+</sup> = ABDF <br>

  (DE)<sup>+</sup> = DE  = ADEF = ABCDEF <br>
             
  (DE)<sup>+</sup> = ABCDEF <br>     

  
## Armstrong's Axioms and Inference Rules in Functional Dependency

   Axiom is a statement that is taken to be true and serve as a premise or starting point for further arguments <br>
   Armstrong axiom holds an every relational database can be used to generate closure set <br>

   - Primary rules

     - Reflexivity : if Y ⊆ X then X-->Y  <br>
     - Augmentation : if X --> Y then XZ --> YZ <br>
     - Transitivity : if X --> Y && Y --> Z then X --> Z <br>

   - Secondary rules

     - Union : if X --> Y && X --> Z then X -->YZ <br>
     - Decomposition : if X --> YZ then X --> Y && X --> Z <br>
     - Pseudo transitivity : if X --> Y && WX --> Z then WX --> Z  <br>
     - Composition : if x --> Y && Z --> W then XZ -->YW <br>

     ## Closure set of attributes examples

     - example 1 : <br>

       R ( ABCDEFG ) <br>

       1. A --> B 
       2. BC --> DE 
       3. AEG --> G

          (AC)<sup>+</sup> = AC = ABC = ABCDE <br>
          (AC)<sup>+</sup> = ABCDE <br>


       R ( ABCDE ) <br>

       1. A --> BC
       2. CD --> E
       3. B --> D
       4. E --> A
       
          (B)<sup>+</sup> = B = BD <br>
          (B)<sup>+</sup> = BD <br>

       R ( ABCDEF ) <br>

       1. AB --> C
       2. BC --> AD
       3. D --> E
       4. CF --> B
       
          (AB)<sup>+</sup> = AB = ABC = ABCD = ABCDE <br>
          (AB)<sup>+</sup> = ABCDE <br>

       R ( ABCDEFGH ) <br>

       1. A --> BC
       2. CD --> E
       3. E --> C
       4. D --> AEH
       5. ABH --> BD
       6. DH --> BC
      
          BCD --> H ?? Is it a valid functional dependancy <br>
          if BCD Contain H in its closure set then yes.
       
          (BCD)<sup>+</sup> = BCD = BCDE = ABCDEH So yes it is a functional dependancy.
      
 ## Equivalance of functional dependancy
 
 ## 3.6 Equivalence Of Functional Dependencies
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/8f18b675-5888-49ae-8c21-325d5c3bd9c6" width="600px" >
 
 ## 3.7 Equivalence Of Functional Dependencies Examples
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/de435ba5-19c3-4fe1-9516-e3db082bb118" width="400px" >
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/ec4076eb-267d-46eb-87e1-caa4ad391ce2)" width="400px" >
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/bcc2ee81-d9cc-4236-ae54-cfb9e84fbbec" width="400px" >
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/612cabde-1120-405f-bf89-176df2b8458f" width="400px" >
 
 ## 3.8 Minimal Cover or Canonical Cover or Irreducible set of Functional Dependencies
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/c0426030-1d3e-4376-a04f-e21636951872" width="600px" >

 ## 3.9 Practice questions on Minimal Cover or Canonical Cover or Irreducible set
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/7243e782-cac7-45a0-a424-00d957b887a7" width="400px" >
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/e32197cd-0f73-4b2f-a999-093ed8667de1" width="400px" >
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/7efe0fb3-6adc-4d26-abf4-fcf9baae457e" width="400px" >
 <img src="https://github.com/MaheshRautrao/CS-CORE-SUBJECTS-LEARNING/assets/101188065/74552d9e-5e11-4020-a859-7a3a504d9181" width="400px" >

  
