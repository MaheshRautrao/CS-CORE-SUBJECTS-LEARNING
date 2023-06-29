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
         
  x ≤ R , y ≤ R   <br> 
  x --> y <br>
  Lets consider two tuples t1 and t2 in relation R <br>
  t1[x] = t2[x] <br>
  t1[y] = t2[y] <br>
  
 - Types <br>

   x --> y

   |trivial | non-trivial |
   |--------|-------------|
   |AB --> A  |     y ≤/ x  |
   |y ≤ x|   |
   
   here ≤/ means not less than equal to

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
   
    
  
  
