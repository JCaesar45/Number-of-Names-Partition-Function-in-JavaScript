```markdown
# Number of Names (Partition Function) in JavaScript

This project implements a function to compute the number of partitions of a given integer `n`. The number of partitions corresponds to the number of ways to write `n` as a sum of positive integers, where order does not matter.

---

## Description

The problem is derived from a variation of Arthur C. Clarke's story "The Nine Billion Names of God." In this context, each integer `n` has a certain number of "names" (partitions), which is the count of all distinct ways to express `n` as a sum of positive integers.

For example:
- `1` has 1 name: `1`.
- `2` has 2 names: `1+1`, `2`.
- `3` has 3 names: `1+1+1`, `2+1`, `3`.
- `4` has 5 names: `1+1+1+1`, `2+1+1`, `2+2`, `3+1`, `4`.
- `5` has 7 names, and so on.

The number of names for `n` is mathematically known as the **partition function**, denoted as `P(n)`.

---

## Implementation

The core of this project uses **dynamic programming** with a recurrence relation based on **Euler's pentagonal number theorem** to efficiently compute `P(n)` for large `n`.

### How it works:
- Initializes an array `partitions` with `P(0) = 1`.
- Iteratively computes `P(i)` for `i` from `1` to `n`.
- Uses the pentagonal number theorem to sum over generalized pentagonal numbers with alternating signs.

---

## Usage

Call the `numberOfNames(n)` function with the desired integer:

```javascript
console.log(numberOfNames(5)); // Output: 7
console.log(numberOfNames(12)); // Output: 77
console.log(numberOfNames(18)); // Output: 385
console.log(numberOfNames(23)); // Output: 1255
console.log(numberOfNames(42)); // Output: 53174
console.log(numberOfNames(123)); // Output: 2552338241
``

---

## License

This implementation is provided for educational purposes. Feel free to adapt and expand upon it.

---

## Author

[Your Name or Alias]

---

## Acknowledgments

Based on classical number theory concepts and inspired by Arthur C. Clarke's story "The Nine Billion Names of God."
