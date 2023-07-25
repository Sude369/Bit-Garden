---
{"dg-publish":true,"permalink":"/python/python-reference/string-methods/","created":"","updated":""}
---

- ### Case Manipulation
	- **.capitalize()**
		-  **.capitalize()** is a string method in Python that is used to capitalize the first character of a string while converting all other characters to lowercase. It doesn't modify the original string but returns a new string with the capitalized first character.
		- **Syntax:** 
			```python
			.capitalize()
			```
		- **Parameters:** The `.capitalize()`method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns a new string with the first character capitalized and all other characters converted to lowercase.
		- ***Examples***
			- In this example, the original string "hello, world!" is transformed using `.capitalize()` resulting in "Hello, world!" as the output.
				```python
				original_string = "hello, world!"
				capitalized_string = original_string.capitalize()
				print(capitalized_string)
				# Output: Hello, world!
				```
			- It's important to note that `.capitalize()` only capitalizes the first character of the string and converts the rest of the characters to lowercase. If you have a string with multiple words separated by spaces, only the first word will be capitalized, and the rest will be in lowercase.
				```python
				original_string = "hello there, how are you?"
				capitalized_string = original_string.capitalize()
				print(capitalized_string)
				# Output: Hello there, how are you?
				```
			- Keep in mind that the `.capitalize()` method will not modify the original string but create a new string with the capitalized first character. If you want to change the original string itself, you should reassign the new string back to the original variable.
				```python
				original_string = "hello, world!"
				original_string = original_string.capitalize()
				print(original_string)  
				# Output: "Hello, world!"
				```









