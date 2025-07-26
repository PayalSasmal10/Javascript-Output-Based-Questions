# JavaScript output-based interview questions

## Contributing Guidelines

👉 Please ensure that your contributions adhere to the coding style and guidelines of this project.  
👉 Include clear and concise commit messages for all your commits.  
👉 Provide a detailed description of your changes in the pull request.  
👉 Be respectful and considerate towards other contributors.

##

1. What will be the output

```javascript
console.log(0 || 3);
console.log(1 || 2);
console.log(0 && 1);
console.log(1 && 2);
```

<details>
  <summary>View Answer</summary>

**Output:**

```
3
1
0
2
```

**Explanation:**

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
  <summary>View Answer</summary>

**Output:**

```
7
```

**Explanation:**

- `let f = "2";` — `f` is a string `"2"`.
- `+f` — the unary plus converts the string `"2"` to the number `2`.
- `+f + a + 1` → `2 + 4 + 1` → `7`.
</details>
