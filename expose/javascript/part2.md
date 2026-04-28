## Part 2

1. Prints "3". var is function-scoped so i leaks out of the for loop and is still accessible at line 12. The loop exits when i = 3.

2. Prints "150". var is function-scoped so discountedPrice leaks out of the for loop. The last value was 300 \* 0.5 = 150.

3. Prints "150". var is function-scoped so finalPrice leaks out of the for loop. The last value was Math.round(150 \* 100) / 100 = 150.

4. Returns [50, 100, 150]. Each price is multiplied by 0.5, so 100 -> 50, 200 -> 100, 300 -> 150.
5. Throws an error. let is block-scoped so i only exists inside the for loop.

6. Throws an error. let is block-scoped so discountedPrice only exists inside the for loop.

7. Prints "150". finalPrice is declared with let outside the for loop so it is accessible throughout the function. Last value is 150.

8. Returns [50, 100, 150]. discounted is declared with let outside the for loop.
9. Throws an error. let is block-scoped so i only exists inside the for loop.

10. Prints "3". length is declared with const outside the for loop. prices.length for [100, 200, 300] is 3.

11. Returns [50, 100, 150]. you can still modify array contents with push even with const declaration.

12. A. student.name
    B. student['Grad Year']
    C. student.greeting()
    D. student['Favorite Teacher'].name
    E. student.courseLoad[0]

13. A. '3' + 2 = '32'. '2+ with a string concatenates, so 2 is converted to '2' and joined with '3'.
    B. '3' - 2 = 1. - converts the string '3' to a number and subtracts.
    C. 3 + null = 3. null converts to 0 in numeric operations.
    D. '3' + null = '3null'. + with a string converts null to 'null' and concatenates.
    E. true + 3 = 4. true converts to 1 in numeric operations.
    F. false + null = 0. false converts to 0 and null converts to 0.
    G. '3' + undefined = '3undefined'. + with a string converts undefined to 'undefined' and concatenates.
    H. '3' - undefined = NaN. undefined cannot be converted to a number so the result is NaN.

14. A. '2' > 1 = true. converts '2' to a number and compares. 2 > 1 = true.
    B. '2' < '12' = false. When comparing two strings it compares alphabetically. '2' comes after '1' so '2' is greater.
    C. 2 == '2' = true. == is loose equality so it converts '2' to a number and compares 2 == 2 = true.
    D. 2 === '2' = false. === is strict equality so it checks both value and type. 2 is a number and '2' is a string so they are not equal.
    E. true == 2 = false. true converts to 1 and 1 == 2 is false.
    F. true === Boolean(2) = true. Boolean(2) converts 2 to true since any non-zero number is true. true === true is true.

15. == is the loose equality operator and === is the strict equality operator. == converts both sides to the same type before comparing, while === checks both value and type without any conversion. So, == can compare different data types but === requires both sides to be the same type and value.

16. in part2-question16.js

17. modifyArray([1,2,3], doSomething) returns [2, 4, 6]. The modifyArray function iterates through each element and applies the doSomething callback which multiplies each number by 2. So 1->2, 2->4, 3->6.
18. in part2-question18.js
19. The output is:  
    1
    4
    3
    2
    console.log(1) and console.log(4) run immediately. The two setTimeouts get pushed back even if the delay is 0ms. So 3 runs after console.log(1) and console.log(4) run and 2 runs last (1000ms delay).
