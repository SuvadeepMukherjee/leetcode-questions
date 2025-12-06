# Strings

## Length Function

- Suppose we had a string like `my_str = "NeetCode"` and we wanted to know how many characters are in the string

-  We can use a built-in function called `len()` to find the length of a string

  ```python
  my_str = "NeetCode"
  print(len(my_str))  # Output: 8
  ```

## String Indexing

- Suppose we want to access individual characters from a string. We can do this by **indexing** the string.

- ```python
  my_str = "Hello"
  print(my_str[0])  # Output: H
  print(my_str[1])  # Output: e
  print(my_str[2])  # Output: l
  print(my_str[3])  # Output: l
  print(my_str[4])  # Output: o
  ```

## String Looping

```python
my_string = "Hello, World!"

length = len(my_string) # 13

for i in range(length):
    print(my_string[i])
```

## String Looping Shorthand

- we can use a shorthand to loop through each character in the string:

  ```python
  my_string = "Hello"
  
  for char in my_string:
      print(char)
  ```

- This code will output:

- ```plaintext
  H
  e
  l
  l
  o
  ```

- Directly using the `in` keyword allows us to iterate through each character of the string without needing to use the index. We used the name `char` for readability, but you can use any name you want, like `c` or `i`.

## String Concatenation

- **concatenation** is the process of combining two or more strings into a single string

- Python provides the `+` operator for concatenating strings

- When you use the `+` operator with two strings, Python joins them together to create a new string.

  ```python
  str1 = "Hello, "
  str2 = "world!"
  print(str1 + str2) # Output: Hello, world!
  ```

## String Slicing

- If we only want to access a portion of a string we can use **slicing**. Slicing allows us to extract a substring from a string, by specifying a range of indices.

  ```python
  my_string = "Hello, World!"
  
  start, end = 1, 5
  
  print(my_string[start:end])  # Output: ello
  ```

- In this example, we are extracting the substring from index 1 to 5 (not including 5) from the string `"Hello, World!"`.

- With string slicing we are actually not required to specify either the start or the end index.

- If we don't specify the start, it's equivalent to starting from the beginning of the string.

- If we don't specify the end, it's equivalent to ending at the end of the string.

- If we don't specify either, we get the entire string.

  

  ```python
  my_string = "NeetCode"
  
  print(my_string[:3])  # Output: Nee
  
  print(my_string[0:3]) # Output: Nee
  
  print(my_string[4:])  # Output: Code
  
  print(my_string[4:8]) # Output: Code
  
  print(my_string[:])  # Output: NeetCode
  
  print(my_string)     # Output: NeetCode
  ```

## Reversing a String

- We can also use slicing to reverse a string. By not specifying the starting index or the ending index, and setting the step to -1, the string will be reversed.

  ```python
  my_string = "Hello"
  
  print(my_string[::-1])  # Output: olleH
  ```

- Notice that we have two colons in the slicing syntax. This will make more sense if you look at the below example:

  ```python
  my_string = "Hello"
  start, end, step = 1, 4, 1
  
  print(my_string[start:end:step])   # Output: ell
  
  start, end, step = 3, 0, -1
  
  print(my_string[start:end:step]) # Output: lle
  ```

- The value before the first colon is the starting index, the value after the first colon is the ending index, and the value after the second colon is the step. If the step is negative, the string will be reversed.
- Remember that the starting index is inclusive, and the ending index is exclusive, even when the step is negative.

## Strings are Immutable

- It's important to know that whenever you slice a string, you are not modifying the underlying string.

- Instead, you are creating a new string with the sliced characters. This is because strings are **immutable** in Python, which means they cannot be changed after they are created.

  ```python
  message = "I will never change."
  
  message[0] = "X" # This will cause an error
  ```

- In the above code, we try to reassign just the first character of the string. This will cause a **TypeError** because strings are immutable. We cannot change individual characters, we can only reassign the entire string.

- If we wanted to create a new string with the second character removed, we can accomplish this by slicing and concatenation.

- ```python
  message = "I will never change."
  
  before_second = message[:1] # "I"
  after_second = message[2:]  # "will never change."
  
  new_message = before_second + after_second
  ```

## String Formatting

- We saw that we can concatenate strings using the `+` operator. However, this can be cumbersome when we have many strings to concatenate. Python provides a more elegant way to format strings using the `format` method.

- ```python
  name = "Alice"
  age = 25
  
  msg = "Hello, {}. You are {} years old.".format(name, age)
  
  print(msg)  # Output: Hello, Alice. You are 25 years old.
  ```

- In the above code, we have a string with two placeholders: `{}`. We then call the `format` method on the string and pass in the values we want to replace the placeholders with. The values are passed in the order they are to be inserted. The number of placeholders must match the number of arguments passed to the `format` method.

- You can also use the index of the placeholders to specify the order of the arguments.

  ```python
  name = "Alice"
  age = 25
  
  msg = "Hello, {1}. You are {0} years old.".format(age, name)
  
  print(msg)  # Output: Hello, Alice. You are 25 years old
  ```

- An even more concise way to format strings is to use **f-strings**. These are prefixed with an `f` before the string and allow you to insert variables directly into the string.

  ```python
  name = "Alice"
  age = 25
  
  msg = f"Hello, {name}. You are {age} years old."
  ```