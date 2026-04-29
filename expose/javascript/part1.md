1. values added: 20
2. final result: 20
3. You should avoid using var because it is function-scoped instead of block-scoped. This can make variables accessible in places where you do not expect them, which can cause bugs and naming conflicts. let and const are safer because they follow block scope.
4. values added: 20
5. Line 13 causes a ReferenceError. result was declared with let inside the if block, so it cannot be accessed outside that block.
6. Line 9 causes a TypeError. result was declared with const, so it cannot be reassigned after being initialized to 0.
7. Line 13 does not run because the program already errors before reaching it. The error happens when the code tries to reassign the const result.
