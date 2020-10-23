# CosmosDB Workshop - Server side Programming

## Exercise 1 - Create User defiened Function
1. Create a UDF which takes ZIP code as an input and return state name. Use below data to implement your function.
  * State: CA, Zip Range: (90001-96162)
  * State: NY, Zip Range: (10001-14975)
  * State: WA, Zip Range: (98001-99403)
  * State: FL, Zip Range: (32004-34997)
  * State: TX, Zip Range: (75001-75501)

2. Write a SQL query to return Familyname, Zip, State, StateUsingFunction and compare the values of States returned by function and stored in document.

3. Create a UDF which takes a string and regular expression as inputs and if string matches the expression return true else return false.

4. Write SQL query using above UDF which returns families with names ending with 'Family'.
  * Query should return the data for WakefieldFamily, MeyerAndFamily and AndersenFamily.
