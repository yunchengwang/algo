### Topological Sort

Kahn's Algortithm

```python
from collections import defaultdict, deque

def kahns_topological_sort(vertices, edges):
    # Step 1: Create the adjacency list representation of the graph
    graph = defaultdict(list)
    in_degree = {v: 0 for v in vertices}  # Initialize in-degree of all vertices to 0

    # Step 2: Build the graph and compute in-degrees of each vertex
    for u, v in edges:
        graph[u].append(v)
        in_degree[v] += 1  # Increment the in-degree of the destination vertex

    # Step 3: Initialize the queue with all vertices that have in-degree of 0
    queue = deque([v for v in vertices if in_degree[v] == 0])
    topological_order = []

    # Step 4: Process the queue
    while queue:
        v = queue.popleft()
        topological_order.append(v)  # Add current vertex to the topological order
        
        # For each neighbor, reduce its in-degree by 1
        for neighbor in graph[v]:
            in_degree[neighbor] -= 1
            if in_degree[neighbor] == 0:  # If in-degree becomes 0, enqueue it
                queue.append(neighbor)

    # Step 5: Check if all vertices are in topological order
    if len(topological_order) == len(vertices):
        return topological_order
    else:
        return []  # Return an empty list if the graph has a cycle (topological sort not possible)
```

### Merge Sort

```python
def merge_sort(arr):
    # Base case: A list of length 0 or 1 is already sorted
    if len(arr) <= 1:
        return arr

    # Step 1: Divide the array into two halves
    mid = len(arr) // 2
    left_half = arr[:mid]
    right_half = arr[mid:]

    # Step 2: Recursively sort each half
    left_sorted = merge_sort(left_half)
    right_sorted = merge_sort(right_half)

    # Step 3: Merge the two sorted halves
    return merge(left_sorted, right_sorted)

# Helper function to merge two sorted arrays
def merge(left, right):
    sorted_array = []
    i = j = 0
    
    # Compare elements from both halves and merge them in sorted order
    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            sorted_array.append(left[i])
            i += 1
        else:
            sorted_array.append(right[j])
            j += 1
    
    # If there are remaining elements in left or right, add them to the result
    sorted_array.extend(left[i:])
    sorted_array.extend(right[j:])
    
    return sorted_array
```