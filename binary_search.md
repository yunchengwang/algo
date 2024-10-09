### 1) Binary Search to Find Value in the List

```python
def binary_search(arr, target):
    left = 0
    right = len(arr) - 1

    while left <= right:
        mid = left + (right - left) // 2

        if arr[mid] == target:
            return mid  # Target found at index mid
        elif arr[mid] < target:
            left = mid + 1  # Search right half
        else:
            right = mid - 1  # Search left half

    return -1  # Target not found
```

---

### 2) `bisect_left`

```python
def bisect_left(arr, x):
    left = 0
    right = len(arr)

    while left < right:
        mid = left + (right - left) // 2

        if arr[mid] < x:
            left = mid + 1
        else:
            right = mid

    return left  # Insertion point
```

---

### 3) `bisect_right`

```python
def bisect_right(arr, x):
    left = 0
    right = len(arr)

    while left < right:
        mid = left + (right - left) // 2

        if arr[mid] <= x:
            left = mid + 1
        else:
            right = mid

    return left  # Insertion point
```

---

### 4) Binary Search for Minimum Valid Value

```python
def find_minimum_valid(left, right, is_valid):
    while left < right:
        mid = left + (right - left) // 2

        if is_valid(mid):
            right = mid
        else:
            left = mid + 1

    if is_valid(left):
        return left
    else:
        return -1  # No valid value found
```

---

### 5) Binary Search for Maximum Valid Value

```python
def find_maximum_valid(left, right, is_valid):
    while left < right:
        mid = left + (right - left + 1) // 2

        if is_valid(mid):
            left = mid
        else:
            right = mid - 1

    if is_valid(left):
        return left
    else:
        return -1  # No valid value found
```