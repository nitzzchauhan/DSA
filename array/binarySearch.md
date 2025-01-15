### **Binary Search Explained**

**Binary Search** is an efficient algorithm used to search for an element in a **sorted** array or list. Unlike **Linear Search**, which checks each element one by one, **Binary Search** divides the search space in half with each comparison, making it much faster for large datasets.

---

### **How Binary Search Works**
Binary Search works on the principle of **divide and conquer**. It repeatedly divides the search interval in half, checking if the element is in the left half or the right half. This is done as follows:

1. **Start with the entire array**: Set the left pointer to the start of the array and the right pointer to the end.
2. **Find the middle element**: Calculate the middle index using the formula:
   \[
   \text{middle} = \frac{\text{left} + \text{right}}{2}
   \]
3. **Compare**:
   - If the target element is equal to the middle element, return the index of the middle element.
   - If the target element is **smaller** than the middle element, narrow the search to the **left half** by adjusting the right pointer: 
     \[
     \text{right} = \text{middle} - 1
     \]
   - If the target element is **larger** than the middle element, narrow the search to the **right half** by adjusting the left pointer:
     \[
     \text{left} = \text{middle} + 1
     \]
4. **Repeat** the process on the new left or right half until the left pointer exceeds the right pointer (meaning the element is not in the array).

---

### **Binary Search Algorithm**

Here’s the **pseudocode** for Binary Search:

```
BinarySearch(arr, target):
    left = 0
    right = len(arr) - 1

    while left <= right:
        middle = (left + right) // 2   // Find the middle index

        if arr[middle] == target:
            return middle                 // Element found at middle index
        elif arr[middle] < target:
            left = middle + 1             // Narrow search to the right half
        else:
            right = middle - 1            // Narrow search to the left half

    return -1  // Element not found
```

### **Example**

Let’s take an example:

**Array**: `[1, 3, 5, 7, 9, 11, 13, 15]`

**Target**: `7`

1. Start with **left = 0** and **right = 7** (array length is 8).
2. The middle element is at index `(0 + 7) // 2 = 3`. The value at index 3 is `7`, which is the target.
3. Return the index `3`.

So, **Binary Search** would return **index 3**.

---

### **Time and Space Complexity**

1. **Time Complexity**: 
   - **Best Case**: \(O(1)\) – when the target is found at the middle element.
   - **Worst Case**: \(O(\log n)\) – each comparison cuts the search space in half.
   - **Average Case**: \(O(\log n)\)

2. **Space Complexity**:
   - **Iterative Approach**: \(O(1)\) – constant space.
   - **Recursive Approach**: \(O(\log n)\) – due to the function call stack in recursion.

---

### **Binary Search Advantages**
- **Efficiency**: Since the search space is halved at each step, it is much faster than linear search, especially for large datasets.
- **Time Complexity**: \(O(\log n)\) compared to \(O(n)\) for Linear Search.

---

### **Binary Search Conditions**
- **Sorted Array**: Binary Search requires the array to be sorted. If the array is not sorted, you must sort it first (which can take \(O(n \log n)\) time) before performing Binary Search.
- **Works for**: Sorted arrays, lists, and certain data structures (like balanced trees).

---

### **Example Code in Python**

Here’s an example of **Binary Search** implemented in Python:

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        middle = (left + right) // 2
        
        if arr[middle] == target:
            return middle  # Target found
        elif arr[middle] < target:
            left = middle + 1  # Search right half
        else:
            right = middle - 1  # Search left half

    return -1  # Target not found

# Example usage
arr = [1, 3, 5, 7, 9, 11, 13, 15]
target = 7
result = binary_search(arr, target)

