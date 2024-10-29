### Kahn's Algortithm

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