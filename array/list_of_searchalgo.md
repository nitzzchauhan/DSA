Here is a table listing the **searching algorithms** used with arrays, including their descriptions, time complexities, and conditions for use:

| **Algorithm**       | **Description**                                                                                              | **Best Case Time Complexity** | **Worst Case Time Complexity** | **Array Requirement**                  |
|----------------------|------------------------------------------------------------------------------------------------------------|-------------------------------|--------------------------------|------------------------------------------|
| **Linear Search**    | Sequentially checks each element until the target element is found or the array ends.                      | \(O(1)\)                     | \(O(n)\)                      | Works on any array (unsorted/sorted).   |
| **Binary Search**    | Efficiently divides the array into halves to search for the target.                                        | \(O(1)\)                     | \(O(\log n)\)                 | Requires a sorted array.                |
| **Jump Search**      | Skips elements in fixed steps, then performs a linear search within the smaller block.                     | \(O(\sqrt{n})\)              | \(O(\sqrt{n})\)               | Requires a sorted array.                |
| **Interpolation Search** | Estimates the position of the target based on the distribution of values (works well for uniformly distributed data). | \(O(1)\)                     | \(O(n)\)                      | Requires a sorted array.                |
| **Exponential Search** | Searches by doubling the range until the target is within a range, then applies binary search.           | \(O(\log i)\)                | \(O(\log n)\)                 | Requires a sorted array.                |
| **Fibonacci Search** | Uses Fibonacci numbers to divide the search range and performs comparisons to find the target.             | \(O(\log n)\)                | \(O(\log n)\)                 | Requires a sorted array.                |
| **Ternary Search**   | Divides the array into three parts and recursively searches in the relevant section.                       | \(O(\log n)\)                | \(O(\log n)\)                 | Requires a sorted array.                |

---

### **Key Notes**:
1. **Unsorted Arrays**:
   - Linear Search is the only algorithm that works efficiently, as it does not rely on sorted data.
2. **Sorted Arrays**:
   - Binary Search is the most common and efficient choice.
   - Advanced algorithms like Jump Search, Interpolation Search, or Fibonacci Search are used for specific cases, such as uniform distributions or specific performance constraints.
3. **Space Complexity**:
   - All the above algorithms have \(O(1)\) space complexity except recursive versions of Binary or Ternary Search, which may have additional stack space usage.

If you'd like details or code examples for any specific algorithm, let me know!