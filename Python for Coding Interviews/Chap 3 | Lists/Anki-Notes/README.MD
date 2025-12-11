lists (anki)

**Q1**: What does `append() ` do and what is its Time Complexity ? 

**Solution:**

- `append()` : adds an element to the end of the list

- Time Complexity :O(1)



**Q2**: What does `pop()` do in a list ? 

**Solution**: 

- Removes and returns the last element

- If the list is empty, calling `pop()` raises an `IndexError`.



**Q3**: How do you remove an element at a specific index using `pop()` ? 

**Solution:**

- Pass the index to `pop(index)`.

- Popping an out-of-bounds index also raises an `IndexError`.

**Q4**: What is the Time Complexity of the `pop()` operation in python ? 

**Solution**:

Time Complexity :O(1)

**Q5**: What does the `insert()` method do in a Python list ? 

**Solution:**

- Inserts an element at a specified index.

- If the index is too large, the element is added at the **end**if the index is negative, it is added at the **beginning**.

**Q6:** What is the Time Compexity of `insert()` method in Python ? 

**Solution:**

Time complexity: O(n), where n is the number of elements in the list.

**Q7**:What  does `list.index(x)` return ? 

**Solution**:

- The index of the first occurrence of `x`
- Raises `ValueError` if `x` not found

**Q8**: What error does `list.index(x)` raise when the element is missing ? 

**Solution**: `ValueError`

**Q9**: Time Complexity of `index()` on a list ? 

**Solution**:

- O(n)
- Linear scan

**Q10**: What does `list.remove(x) do ? 

**Solution**:

- Removes the first occurrence of `x` from the list 
- Modifies the list in place

**Q11**: Time Complexity of `remove()` on a list ? 

**Solution**:

- O(n)
- Must search + shift elements

**Q11**: What does `list.extend(other_list)` do ? 

**Solution**:

- Adds all elements to another list to the end 

```python
my_list = [1, 3, 2, 3]

my_list.extend([4, 5]) # [1, 3, 2, 3, 4, 5]
```

**Q12**:Which operator checks if an element is in a list?

**Solution**:`in`

**Q13**: Time Complexity of the `in` operator on a list ? 

**Solution**:

- `O(n)`
- Linear search

**Q14**: Which operator concatenates two Python lists ? 

**Solution**: `+`

**Q15**: What is the difference between `+` and `extend()` ? 

**Solution**: `+` creates a new list

**Q16**: What is the time complexity of list concatenation with `+` ? 

**Solution**: `O(n+m)`

**Q17**: Create a list of five 0s 

**Solution**:

`[0] * 5` creates a list of 5 0s 

**Q18**: What is the time complexity of creating a list of 5 0s 

```python
my_list = [0] * 5   
```

**Solution**: `O(n)`

**Q19**: How do you clone a list using slicing in Python ? 

**Solution**:

- `original_list[:]`
- slicing creates a shallow copy

**Q20**: What type of copy does slicing create ? 

**Solution**:

- `Shallow copy`

**Q21**: What is the time complexity of cloning a list ? 

**Solution**: `O(n)` , n = list length

**Q22**: What is the basic syntax of a list comprehension, and what does each part mean?

**Solution**: 

`[expression for item in iterable]` — “expression” is what you put in the list, “item” is each element, and “iterable” is what you loop over.

Examples 

```python
my_list = [i for i in range(5)]

print(my_list) # [0, 1, 2, 3, 4]
```

**Q23**: What is the syntax of a list comprehension with a condition, and how does it work?

**Solution**:

`[expression for item in iterable if condition]` — the item is added **only if** the condition is true.

```python
arr = [1, 2, 3, 4, 5]

result = [i for i in arr if i % 2 == 0]
```

**Q24**: How does list comprehension work when iterating over two lists at the same time ? 

**Solution**:

`[expression for a, b in zip(list1, list2)]`

```python
arr1 = [1, 2, 3]
arr2 = [4, 5, 6]

result = [i + j for i, j in zip(arr1, arr2)]
```
