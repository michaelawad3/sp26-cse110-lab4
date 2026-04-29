1. What was the bug?
The bug was that using the '+' operator on will concatenates them rather adding them. Therefore, the "1" + "2" becomes "12."

2. How would you fix it?
We would need to cast the variables to Number() to make sure that we are working on numbers that can therefore be added.

```javascript
function calculateSum(num1, num2) {
    let result = Number(num1) + Number(num2);
    return result;
}