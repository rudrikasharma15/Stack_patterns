
# 🌟 Complete Stack-Based DSA Patterns  


---

## **1. Monotonic Stack (Increasing/Decreasing)**  
Used for problems like **Next Greater/Smaller Element, Stock Span, Histogram Area, Subarray Minimums**.

**Key Idea:**  
- Maintain a stack of elements (or indices) in **increasing or decreasing order**.  
- Pop elements that break the monotonic order.  
- Decide traversal direction (left→right or right→left) based on what we need.

**Template:**  
```java
Stack<Integer> st = new Stack<>();
for (int i = 0; i < arr.length; i++) {
    while (!st.isEmpty() && arr[st.peek()] >= arr[i]) st.pop();  // for increasing
    // process based on stack state
    st.push(i);
}
````

**Examples:**

* Next Greater Element I/II
* Daily Temperatures (with indices)
* Largest Rectangle in Histogram
* Sum of Subarray Minimums (prefix + monotonic stack)

---

## **2. Balancing Symbols (Parentheses & Brackets)**

Used to **check or fix valid parentheses/brackets**.

**Key Idea:**

* Push opening brackets.
* Pop and check when a closing bracket is found.
* Stack must be empty at the end.

**Template:**

```java
Stack<Character> st = new Stack<>();
for(char c: s.toCharArray()){
    if(c=='(' || c=='[' || c=='{') st.push(c);
    else if(st.isEmpty() || !matches(st.pop(), c)) return false;
}
return st.isEmpty();
```

**Examples:**

* Valid Parentheses
* Minimum Add to Make Valid
* Remove Invalid Parentheses
* Longest Valid Parentheses (with prefix + stack)

---

## **3. Min Stack / Max Stack (Tracking Min/Max in O(1))**

Used in **design problems** where we track minimum or maximum efficiently.

**Key Idea:**

* Use an **auxiliary stack** to store min/max at each step.

**Template (Min Stack):**

```java
Stack<Integer> st = new Stack<>();
Stack<Integer> minSt = new Stack<>();
public void push(int x){
    st.push(x);
    if(minSt.isEmpty() || x <= minSt.peek()) minSt.push(x);
}
public void pop(){
    if(st.pop().equals(minSt.peek())) minSt.pop();
}
public int getMin(){ return minSt.peek(); }
```

**Examples:**

* Design Min Stack
* Design Max Stack
* Stack with Increment

---

## **4. Greedy Stack Simulation (Push/Pop Logic)**

Used for **dynamic simulations** like collisions, removing digits, or building strings.

**Key Idea:**

* Push until a conflict, then pop based on conditions.
* Often paired with **greedy** decisions.

**Template:**

```java
Stack<Integer> st = new Stack<>();
for(int x : arr){
    while(!st.isEmpty() && conflict(st.peek(), x)){
        if(shouldPop(st.peek(), x)) st.pop();
        else break;
    }
    st.push(x);
}
```

**Examples:**

* Asteroid Collision
* Remove K Digits
* Build Lexicographically Smallest String

---

## **5. Infix/Prefix/Postfix Evaluation (Expression Parsing)**

Used for **expression problems and calculators**.

**Key Idea:**

* Use a stack for operands and operators.
* For **postfix**: push operands, apply operator when seen.
* For **infix**: convert to postfix or use two stacks (operands + operators).

**Template (Postfix):**

```java
Stack<Integer> st = new Stack<>();
for(String token : tokens){
    if(isNumber(token)) st.push(Integer.parseInt(token));
    else {
        int b = st.pop(), a = st.pop();
        st.push(applyOp(a, b, token));
    }
}
return st.pop();
```

**Examples:**

* Evaluate Reverse Polish Notation
* Basic Calculator I/II/III
* Decode String (nested stacks)

---

## **6. Backtracking Using Stack (DFS-like)**

Used when **exploring paths, combinations, or undoing decisions**.

**Key Idea:**

* Push current path/state.
* Pop back when reaching dead ends.
* Similar to recursion but explicit.

**Examples:**

* Path Sum (DFS iterative)
* Combination Sum (explicit stack)
* Generate Parentheses (stack-based)

---

## **7. Stack + Prefix Sum Hybrid**

Used for problems combining **range checks** and **parentheses matching**.

**Key Idea:**

* Track prefix sum (or balance) along with stack for positions.

**Example:**

* Longest Valid Parentheses
* Minimum Remove to Make Valid Parentheses

---

## **8. Design Stack-Based Data Structures**

Used for **custom behavior**.

**Examples:**

* Max Frequency Stack (Stack + HashMap)
* Stack of Plates (split stacks)
* Implement Deque/Queue with Two Stacks
* Circular Buffer with Stack

---

## **9. Custom Stack Implementation (From Scratch)**

For interviews where you must implement a stack yourself.
Use **array or LinkedList**, support O(1) operations.

**Examples:**

* Implement Stack using Queues
* Implement Queue using Stacks

---

## **Practice Ladder (Cover All Patterns)**

1. Valid Parentheses
2. Next Greater Element I/II
3. Daily Temperatures
4. Largest Rectangle in Histogram
5. Asteroid Collision
6. Remove K Digits
7. Min Stack & Max Stack
8. Evaluate Reverse Polish Notation
9. Decode String
10. Basic Calculator II & III
11. Longest Valid Parentheses
12. Max Frequency Stack
13. Implement Queue using Stacks


