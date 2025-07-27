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
