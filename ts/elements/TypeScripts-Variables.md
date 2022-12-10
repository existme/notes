_Written by: Reza Shams Amiri_
# 01 - Variable Declaration (See also [ts-docs][TDVD])

1. Don't use `var` instead use `let` (scoping reasons see [ref][TDVD])
2. Use `const` if the variable is not going to be changed


## Array destructuring
1. Destructuring assignment:
    ``` js
    let input = [1, 2];
    let [first, second] = input;
    console.log(first); // outputs 1
    console.log(second); // outputs 2
    ```
1. Swapping:
   ``` js
   // swap variables
   [first, second] = [second, first];
   ```
2. Destructing function parameters:   
    ``` js
    function f([first, second]: [number, number]) {
      console.log(first);
      console.log(second);
    }
    f([1, 2]);
    ```

* * *
Creation date: _2022-12-10_

[TDVD]: https://www.typescriptlang.org/docs/handbook/variable-declarations.html