# article
Understanding let and const in JavaScript
JavaScript provides multiple ways to declare variables, with let and const being the most commonly used in modern development. These were introduced in ES6 to address the limitations of var. Understanding their differences and use cases is essential for writing efficient and bug-free code.
let - Block Scoped Variable Declaration
Features of let
1.	Block Scope: Variables declared with let are limited to the block in which they are defined.
2.	Reassignable: You can change the value of a let variable after its declaration.
3.	Does Not Hoist Like var: While let is hoisted, it is not initialized, leading to a ReferenceError if accessed before declaration.
Example:
function exampleLet() {
    let x = 10;
    if (true) {
        let x = 20; // Different variable due to block scope
        console.log(x); // Output: 20
    }
    console.log(x); // Output: 10
}
exampleLet();
const - Immutable Variable Declaration
Features of const
1.	Block Scope: Similar to let, const is limited to the block where it is defined.
2.	Immutable Reference: Once a value is assigned to a const variable, it cannot be reassigned.
3.	Must Be Initialized: Unlike let, const requires an initial value at the time of declaration.
Example:
function exampleConst() {
    const PI = 3.14;
    console.log(PI); // Output: 3.14
    
    // Attempting to reassign will throw an error
    // PI = 3.14159; // TypeError: Assignment to constant variable
}
exampleConst();
