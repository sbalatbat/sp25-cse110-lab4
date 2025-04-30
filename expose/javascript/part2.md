# Lab 4 Expose: Part 2. A Little More of a Challenge...

1. Line 12 prints out `3`. There are 3 elements in the list passed into the function, which the `for` loop iterates over. The `i` variable got incremented to `3` as each element was iterated over. Due to the `var` keyword being used to define `i`, this variable has function scope instead of block scope, allowing it to be accessed and printed.
2. Line 13 prints out `150`. The variable `discountedPrice` defined with the `var` keyword, giving it function scope rather than block scope. At the end of the `for` loop, `discountedPrice` was calculated as `300 * (1 - 0.5)`, which is equal to `150`. Although the `for` loop terminates shortly after, due to having function scope, the variable was accessed and printed anyway.
3. Line 14 prints out `150`. The variable `finalPrice` was defined with the `var` keyword, giving it function scope rather than block scope. At the end of the `for` loop, `finalPrice` was calculated as `(300 * 100) / 100`, which is equal to `150`. Although the `for` loop terminates shortly after, due to having function scope, the variable was accessed and printed anyway.
4. This function will return a list of discounted prices. At the start of the function, `discounted` is instantiated as an empty list with the keyword `var`, giving the variable function scope. Throughout the `for` loop, the `discount` parameter was applied to the list of `prices` passed into the function, and the discounted final prices were added to the `discounted` list. Line 16 returns `discounted`, which now contains those calculated discounted final prices.
5. At line 12, a ReferenceError occurs, with the explanation `i is not defined`. Since `i` was defined with the `let` keyword, it had block scope within the `for` loop block only. Once the `for` loop terminates, the variable `i` is no longer accessible because the block it was declared in has terminated, thus it doesn't exist as a variable at this point in the program, leading to this error.
6. At line 13, a ReferenceError occurs, with the explanation `discountedPrice is not defined`. Since `discountedPrice` was defined with the `let` keyword, it had block scope within the `for` loop block only. Once the `for` loop terminates, the variable `discountedPrice` is no longer accessible because the block it was declared in has terminated, thus it doesn't exist as a variable at this point in the program, leading to this error.
7. Line 14 prints out `150`. The variable `finalPrice` was defined using the `let` keyword at function level at the beginning of the function. As the `for` loop ran, `discountedPrice` is defined as `300 * (1 - 0.5)` at the 3rd iteration and `finalPrices` is defined as `(300 * 100) / 100`, i.e., `150`. Since it was defined at function level, `finalPrices` was accessible as a variable at line 14, and is printed.
8. This function will return a list of discounted prices. At the start of the function, `discounted` is instantiated as an empty list with the keyword `let`, giving the variable function scope. Throughout the `for` loop, the `discount` parameter was applied to the list of `prices` passed into the function, and the discounted final prices were added to the `discounted` list. Line 16 returns `discounted`, which now contains those calculated discounted final prices.
9. At line 11, a ReferenceError occurs, with the explanation `i is not defined`. Since `i` was defined with the `let` keyword, it had block scope within the `for` loop block only. Once the `for` loop terminates, the variable `i` is no longer accessible because the block it was declared in has terminated, thus it doesn't exist as a variable at this point in the program, leading to this error.
10. Line 12 prints out `3`. The variable `length` was defined with the `const` keyword at the fuction level, giving it block scope within the function. It was assigned once to the length of the `prices` parameter, which is a list of 3 elements at the function call in line 17. Since it has function scope, it was accessible at line 12 and printed out.
11. This function will return a list of discounted prices. At the start of the function, `discounted` is instantiated as an empty list with the keyword `const`, giving the variable function scope and prohibiting it from being reassigned. Since `discounted` is a list, its contents can be changed using its modifying methods and without reassignment of the variable. Throughout the `for` loop, the `discount` parameter was applied to the list of `prices` passed into the function, and the discounted final prices were added to the `discounted` list. Line 16 returns `discounted`, which now contains those calculated discounted final prices.
12. Object: student
    - A. `student.name`
    - B. `student['Grad Year']`
    - C. `student.greeting()`
    - D. `student['Favorite Teacher'].name`
    - E. `student.courseLoad[0]`
13. Arithmetic
    - A. `'3' + 2 = '32'` The integer `2` maps to a string representation of itself, `'2'` which is concatenated to `'3'` hence leading to `'32'`.
    - B. `'3' - 2 = 1` The string `'3'` is converted to its number representation, `3`, then the subtraction takes place, leading to `1`.
    - C. `3 + null = 3` The keyword `null` is converted to `0` through numeric conversion and then added to `3`, leading to `3`.
    - D. `'3' + null = '3null'` The keyword `null` is converted to its string representation then concatenated to `'3'` leading to `'3null'`.
    - E. `true + 3 = 4` The boolean `true` is converted to `1` through numeric conversion and then added to `3`, leading to `4`.
    - F. `false + null = 0` The boolean `false` and the keyword `null` are both converted to `0` through numeric conversion then added, leading to `0`.
    - G. `'3' + undefined = '3undefined'` The keyword `undefined` is converted to its string representation then concatenated to `'3'` leading to `'3undefined'`.
    - H. `'3' - undefined = NaN` Both the string `'3'` and keyword `undefined` are converted to `3` and `NaN` respectively by number conversion. Proceeding with the subtraction leads to `NaN` because of `undefined` being converted to `NaN`.
14. Comparison
    - A. `'2' > 1 = true` The string `'2'` is converted to `2` through numeric conversion, which is greater than `1` so the comparison resolves to `true`.
    - B. `'2' < '12' = false` The strings are compared lexicographically at every position. At the first position, `'2'` is greater than `'1'` because `'2'` has a greater lexicographic value, so the comparison immediately terminates and resolves to `false`.
    - C. `2 == '2' = true` JavaScript converts the values to numbers in comparisons with different types, so `'2'` becomes `2`, resolving the comparison to `true` since 2 is equal to itself.
    - D. `2 === '2' = false` This comparison uses a strict equality, which compares without type conversion, resolving this automatically to `false` since they are different types.
    - E. `true == 2 = false` The boolean `true` is converted to `1` by numeric conversion, which is not equal to `2`, resolving this to `false`.
    - `true === Boolean(2) = true` Following boolean conversion, `2` is "nonempty" so it converts to true. Under strict comparison, the boolean `true` is equal to the now converted boolean `true` so this resolves to `true`.
15. The `==` operator compares values, even ones of different types, while taking type conversion into consideration. If two values of different types are being compared, the values are converted into numbers then compared according to number rules. Meanwhile, the `===` is a strict equality operator that compares values without type conversion. If the two values being compared are different types, it immediately returns false without attempting any conversion. This also applies to the keywords `null` and `undefined`, which are interpreted to be different types under strict equality comparison although they equal one another under non-strict comparison check.
16. `/part2-question16.js`
17. The returned result is a list consisting of each number in the `array` parameter being doubled. For this specific function call `modifyArray([1,2,3], doSomething)`, the returned list is `[ 2, 4, 6 ]`. The list `[1,2,3]` is passed into `modifyArray` along with the function `doSomething`. Inside of `modifyArray`, `doSomething` is called on each element of the list, and the returned result is added into `newArr` which is returned at the end of `modifyArray`. `doSomething` doubles each number passed into it and returns that result.
18. `/part2-question18.js`
19. `printNums`
    ```
    1
    4
    3
    2
    ```