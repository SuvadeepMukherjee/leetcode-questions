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
