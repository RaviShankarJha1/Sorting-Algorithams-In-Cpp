# Aim  
To study and implement Sorting Algorithms in C++  

# Software Required  
Visual Studio  

# Theory  
A Sorting Algorithm rearranges a given array or list of elements in a specific order, such as increasing or decreasing. Sorting can be categorized by stability (maintaining order of equal elements) or optimized for specific types of input.  

### **Selection Sort**  
- Comparison-based sorting algorithm.  
- Repeatedly selects the smallest (or largest) element from the unsorted portion and swaps it with the first unsorted element.  
- Time Complexity: O(n²)  

### **Bubble Sort**  
- Simplest sorting algorithm.  
- Repeatedly swaps adjacent elements if they are in the wrong order.  
- After each pass, the largest unsorted element moves to its correct position.  
- Time Complexity: O(n²)  

### **QuickSort**  
- Divide and Conquer algorithm.  
- Steps:  
  1. Choose a pivot element.  
  2. Partition array around pivot (elements smaller on left, larger on right).  
  3. Recursively sort left and right sub-arrays.  
- Time Complexity: Average O(n log n), Worst O(n²)  

# Implementation  
Sorting is demonstrated using the following algorithms:  
- Selection Sort  
- Bubble Sort  
- QuickSort  

# Algorithms  

### Sorting and Searching in an Array  

1. Start  
2. Define a class `BubbleSort` with function `sort(std::vector<int>& arr)`:  
   - For `i = 0` to `n-2`, and `j = 0` to `n-i-2`:  
     - If `arr[j] > arr[j+1]`, swap them.  
3. Define a class `SearchArr` with function `binarysearch(const std::vector<int>& arr, int target)`:  
   - Initialize `low = 0`, `high = n-1`.  
   - While `low <= high`:  
     - Compute `mid = low + (high - low)/2`.  
     - If `arr[mid] == target`, return `mid`.  
     - Else adjust `low` or `high` accordingly.  
   - Return `-1` if element not found.  
4. In `main()`:  
   - Create objects `sorter` and `s`.  
   - Initialize array `arr = {-1, 0, 3, 5, 9, 12}`.  
   - Call `sorter.sort(arr)` and print sorted array.  
   - Set `target = 9` and call `s.binarysearch(arr, target)`.  
   - Print index if found, else *"Element not found"*.  
5. End  

### Quick Sort  

1. Start  
2. `partition(arr, low, high)`:  
   - Choose last element as pivot.  
   - Initialize `i = low - 1`.  
   - For `j = low` to `high - 1`:  
     - If `arr[j] < pivot`, increment `i` and swap `arr[i]` and `arr[j]`.  
   - Swap `arr[i+1]` and `arr[high]`.  
   - Return `i+1` (partition index).  
3. `quickSort(arr, low, high)`:  
   - If `low < high`:  
     - Call `partition` to get pivot index `pi`.  
     - Recursively call `quickSort(arr, low, pi - 1)` and `quickSort(arr, pi + 1, high)`.  
4. In `main()`:  
   - Initialize array `arr = {10, 7, 8, 9, 1, 5}`.  
   - Call `quickSort(arr, 0, n-1)`.  
   - Print sorted array.  
5. End  

### Selection Sort  

1. Start  
2. Take an unsorted array of size `n`.  
3. For `i = 0` to `n-2`:  
   - Assume `arr[i]` is minimum (`min_idx = i`).  
   - For `j = i+1` to `n-1`, if `arr[j] < arr[min_idx]`, update `min_idx = j`.  
   - Swap `arr[i]` and `arr[min_idx]`.  
4. Continue until array is sorted.  
5. Print sorted array.  
6. End  

# Conclusion  
The above programs demonstrate various sorting techniques—**Selection Sort**, **Bubble Sort**, and **QuickSort**—in C++, along with integration of sorting and binary search for efficient element retrieval.