if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")
```

**Output**:
```
Element found at index 3
```

---

### **Conclusion**
Binary Search is one of the most efficient searching algorithms for **sorted arrays**, providing logarithmic time complexity. It’s widely used in applications where large datasets need to be searched quickly, and is the foundation for many more complex algorithms.






Here are some **binary search interview questions** commonly asked by companies, along with their explanations and expected approaches to solving them:

---

### **1. Basic Binary Search Problem**
#### **Question**:
Given a **sorted array**, write a function to find the index of a target element using **binary search**. If the target is not found, return `-1`.

#### **Explanation**:
This is the most straightforward binary search question where you need to implement the basic binary search algorithm.

#### **Example**:
```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
```

---

### **2. Find First Occurrence of a Target**
#### **Question**:
Given a **sorted array** that may have duplicate elements, find the **first occurrence** of the target value using binary search.

#### **Explanation**:
This problem modifies the typical binary search to ensure that you always return the first occurrence of the target.

#### **Approach**:
1. When you find the target, check if it's the first element or if the element before it is different.
2. Keep searching in the left half even if you find the target.

#### **Example**:
```python
def find_first_occurrence(arr, target):
    left, right = 0, len(arr) - 1
    result = -1
    
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            result = mid
            right = mid - 1  # Search in left half
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return result
```

---

### **3. Find Last Occurrence of a Target**
#### **Question**:
Given a **sorted array** that may have duplicates, find the **last occurrence** of the target value using binary search.

#### **Explanation**:
This is similar to the previous question, except you now need to search for the last occurrence of the element.

#### **Approach**:
1. When you find the target, check if it's the last element or if the element after it is different.
2. Keep searching in the right half even if you find the target.

#### **Example**:
```python
def find_last_occurrence(arr, target):
    left, right = 0, len(arr) - 1
    result = -1
    
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            result = mid
            left = mid + 1  # Search in right half
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return result
```

---

### **4. Find the Element Closest to the Target**
#### **Question**:
Given a **sorted array**, find the element that is **closest** to a given target. If there are two elements equally close, return the smaller one.

#### **Explanation**:
This question requires you to perform binary search and then adjust the left and right pointers to find the closest element.

#### **Approach**:
1. Perform the usual binary search.
2. After the search, check which of the two surrounding elements (left and right) is closer to the target.

#### **Example**:
```python
def closest_element(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            return arr[mid]
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    # After binary search, left and right will point to two potential candidates
    if left < len(arr) and abs(arr[left] - target) < abs(arr[right] - target):
        return arr[left]
    else:
        return arr[right]
```

---

### **5. Find Peak Element**
#### **Question**:
A peak element is an element that is greater than or equal to its neighbors. Given an **array** where every element is greater than its neighbors (except possibly at the ends), find a peak element using binary search.

#### **Explanation**:
A peak element can be found in \(O(\log n)\) time using binary search. If the middle element is greater than its neighbors, it’s a peak. Otherwise, the search continues in the half where a peak must exist.

#### **Approach**:
1. Compare the middle element with its neighbors.
2. If the middle element is greater than both neighbors, return it as a peak.
3. Otherwise, move the search to the side where the greater neighbor exists.

#### **Example**:
```python
def find_peak(arr):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        if (mid == 0 or arr[mid - 1] <= arr[mid]) and (mid == len(arr) - 1 or arr[mid + 1] <= arr[mid]):
            return arr[mid]  # Peak found
        elif mid > 0 and arr[mid - 1] > arr[mid]:
            right = mid - 1  # Search in left half
        else:
            left = mid + 1  # Search in right half
```

---

### **6. Search in a Rotated Sorted Array**
#### **Question**:
Given a **rotated sorted array**, write a function to search for a target element using binary search. The array was originally sorted, but then rotated at an unknown pivot.

#### **Explanation**:
In a rotated sorted array, the array is first sorted and then rotated. You need to modify binary search to handle the rotation.

#### **Approach**:
1. Find the middle element.
2. Determine which side of the array is sorted.
3. If the target is in the sorted side, narrow the search to that half.
4. Otherwise, search the unsorted half.

#### **Example**:
```python
def search_rotated(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            return mid
        
        # Check if the left half is sorted
        if arr[left] <= arr[mid]:
            if arr[left] <= target < arr[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            # Right half is sorted
            if arr[mid] < target <= arr[right]:
                left = mid + 1
            else:
                right = mid - 1
    
    return -1
```

---

### **7. Find Minimum in Rotated Sorted Array**
#### **Question**:
Given a **rotated sorted array** (not necessarily containing duplicates), find the minimum element using binary search.

#### **Explanation**:
In a rotated sorted array, the minimum element is the point where the array changes from a larger value to a smaller one.

#### **Approach**:
1. Find the middle element.
2. If the middle element is greater than the right element, the minimum must be in the right half.
3. Otherwise, the minimum is in the left half.

#### **Example**:
```python
def find_min_in_rotated(arr):
    left, right = 0, len(arr) - 1
    
    while left < right:
        mid = (left + right) // 2
        
        if arr[mid] > arr[right]:
            left = mid + 1  # Search right half
        else:
            right = mid  # Search left half
    
    return arr[left]
```

---

### **8. Counting Occurrences of an Element**
#### **Question**:
Given a **sorted array** with possible duplicate elements, count the number of occurrences of a target element using binary search.

#### **Explanation**:
Use binary search to find the first and last occurrences of the target, then subtract their indices to get the count.

#### **Example**:
```python
def count_occurrences(arr, target):
    def find_first(arr, target):
        left, right = 0, len(arr) - 1
        result = -1
        while left <= right:
            mid = (left + right) // 2
            if arr[mid] == target:
                result = mid
                right = mid - 1
            elif arr[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return result

    def find_last(arr, target):
        left, right = 0, len(arr) - 1
        result = -1
        while left <= right:
            mid = (left + right) // 2
            if arr[mid] == target:
                result = mid
                left = mid + 1
            elif arr[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return result

    first = find_first(arr, target)
    if first == -1:
        return 0  # Target not found
    last = find_last(arr, target)
    return last - first + 1
```

---

These are common variations of binary search questions asked in interviews. The key to solving these problems efficiently is modifying the basic binary search algorithm according to the requirements. Understanding how to adjust the search space based on the problem is crucial for successfully solving these types of questions.