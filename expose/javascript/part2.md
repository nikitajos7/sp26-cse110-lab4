1. Line 12 prints: 3 Because i was declared using var, it is function-scoped. After the loop finishes, i has incremented to 3, so it can still be accessed outside the loop.
   
2. Line 13 causes a ReferenceError. discountedPrice was declared using var inside the for loop body, but since var is function-scoped, it is accessible in the function. However, in the code, discountedPrice exists after the loop and its final value is from the last iteration. It prints: 150
   
3. Line 14 prints: 150 finalPrice was declared with var, so it is function-scoped. Its final value after the last loop iteration is 150.
   
4. The function returns: [50, 100, 150] Each price is multiplied by 1 - discount, so with a discount of 0.5, each price is cut in half.

5. Line 12 causes a ReferenceError. i was declared with let inside the for loop, so it is only accessible inside the loop.

6. Line 13 causes a ReferenceError. discountedPrice was declared with let inside the loop body, so it cannot be accessed outside the loop body.

7. Line 14 causes a ReferenceError. finalPrice was declared with let inside the loop body, so it cannot be accessed outside the loop body.

8. The function returns: [50, 100, 150] Even though discounted, discountedPrice, and finalPrice are declared with let, they are used within the correct scopes. The returned array contains the discounted prices.

9. Line 11 causes a ReferenceError. i was declared with let inside the loop, so it is not accessible outside the loop.

10. Line 12 prints: 3 length was declared with const in the function scope, so it can be accessed inside the function after the loop.

11. The function returns: [50, 100, 150] discounted is declared with const, but the array itself can still be mutated with .push(). const only prevents reassignment of the variable, not modification of the object or array it refers to.

12. 
    A. Accessing the value of the name property: student.name

    B. Accessing the value of the Grad Year property: student["Grad Year"]

    C. Calling the greeting function: student.greeting()

    D. Accessing the name property inside Favorite Teacher: student["Favorite Teacher"].name

    E. Accessing index zero in courseLoad: student.courseLoad[0]

13. 

    A. '3' + 2 Output: "32" Because + with a string performs string concatenation.

    B. '3' - 2 Output: 1 Because - converts the string "3" to the number 3.

    C. 3 + null Output: 3 Because null converts to 0.

    D. '3' + null Output: "3null" Because + with a string converts null to a string.

    E. true + 3 Output: 4 Because true converts to 1.

    F. false + null Output: 0 Because false converts to 0 and null converts to 0.

    G. '3' + undefined Output: "3undefined" Because + with a string converts undefined to a string.

    H. '3' - undefined Output: NaN Because undefined converts to NaN in numeric operations.

14. 
    A. '2' > 1 Output: true The string "2" is converted to the number 2.

    B. '2' < '12' Output: false Both values are strings, so JavaScript compares them lexicographically. "2" is greater than "1".

    C. 2 == '2' Output: true == allows type conversion, so "2" becomes 2.

    D. 2 === '2' Output: false === checks both value and type. One is a number and the other is a string.

    E. true == 2 Output: false true converts to 1, and 1 == 2 is false.

    F. true === Boolean(2) Output: true Boolean(2) is true, so this compares true === true.


15. == checks equality after allowing type conversion. === checks strict equality, meaning both the value and type must match. In general, === is safer because it avoids unexpected automatic conversions.

17. The result is: [2, 4, 6] modifyArray loops through [1, 2, 3]. For each element, it calls doSomething. Since doSomething(num) returns num * 2, the new array becomes [2, 4, 6].

19. The output is:
1
4
3
2
First, 1 prints immediately. Then the first setTimeout schedules 2 after 1000 ms. The second setTimeout schedules 3 after 0 ms, but it still runs after the current synchronous code finishes. Then 4 prints immediately. After that, 3 prints, and finally 2 prints after about one second