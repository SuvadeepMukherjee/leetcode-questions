# Anki Notes -sorting 

**Q1**: What does the `.sort()` method do by default in Python ? 

**Solution**:

- Sorts a list in ascending order in-place 
- It modifies the original list and returns `None`

```python
elements = [5, 3, 6, 2, 1]

elements.sort()

print(elements) # [1, 2, 3, 5, 6]
```

**Q2**: How are strings sorted when using `.sort()` ? 

**Solution**:

- In lexicographical order.
- Example: `"apple"` comes before `"banana"`

**Q3**: What is the time and space complexity of Python's `.sort()` method ? 

**Solution**:

- Time Complexity 
  - O(n log n)
  - `.sort()` uses the Timsort algorithm.
- Space Complexity 
  - O(n)
  - Needed because Timsort uses temporary arrays.

**Q4**: Which sorting algorithm does Python use for `.sort()`?

**Solution**:

- Timsort
- A hybrid of merge sort and insertion sort

**Q6**: Show the function signature of `.sort()` function in Python 

**Solution**:

- The `.sort()` method also accepts some optional parameters. This is the `.sort()` function signature:

  ```python
  def sort(key=None, reverse=False) -> None:	
  ```

- The `key` parameter allows us to customize the sorting order

- The `reverse` parameter is a boolean value that determines whether the list should be sorted in *descending order*. By default, it is set to `False`

**Q5**: How do you sort a list in descending order using `.sort()`?

**Solution**:

- Use `reverse=True`

  ```python
  elements = [5, 3, 6, 2, 1]
  
  elements.sort(key=None, reverse=True)
  
  print(elements) # [6, 5, 3, 2, 1]
  ```

- We can actually omit the `key` parameter and only pass the `reverse` parameter

  ```python
  elements.sort(reverse=True)
  ```

**Q6**: What is the purpose of the `key` parameter in `.sort()` ? 

**Solution**:

- To define a custom sorting order.
- It expects a function that returns the sorting value.

Example : 

```python
def get_word_length(word: str) -> int:
    return len(word)

words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]

words.sort(key=get_word_length)

print(words) # ['kiwi', 'pear', 'apple', 'banana', 'cherry', 'blueberry', 'watermelon']


```

**Q7**: What does a Lambda function allow you to do in sorting ? 

**Solution**:

- define a custom sorting order.

**Q8**: Sort this list by the length of each word with the help of lambda function 

```python
words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]
```

**Solution**:

```python
words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]

words.sort(key=lambda word: len(word))

print(words) # ['kiwi', 'pear', 'apple', 'banana', 'cherry', 'blueberry', 'watermelon']
```

The syntax includes:

1. The keyword `lambda`.
2. The input variable `word`. We can use any variable name here.
3. The colon `:`, after which we define the function body.
4. The expression `len(word)`, which is the return value of the function.

Note ➡️ A lambda function must be a single expression, and it cannot contain multiple statements

**Q9**: Fill in the table 

|             | Returns | Modifies Original |
| ----------- | ------- | ----------------- |
| `.sort()`   |         |                   |
| `.sorted()` |         |                   |

**Solution**:

|             | Returns         | Modifies Original             |
| ----------- | --------------- | ----------------------------- |
| `.sort()`   | None            | Yes                           |
| `.sorted()` | new sorted list | does not modify original list |

