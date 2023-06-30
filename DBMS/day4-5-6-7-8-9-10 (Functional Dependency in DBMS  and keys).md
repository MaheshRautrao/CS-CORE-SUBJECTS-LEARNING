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

      
   
    
  
  
