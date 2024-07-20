![DAY 1](https://github.com/user-attachments/assets/e94a9511-625c-481c-bbb7-e7d36632c34d)

# 7 Days Discipline: Day 1

Welcome to Day 1 of the '7 Days Discipline' series! Aaj hum cover karenge essential interview questions JavaScript aur Aptitude me. Pehle basic questions se shuru karenge aur dheere dheere advanced topics tak jayenge.

## JavaScript Interview Questions


### 1. JavaScript kya hai?
JavaScript ek lightweight, interpreted ya just-in-time compiled programming language hai with first-class functions. Ye web pages ke liye sabse zyada jaana jaata hai, but non-browser environments me bhi use hoti hai.

### 2. JavaScript me different data types kya hai?
JavaScript me alag alag data types hote hai values ko hold karne ke liye. Do types ke data types hai JavaScript me:
- Primitive data types: String, Number, Boolean, Null, Undefined, Symbol.
- Non-primitive data type: Object.

```javascript
Primitive Examples
let name = "John"; // String
let age = 30;      // Number
let isActive = true; // Boolean
let user = null;  // Null
let address;      // Undefined
```
```javascript
Non-primitive Examples
let party = {
    Budget: "Rs 5000",
    Boys: 5
};

let Contri = {
      Ayush: 2000,
      Shubham: 100,
      Manav: 1400,
      Dubey: 1000,
      Aniket: 500
};
```

### 3. `var` and `let`, `const` me kya difference hai?

| Feature             | `var`                            | `let`                          | `const`                        |
|---------------------|----------------------------------|-------------------------------|-------------------------------|
| Scope               | Function-scoped                  | Block-scoped                  | Block-scoped                  |
| Redeclaration       | Allowed                          | Not allowed                   | Not allowed                   |
| Reassignment        | Allowed                          | Allowed                       | Not allowed                   |
| Hoisting            | Yes (initialized with `undefined`) | Yes (but not initialized)      | Yes (but not initialized)      |
| Initial Value       | Optional                         | Optional                      | Required                      |

## Examples

### `var` Example

#### var function-scoped hota hai aur redeclare aur update kiya ja sakta hai.

```javascript
function varExample() {
    var x = 10;
    if (true) {
        var x = 20; // redeclare and update within same function scope
        console.log(x); // 20
    }
    console.log(x); // 20
}
varExample();
```

### `let` Example
#### let block-scoped hota hai aur update kiya ja sakta hai but redeclare nahi.

```javascript
function letExample() {
    let y = 10;
    if (true) {
        let y = 20; // block-scoped, so this is a new y within this block
        console.log(y); // 20
    }
    console.log(y); // 10
    
    y = 30; // update allowed
    console.log(y); // 30

    // let y = 40; // redeclaration not allowed, will cause error
    // SyntaxError: Identifier 'y' has already been declared
}
letExample();
```

### `const` Example
#### const block-scoped hota hai aur update ya redeclare nahi kiya ja sakta.

```javascript
function constExample() {
    const z = 10;
    if (true) {
        const z = 20; // block-scoped, so this is a new z within this block
        console.log(z); // 20
    }
    console.log(z); // 10

    // z = 30; // update not allowed, will cause error
    // TypeError: Assignment to constant variable.

    // const z = 40; // redeclaration not allowed, will cause error
    // SyntaxError: Identifier 'z' has already been declared
}
constExample();

```
