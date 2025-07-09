# 🌟 Stack-Based DSA Patterns

**Author:** Rudrika Sharma

---

## 📊 STACK PATTERNS (with Examples)

### 1. 🫠 Monotonic Stack (Increasing/Decreasing)

Use when solving problems like Next Greater/Smaller Element, Histogram area, or spans.

🧠 Technique:

* Traverse from right to left (or left to right based on requirement)
* Maintain elements in **monotonic increasing or decreasing order**
* Pop elements that break the stack condition

🔹 Examples:

* Next Greater/Smaller Element
* Stock Span
* Largest Rectangle in Histogram

---

### 2. 🧵 Balancing Symbols (Parentheses, Brackets)

Used when checking for valid brackets, balancing characters.

🧠 Technique:

* Push opening brackets
* Pop and check on closing bracket
* Stack should be empty at the end

🔹 Examples:

* Valid Parentheses
* Minimum Add to Make Valid
* Remove Invalid Parentheses

---

### 3. ⚖️ Min Stack / Max Stack

Use to track the minimum/maximum element in O(1) alongside the original stack.

🧠 Technique:

* Use an auxiliary stack to store the minimum value at each state

🔹 Examples:

* Design Min Stack
* Design Stack with Increment

---

### 4. 🫰 Stack Simulation (Greedy Stack)

Use when simulating dynamic changes (collisions, popping, removing digits).

🧠 Technique:

* Push or pop based on rules/conditions
* Often combines with greedy logic

🔹 Examples:

* Asteroid Collision
* Remove K Digits
* Build Lexicographically Smallest String

---

### 5. 🔄 Infix/Prefix/Postfix Evaluation

Use when parsing or evaluating expressions using operator precedence.

🧠 Technique:

* Use a stack to process operands and operators
* For postfix: push operands, apply operators

🔹 Examples:

* Evaluate Reverse Polish Notation
* Basic Calculator I/II/III

---

### 6. 🚪 Backtracking Using Stack

Use in DFS traversal, exploring paths, or undoing decisions.

🧠 Technique:

* Push path/state on stack
* Pop back on dead ends or to try next possibility

🔹 Examples:

* Path Sum using DFS
* Combination Problems with Explicit Stack

---

### 7. 🏛️ Design Stack-Based Data Structures

Use for custom behavior like push, pop, getMin, increment, etc.

🧠 Technique:

* Use 2 stacks or additional arrays

🔹 Examples:

* Stack with Frequency Tracking
* Stack of Plates
* Max Stack

---

### 8. 🔧 Custom Stack Implementation

When you're asked to build a stack from scratch with extra features.

🧠 Technique:

* Array or LinkedList implementation
* Support O(1) operations

🔹 Examples:

* Implement Stack using Queue
* Implement Queue using Stack

---

## 📆 Practice Ladder (Apply These Patterns)

* Valid Parentheses
* Next Greater Element
* Daily Temperatures
* Largest Rectangle in Histogram
* Asteroid Collision
* Remove K Digits
* Min Stack
* Max Stack
* Evaluate Reverse Polish Notation
* Decode String
* Basic Calculator
* Stock Span Problem

---

