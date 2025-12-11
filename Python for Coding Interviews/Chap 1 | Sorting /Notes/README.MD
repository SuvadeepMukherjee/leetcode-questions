# Sorting 

## Sort Ascending 

- We can sort a list of elements by calling `.sort()` on the list 

- By default, the `.sort()` method sorts the elements in *ascending* order *in-place*. The return value of the `.sort()` method is `None`.

  ```python
  elements = [5, 3, 6, 2, 1]
  
  elements.sort()
  
  print(elements) # [1, 2, 3, 5, 6]
  ```

- This method also works for a list of strings.By default, strings are sorted in [lexicographical order](https://en.wikipedia.org/wiki/Lexicographic_order).

- ```python
  elements = ["grape", "apple", "banana", "orange"]
  
  elements.sort()
  
  print(elements) # ['apple', 'banana', 'grape', 'orange']
  ```

- Time and Space Complexity 
  - The time complexity of the `.sort()` method is O(nlogn), where `n` is the number of elements in the list.
  - The space complexity is O(n), where `n` is the number of elements in the list.
  - Python uses the [Timsort](https://en.wikipedia.org/wiki/Timsort) algorithm for sorting lists. Timsort is a hybrid sorting algorithm derived from merge sort and insertion sort

## Sort Descending

- The `.sort()` method also accepts some optional parameters. This is the `.sort()` function signature:

  ```python
  def sort(key=None, reverse=False) -> None:
  ```

  - The `key` parameter allows us to customize the sorting order
  - The `reverse` parameter is a boolean value that determines whether the list should be sorted in *descending order*. By default, it is set to `False`.

- If we want to sort a list in descending order, we can set the `reverse` parameter to `True`.

  ```python
  elements = [5, 3, 6, 2, 1]
  
  elements.sort(key=None, reverse=True)
  
  print(elements) # [6, 5, 3, 2, 1]
  ```

- We can actually omit the `key` parameter and only pass the `reverse` parameter, by using a feature of Python called *keyword arguments*.

  ```python
  elements.sort(reverse=True)
  ```

## Sort Custom

- We can also specify a custom sorting order by using the `key` parameter in the `.sort()` method. The `key` parameter doesn't accept a value, instead, it accepts a *function* that returns a value to be used for sorting.

  ```python
  def get_word_length(word: str) -> int:
      return len(word)
  
  words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]
  
  words.sort(key=get_word_length)
  
  print(words) # ['kiwi', 'pear', 'apple', 'banana', 'cherry', 'blueberry', 'watermelon']
  ```

## Sort Lambda 

- Defining a separate function just to pass it into the `key` parameter of the `.sort()` method can be cumbersome. We can use a *lambda function* to define a function in a single line and pass it directly to the `.sort()` method.

- To sort a list of words by their length, we can use a lambda function like this:

  ```python
  words = ["apple", "banana", "kiwi", "pear", "watermelon", "blueberry", "cherry"]
  
  words.sort(key=lambda word: len(word))
  
  print(words) # ['kiwi', 'pear', 'apple', 'banana', 'cherry', 'blueberry', 'watermelon']
  ```

- The lambda function `lambda word: len(word)` is equivalent to the function `get_word_length` we defined in the previous example. It takes a word as input and returns the length of the word.
- The syntax includes:
  1. The keyword `lambda`.
  2. The input variable `word`. We can use any variable name here.
  3. The colon `:`, after which we define the function body.
  4. The expression `len(word)`, which is the return value of the function.
- A lambda function must be a single expression, and it cannot contain multiple statements

## Sorted Copy 

- There is another way to sort a list in Python, using the `sorted()` function
- For the most part, it's similar to the `sort()` method, but it returns a new list instead of modifying the original list.

