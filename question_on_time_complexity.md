Here are some questions (with a mix of difficulty levels) on time complexity to help you understand and apply the concept:

---

### **Basic Questions**
1. What is the time complexity of accessing an element in an array by index?
2. Explain the difference between \( O(n) \) and \( O(n^2) \) in simple terms.
3. If an algorithm has a time complexity of \( O(\log n) \), what type of operation might it be performing?
4. Why do we ignore constants and lower-order terms when expressing time complexity?

---

### **Understanding Growth**
5. Arrange the following time complexities in order of their growth rate (from slowest to fastest):  
   \( O(1) \), \( O(n^2) \), \( O(n \log n) \), \( O(\log n) \), \( O(2^n) \).
6. If an algorithm has \( O(2n + 5) \) as its runtime, what is its simplified time complexity?
7. How does the runtime of \( O(n^3) \) compare to \( O(n^2) \) when \( n = 100 \)?

---

### **Analyzing Algorithms**
8. Consider a nested loop like this:
   ```python
   for i in range(n):
       for j in range(n):
           print(i, j)
   ```
   What is the time complexity of this code?
9. How does the time complexity change if the inner loop depends on the outer loop, like this:
   ```python
   for i in range(n):
       for j in range(i):
           print(i, j)
   ```

10. An algorithm divides the input size by 2 in each step until it reaches 1. What is its time complexity?

---

### **Real-Life Scenarios**
11. You’re designing a search algorithm for a phonebook:
    - Binary search is \( O(\log n) \).
    - Linear search is \( O(n) \).  
    Which one should you use if the phonebook is sorted? Why?

12. A sorting algorithm takes \( O(n \log n) \) in the worst case. If the input size doubles, how does the runtime change?

---

### **Tricky Questions**
13. An algorithm runs in \( O(n^2) \) for small inputs but switches to \( O(n) \) for larger inputs. How would you describe its overall time complexity?
14. Two algorithms A and B solve the same problem:
    - Algorithm A: \( O(n^2) \)
    - Algorithm B: \( O(n \log n) \)  
    Which algorithm is better for large inputs? Why?

15. If a recursive function splits the problem into two smaller problems of size \( n/2 \), and each split takes constant time, what is its time complexity?

---

### **Practical Applications**
16. Why is \( O(n \log n) \) considered efficient for sorting, while \( O(n^2) \) is not?
17. How does time complexity impact the scalability of algorithms in real-world applications like search engines or social networks?
