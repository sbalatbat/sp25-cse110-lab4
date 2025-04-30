# Lab 4 Expose: Part 1. A Quick Introduction...

1. `values added:  20`
2. `final result:  20`
3. We should not use `var` because it gives the variable declared with it full function scope regardless of which block it is declared in. This can cause conflicts when we want to use the same variable name for different things between code blocks.
4. `values added:  20`
5. Nothing is printed by line 13. Instead, a ReferenceError occurs with the explanation `result is not defined`. Since the variable `result` is defined using the `let` keyword in a block excluding line 13, line 13 does not have access to the `result` variable, thus the program runs as though that variable doesn't exist, leading to an error.
6. Nothing is printed by line 9. Instead, a TypeError occurs with the explanation `Assignment to constant variable`. Since the variable `result` is defined using the `const` keyword, its value cannot be reassigned after it was initially defined. Line 7 attempts to reassign `result` to the value `num1 + num2` after being intially defined as `0`, causing an error at line 7 and no subsequent prints.
7. Nothing is printed by line 13. The TypeError at line 7 previously explained in question 6 remains in place, leading to no subsequent prints.