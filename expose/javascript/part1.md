1. values added:  20
2. final result:  20
3. We should not use var because its scope is not limited to the block that it is in, but the entire function. This can make variables available outside the block where you expected them to stay hidden, which can cause confusion in program behavior. 
4. values added:  20
5. Line 13 led to a ReferenceError. This is because the variable 'result' was declared using let which means that it is restricted to the scope of the block. This means that it does not exist outside of the if statement, and therefore cannot be referenced on line 13 which is outside that block.
6. The program never reaches line 9 because it reaches an error at line 7. This is because we defined result with the const keyword which means that its value cannot be changed, yet we attempt to change it on line 7 where we do 'result = num1 + num2'. This leads to the error: TypeError: Assignment to constant variable.
7. The program also does not reach line 13 for the same reason as listed in the answer for question 6.
