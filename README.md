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

## Pseudo Code

Start by defining the function `find_kth_smallest` that takes in two parameters: `nums` (an array of numbers), and `k` (an integer indicating the kth smallest element we are interested in).

1. Inside the function, initialize a new max heap.
2. Iterate over each number in the `nums` array.
3. For each number, insert it into the max heap.
4. After every insertion, check if the size of the heap is greater than `k`.
5. If the size of the heap is indeed greater than `k`, remove the maximum value from the heap. This ensures that the heap only keeps the smallest `k` numbers at any point during the iteration.
6. After going through all the numbers in `nums`, the max heap now contains the k smallest numbers in the array. However, since it's a max heap, the root of the heap is the largest of these k smallest numbers, which is effectively the kth smallest number in the array.
7. Return the root of the heap (the kth smallest number in the array) by removing the root from the max heap and returning it as the result of the function.

### Explained another way:

Imagine you are playing a game where you have a basket that can hold only `k` marbles and you have a large box full of marbles (these are our `nums`). The marbles are different sizes and you want to find the kth smallest marble.

1. To do this, you start picking marbles from the box one by one (this is our for loop) and put each one in the basket (`max_heap.insert(num)`).
2. But, remember, your basket can only hold `k` marbles.
3. So, when you put in a marble and the basket becomes too full (meaning it has more than `k` marbles), you need to take out the biggest marble (`max_heap.remove()`). This way, your basket will always have the k smallest marbles you've seen so far.
4. Once you've looked at all the marbles in the box (finished the for loop), you will have the `k` smallest marbles in your basket. But you want the kth smallest, not the smallest `k`.
5. Since you've been taking out the biggest marble whenever your basket was too full, the biggest marble in your basket now will be the kth smallest marble from the box.
6. So, you take out the biggest marble from your basket one last time (`max_heap.remove()`) and that's your answer!
