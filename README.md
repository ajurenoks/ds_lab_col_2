# Heap: Kth Smallest Element in an Array

You are given a list of numbers called `nums` and a number `k`.

Your task is to write a function `find_kth_smallest(nums, k)` to find the kth smallest number in the list.

The list can contain duplicate numbers and `k` is guaranteed to be within the range of the length of the list.

### Parameters
- `nums`: A list of integers.
- `k`: An integer.

### Return
This function should return the kth smallest number in `nums`.

### Example
```python
nums = [3, 2, 1, 5, 6, 4]
k = 2
print(find_kth_smallest(nums, k))

```
In the example above, the function should return `2`. If we sort the list, it becomes `[1, 2, 3, 4, 5, 6]`. The 2nd smallest number is `2`, so the function returns `2`.
