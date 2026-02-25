
---

## ⚙️ Constraints
- 1 ≤ nums.length ≤ 10^4  
- -10^4 ≤ nums[i] ≤ 10^4  
- `nums` is strictly increasing  

---

## 🚀 Approaches

### 1. Recursive Divide & Conquer
- **Idea:** Pick the middle element of the array as the root.  
- **Process:**  
  - Recursively build the left subtree from the left half.  
  - Recursively build the right subtree from the right half.  
- **Why it works:** Choosing the middle ensures the tree remains balanced.  
- **Complexity:**  
  - Time: O(n)  
  - Space: O(log n) recursion stack  

---

### 2. Iterative Queue-Based Approach
- **Idea:** Avoid recursion by simulating the process with a queue.  
- **Process:**  
  - Start with the middle element as root.  
  - Use a queue to store nodes along with their subarray ranges.  
  - Iteratively assign left and right children until all nodes are built.  
- **Why it works:** It builds the tree level by level, ensuring balance.  
- **Complexity:**  
  - Time: O(n)  
  - Space: O(n) in worst case due to queue storage  

---

### 3. Randomized Middle Selection
- **Idea:** For even-length arrays, randomly pick between the two middle indices.  
- **Process:**  
  - Random choice ensures multiple valid BSTs can be generated.  
  - Recursively build left and right subtrees as usual.  
- **Why it works:** Still maintains balance, but produces varied tree structures.  
- **Complexity:**  
  - Time: O(n)  
  - Space: O(log n) recursion stack  

---

## 📊 Comparison

| Approach                  | Pros                                | Cons                                |
|---------------------------|-------------------------------------|-------------------------------------|
| Recursive Divide & Conquer| Clean, simple, most common solution | May hit recursion depth limits       |
| Iterative Queue-Based     | Avoids recursion depth issues       | More verbose, harder to read        |
| Randomized Middle         | Produces varied valid BSTs          | Less predictable, adds randomness   |

---
