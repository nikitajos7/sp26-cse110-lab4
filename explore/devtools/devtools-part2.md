# DevTools Part 2

## 1
The bug was that the input values were treated as strings instead of numbers. Because of this, the + operator performed string concatenation instead of addition.

## 2
The fix is to convert the inputs to numbers before adding them.

Fix: let result = Number(num1) + Number(num2);