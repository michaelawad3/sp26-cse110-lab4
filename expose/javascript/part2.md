1. Line 12 prints 3. This is because the variable i was defined with i which means that it is not limited to the block (the for loop) so can be used in the anywhere in the function. Since the 'prices' array has length 3, the for loop terminates with i = 3, and so when we console.log(i), we print out 3.
2. Line 13 prints out 150. This behavior is due to the same explanation in question 1. Since discountedPrice was declared with the keyward var, it can be accessed outside the for loop block. The last calculation that was done for discountedPrice when before the for loop terminated was 300 * 0.5 which is 150. Thus, when we print out discountedPrice on line 13, we get 150.
3. Line 14 prints 150 for the same as 1 and 2. It is declared with var and thus can be used anywhere in the function. Its last calculation in the for loop was Math.round(150 * 100) / 100 which equals 150. Therefore when the for loop terminates, it holds the value 150, which gets printed on line 14.
4. The function returns an array of the same length as prices, with values from prices with the applied specificed discount to each value. With the call 'discountPrices([100, 200, 300], 0.5)' it returns [50, 100, 150].
5. Line 12 led to a ReferenceError: i is not defined. This is because we defined i in the for loop with the keyword 'let'. This means it only exists in the scope of the for loop, and thus it cannot be referenced outside of that block where we tried to use it on line 12.
6. Line 13 led to a ReferenceError: discountedPrice is not defined for the same reason. Since discountedPrice was created in the for loop with let, it cannot be referenced outside of that block in the console.log statement on line 13.
7.  Line 14 printed 150. This is because even though finalPrice was declared with the keyword 'let', its location encapsulates the scope of the entire function. Therefore, it does not generate an error on line 14. Its exact value contains the same logic as seen in question 3. 
8.  The function returns [50, 100, 150]. It goes through each price in [100, 200, 300], multiplies it by (1 - 0.5), which is 0.5, then rounds the result and adds it to the discounted array. It maintains the same functionality as before because the let variables are used within their proper scopes.
9.  Line 11 led to a ReferenceError: i is not defined. This is because we defined i in the for loop with the keyword 'let'. This means it only exists in the scope of the for loop, and thus it cannot be referenced outside of that block where we tried to use it on line 11.
10. Line 12 prints 3. This is because even though length was declared with the keyword 'const', its location encapsulates the scope of the entire function. Therefore, it does not generate an error on line 12.
11. The function returns [50, 100, 150]. It stores the array length as 3, loops through each price, calculates each discounted price using price * (1 - 0.5), and pushes those values into the discounted array. There is no error because discounted is a const array, but its contents can still be changed with .push().
12. 
    A. Accessing the value of the name property in the student object: `student.name`

    B. Accessing the value of the Grad Year property in the student object: `student['Grad Year']`

    C. Calling the function for the greeting property in the student object: `student.greeting()`

    D. Accessing the name property of the object in the Favorite Teacher property in student: `student['Favorite Teacher'].name`

    E. Access index zero in the array of the courseLoad property of the student object: `student.courseLoad[0]`

13.  Arithmetic

    A. `'3' + 2` outputs `'32'` because the `+` operator combines values as strings when one value is a string.

    B. `'3' - 2` outputs `1` because the `-` operator converts `'3'` into the number `3`.

    C. `3 + null` outputs `3` because `null` converts to `0`.

    D. `'3' + null` outputs `'3null'` because `+` does string concatenation when one value is a string.

    E. `true + 3` outputs `4` because `true` converts to `1`.

    F. `false + null` outputs `0` because `false` converts to `0` and `null` converts to `0`.

    G. `'3' + undefined` outputs `'3undefined'` because `+` does string concatenation with the string `'3'`.

    H. `'3' - undefined` outputs `NaN` because `undefined` converts to `NaN` in numeric operations.

14. Comparison

    A. `'2' > 1` outputs `true` because `'2'` converts to the number `2`.

    B. `'2' < '12'` outputs `false` because both are strings, so JavaScript compares them lexicographically.

    C. `2 == '2'` outputs `true` because `==` allows type conversion.

    D. `2 === '2'` outputs `false` because `===` checks both value and type.

    E. `true == 2` outputs `false` because `true` converts to `1`, and `1 == 2` is false.

    F. `true === Boolean(2)` outputs `true` because `Boolean(2)` is `true`, so both sides are the same value and type.

15. Difference Between `==` and `===`

    `==` checks for equality after converting values to similar types, which can sometimes give surprising results. `===` checks both value and type without conversion, so it is usually safer and more predictable.
16. Code in part2-question16.js
17. The result will be `[2, 4, 6]`. The `modifyArray` function loops through `[1, 2, 3]` and calls the callback function `doSomething` on each number. Since `doSomething` multiplies each number by `2`, the new array becomes `[2, 4, 6]`.
18. Code in part2-question18.js
19. The output is:

1

4

3

2

This happens because `1` and `4` are logged immediately. Then `setTimeout` with `0` milliseconds logs `3` after the current code finishes running. Finally, `setTimeout` with `1000` milliseconds logs `2` after about one second.