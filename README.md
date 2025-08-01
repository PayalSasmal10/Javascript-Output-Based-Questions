# JavaScript output-based interview questions

## 🙌 Like this project?

If you found this helpful, support the project by clicking the ⭐ button at the top of the repo!
Your star motivates us to add more high-quality content 🌟✨

## Contribution Guidelines

If you want to contribute, improve, or suggest changes to this repo, then check out the
[Contributing Guide](https://github.com/PayalSasmal10/Javascript-Output-Based-Questions/blob/main/CONTRIBUTING.md)

##

1. What will be the output

```javascript
console.log(0 || 3);
console.log(1 || 2);
console.log(0 && 1);
console.log(1 && 2);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
3
1
0
2
```

🧠 **Explanation:**

- `0 || 3` → returns `3` because `0` is falsy, so it evaluates to the second operand (`3`).
- `1 || 2` → returns `1` because `1` is truthy, so it evaluates to the first operand.
- `0 && 1` → returns `0` because `0` is falsy, so `&&` returns the first falsy operand.
- `1 && 2` → returns `2` because both are truthy, so `&&` returns the last operand.
</details>

#

2. What will be the output

```javascript
let f = "2";
let a = 4;
console.log(+f + a + 1);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
7
```

🧠 **Explanation:**

- `let f = "2";` — `f` is a string `"2"`.
- `+f` — the unary plus converts the string `"2"` to the number `2`.
- `+f + a + 1` → `2 + 4 + 1` → `7`.
</details>

#

3. What will be the output

```javascript
const a = (1, 2, 3);
console.log(a);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
3
```

🧠 **Explanation:**

- The comma operator evaluates each of its operands (from left to right) and returns the value of the last operand.
- `(1, 2, 3)` evaluates to `3`.
- So, `a` is assigned the value `3`, and `console.log(a);` prints `3`.
</details>

#

4. What will be the output

```javascript
function multiple(x, y) {
  return x * y;
}
let multi = multiple.bind(this, 7);
console.log(multi(6));
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
42
```

🧠 **Explanation:**

**bind(this, 7) creates a new function where:**

- this is explicitly set (in this case to the current this)
- First argument x is pre-filled with 7
- You need to pass only the second argument y
- this inside multiple is not used, so its value doesn't matter for the output.
</details>

#

5. What will be the output

```javascript
let i = 0;
for (i = 0; i < 3; i++) {
  const log = () => {
    console.log(i);
  };
  setTimeout(log, 100);
}
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
3
3
3
```

🧠 **Explanation:**

- let i = 0; for (i = 0; i < 3; i++) {...} runs the loop 3 times with i = 0, 1, 2.

- Inside the loop, a new function log is created in each iteration, capturing the same i from outer scope.

- The function log is scheduled using setTimeout(..., 100), which executes after the loop has finished.

- By the time all three timeouts fire (after ~100ms), the value of i has already become 3.
  So each call to log() prints 3.

If you wanted it to print 0 1 2, you'd need to capture the value of i for each iteration using let inside the loop or IIFE:

```javascript
for (let i = 0; i < 3; i++) {
  const log = () => {
    console.log(i);
  };
  setTimeout(log, 100);
}
// Output: 0 1 2
```

</details>

#

6. What will be the output

```javascript
console.log({} == {});
console.log({} === {});
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
false
false
```

🧠 **Explanation:**

In JavaScript, objects are compared by reference, not by value.

- {} creates a new object each time.
  So, {} == {} → comparing two different object references → false.

- {} === {} → strict equality also compares reference still false.

- They're not the same object in memory, even though they have the same structure (i.e., empty).
</details>

#

7. What will be the output

```javascript
console.log(typeof isNaN);
console.log(isNaN === isNaN);

console.log(typeof NaN);
console.log(NaN === NaN);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
"function"
true
"number"
false
```

🧠 **Explanation:**

- `typeof isNaN` returns `"function"` because `isNaN` is a built-in function.
- `isNaN === isNaN` is `true` because both refer to the same function.
- `typeof NaN` returns `"number"` because NaN is a special numeric value.
- `NaN === NaN` is `false` because NaN is not equal to anything, even itself.
</details>

#

8. What will be the output

```javascript
let a = [1, 2, 3];
let b = a;
b.push(4);
console.log(a);
console.log(b);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
[1, 2, 3, 4]
[1, 2, 3, 4]
```

🧠 **Explanation:**

- Arrays are reference types. `b` points to the same array as `a`.
- Pushing to `b` also changes `a`.
</details>

#

9. What will be the output

```javascript
console.log(x);
var x = 10;
if (true) {
  console.log(x);
  let y = 5;
}
console.log(y);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
undefined
10
ReferenceError: y is not defined
```

🧠 **Explanation:**

- `var x` is hoisted, so `console.log(x)` before assignment is `undefined`.
- Inside the block, `x` is `10`.
- `let y` is block-scoped, so `console.log(y)` outside the block throws an error.
</details>

#

10. What will be the output

```javascript
console.log(typeof null);
console.log(null instanceof Object);
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
"object"
false
```

🧠 **Explanation:**

- `typeof null` returns `"object"` (quirk in JS).
- `null` is not an instance of `Object`.
</details>

#

11. What will be the output

```javascript
const obj = {
  name: "Heer",
  greet: function () {
    console.log(this.name);
    console.log(`My name is ${this.name}`);
  },
};

const greet = obj.greet;
greet();

obj.greet();
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
undefined
My name is undefined
Heer
My name is Heer
```

🧠 **Explanation:**

- When `greet` is called standalone, `this` is `undefined` (or global object in non-strict mode).
- When called as `obj.greet()`, `this` refers to `obj`.
</details>

#

12. What will be the output

```javascript
// Class based output
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hello, my name is ${this.name}`);
  }
}

const p = new Person("Heer");
p.greet();
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
Hello, my name is Heer
```

🧠 **Explanation:**

- The class constructor sets the name.
- `greet()` prints the name.
</details>

#

13. What will be the output

```html
<div id="parent">
  <button id="child">Child</button>
</div>
```

```javascript
const parentEle = document.getElementById("parent");
const childEle = document.getElementById("child");

parentEle.onclick = function () {
  console.log("Hello from parent");
};

childEle.onclick = function () {
  console.log("Hello from child");
};
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
Clicking the button logs "Hello from child".
Clicking elsewhere in the parent logs "Hello from parent".
```

🧠 **Explanation:**

- Each element has its own click handler.
- Clicking the child triggers only the child's handler.
</details>

#

14. What will be the output

```javascript
function multiple(x, y) {
  return x * y;
}

let multi = multiple.bind(this, 7);
console.log(multi(6));
```

<details>
  <summary>🔍 Click to View Answer</summary>

🧾 **Output:**

```
42
```

🧠 **Explanation:**

- The `bind()` method creates a new function with a fixed `this` value and initial arguments
- `multiple.bind(this, 7)` creates a new function where:
  - First parameter `x` is permanently set to `7`
  - Second parameter `y` will be provided when calling `multi()`
- When we call `multi(6)`:
  - `x` is `7` (bound value)
  - `y` is `6` (passed argument)
  - Returns `7 * 6 = 42`
  </details>

#
