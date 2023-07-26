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
		- **Return Type:** String
		- **Examples**
			1. In this example, the original string "hello, world!" is transformed using `.capitalize()` resulting in "Hello, world!" as the output.
				```python
				original_string = "hello, world!"
				capitalized_string = original_string.capitalize()
				print(capitalized_string)
				# Output: Hello, world!
				```
			2. It's important to note that `.capitalize()` only capitalizes the first character of the string and converts the rest of the characters to lowercase. If you have a string with multiple words separated by spaces, only the first word will be capitalized, and the rest will be in lowercase.
				```python
				original_string = "hello there, how are you?"
				capitalized_string = original_string.capitalize()
				print(capitalized_string)
				# Output: Hello there, how are you?
				```
			3. Keep in mind that the `.capitalize()` method will not modify the original string bu@t create a new string with the capitalized first character. If you want to change the original string itself, you should reassign the new string back to the original variable.
				```python
				original_string = "hello, world!"
				original_string = original_string.capitalize()
				print(original_string)  
				# Output: "Hello, world!"
				```
	- **.casefold()**
		- **.casefold()** is another string method in Python that is used to perform caseless comparisons of strings. It's similar to the `.lower()` method but more aggressive in converting characters to lowercase. The primary use of `.casefold()` is for case-insensitive string comparisons.
		- **Syntax:** 
			```python
			.casefold()
			```
		- **Parameters:** The `.casefold()` method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns a new string with all characters converted to lowercase, including characters that do not have a lowercase equivalent.
		- **Return Type:** String
		- **Examples:**
			1. In this example, the `.casefold()` method is applied to a string with both uppercase and lowercase characters. The method converts all characters to lowercase, even those that do not have a lowercase equivalent. This makes it suitable for case-insensitive comparisons.
				```python
				original_string = "São Paulo"
				casefolded_string = original_string.casefold()
				print(casefolded_string)
				# Output: são paulo
				```
			2. Another example showing the case-insensitive comparison of two strings using `.casefold()`
				```python
				str1 = "Hello"
				str2 = "hello"
				if str1.casefold() == str2.casefold():
				print("The strings are case-insensitive equal.")
				else:
				print("The strings are different.")
				# Output: The strings are case-insensitive equal.
				```
			3. The difference between `.casefold()` and `.lower()` lies in how they handle certain special characters, particularly the German character "ß" (eszett). In German, "ß" is a lowercase character used to represent the sound "ss" in certain contexts. When converting strings to lowercase, the behavior of `.casefold()` and `.lower()` differs when it comes to this character.
				```python
				original_string = "STRAßE"  # The German word for "street"
				lower_case_string = original_string.lower()
				casefolded_string = original_string.casefold()
				print("Original String:", original_string)
				print("Lowercase String:", lower_case_string)
				print("Casefolded String:", casefolded_string)
				# Output: Original String: STRAßE
				# Output: Lowercase String: straße
				# Output: Casefolded String: strasse
				```
		- **Note:** It's important to be cautious when using `.casefold()` for case-insensitive comparisons, as it may alter the string in ways that you may not expect. In most cases, `.lower()` is sufficient for general case-insensitive comparisons.
	- **.lower()**
		- **.lower()** is a string method in Python used to convert all characters in a string to lowercase.
		- **Syntax:** 
			```python
			.lower()
			```
		- **Parameters:** The `.lower()` method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns a new string with all characters converted to lowercase.
		- **Return Type:** String
		- **Examples:**
			1. In this example, the `.lower()` method is used to convert the username input to lowercase, ensuring case insensitivity when processing the input. The `.title()` method is then used to capitalize the first letter of the username for a friendly greeting.
				```python
				username = input("Enter your username: ").lower()
				print(f"Welcome, {username.title()}!")
				```
			1. Here, `.lower()` is applied to both the user's input and the saved password, making the comparison case-insensitive. This allows users to enter their password using any combination of uppercase and lowercase letters.
				```python
				saved_password = "PassWord123"
				user_password = input("Enter your password: ")
				
				if user_password.lower() == saved_password.lower():
				print("Password is correct.")
				else:
				print("Incorrect password.")
				```
			1. In this example, `.lower()` is used to convert each menu option to lowercase. This ensures that the printed menu is presented uniformly in lowercase letters, regardless of how the options were initially capitalized.
				```python
				menu_options = ["Start", "Settings", "Help", "Exit"]
				formatted_menu = "\n".join(option.lower() for option in menu_options)
				print("Select an option:")
				print(formatted_menu)
				```
		- **Note:** `.lower()` is useful when you need to perform case-insensitive comparisons or when you want to standardize the case of characters in a string for processing purposes.
	- **.swapcase()**
		- **.swapcase()** is a string method in Python used to create a new string with the case of each character swapped. Uppercase characters will become lowercase, and lowercase characters will become uppercase.
		- **Syntax:** 
			```python
			.swapcase()
			```
		- **Parameters:** The `.swapcase()` method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns a new string with the case of each character swapped.
		- **Return Type:** String
		- **Examples:** 
			1. The `.swapcase()` method swaps the case of each character in the string. Uppercase characters become lowercase, and lowercase characters become uppercase. In this example, "Hello, World!" is transformed to "hELLO, wORLD!".
				```python
				# Example 1: Basic Case Swap
				original_string = "Hello, World!"
				swapped_string = original_string.swapcase()
				print(swapped_string)
				# Output hELLO, wORLD!
				```
			2. The `.swapcase()` method works on each character individually, regardless of its current case. This example demonstrates how mixed-case characters are flipped, resulting in "tHIs IS a mIXeD caSe sTRiNG."
				```python
				# Example 2: Swapping Mixed Case Characters
				mixed_case_string = "ThiS is A MixEd CASe StrIng."
				swapped_string = mixed_case_string.swapcase()
				print(swapped_string)
				# Output tHIs IS a mIXeD caSe sTRiNG.
				```
			3. The `.swapcase()` method doesn't change non-alphabetic characters. In this example, numbers and special characters are preserved while only the letter cases are swapped.
				```python
				# Example 3: Preserve Special Characters
				special_characters = "3xampl3 $tring! @BraV0"
				swapped_string = special_characters.swapcase()
				print(swapped_string)
				# Output 3XAMPL3 $TRING! @bRAv0
				```
			- **Note:** `.swapcase()` is useful when you need to invert the case of characters in a string. For instance, if you have text with various uppercase and lowercase characters and want to flip their cases, you can use `.swapcase()` to achieve this quickly.
	- **title()**
		- **.title()** is a string method in Python used to create a new string with the first character of each word capitalized.
		- **Syntax:** 
			```python
			.title()
			```
		- **Parameters:** The `.title()` method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns a new string with the first character of each word capitalized.
		- **Return Type:** String
		- **Examples:**
			1. The `.title()` method is applied to the user's input name, ensuring that the name is correctly formatted with the first letter of each word capitalized.
				```python
				user_input = input("Enter your name: ")
				formatted_name = user_input.title()
				print(f"Hello, {formatted_name}!")  
				# Input: "john doe" -> Output: "Hello, John Doe!"
				```
			2. The `.title()` method is used here to capitalize the first letter of each word in the sentence, creating a title-like format for the string.
				```python
				sentence = "python programming is fun"
				formatted_title = sentence.title()
				print(formatted_title)  
				# Output: "Python Programming Is Fun"
				```
			3. In this example, a list of names is converted to titles using .title(). Each name in the list is formatted with the first letter of each word capitalized.
				```python
				names = ["john smith", "emma stone", "michael jordan"]
				formatted_names = [name.title() for name in names]
				print(formatted_names)  
				# Output: ['John Smith', 'Emma Stone', 'Michael Jordan']
				```
		- **Note:** `.title()` is useful when you want to capitalize the first character of each word in a string. It is commonly used for formatting titles or when you want to ensure consistent capitalization for each word in a sentence.
	- **.upper()**
		- **.upper()** is a string method in Python used to convert all characters in a string to uppercase.
		- **Syntax:** 
			```python
			.upper()
			```
		- **Parameters:** The `.upper()` method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns a new string with all characters converted to uppercase.
		- **Return Type:** String
		- **Examples:
			1. In this scenario, the user is prompted to enter a message, and the `.upper()` method is used to convert the user's input to all uppercase letters.
				```python
				user_input = input("Enter a message: ")
				formatted_message = user_input.upper()
				print("Your message in uppercase:", formatted_message)
				# Output: Your message in uppercase: HELLO, WORLD!
				```
			2. In this example, the user is prompted to enter a password, and the `.upper()` method is applied to the user's input password to convert it to uppercase. This allows for a case-insensitive comparison with the `saved_password`.
				```python
				saved_password = "PASS123"
				user_password = input("Enter your password: ")
				
				if user_password.upper() == saved_password:
				    print("Password is correct.")
				else:
				    print("Incorrect password.")
				    # Output: Password is correct.
				```
			3. In this scenario, a list of words is provided, and the `.upper()` method is used to convert each word in the list to uppercase.
				```python
				words = ["apple", "banana", "orange", "grape"]
				uppercased_words = [word.upper() for word in words]
				print(uppercased_words)
				# Output ['APPLE', 'BANANA', 'ORANGE', 'GRAPE']
				```
		- **Note:** `.upper()` is useful when you need to convert all characters in a string to uppercase. It is commonly used when case-insensitive string matching is required or when you want to standardize the case for text processing purposes.
- ### **Searching:**
	- **.count()**
		- **.count()** is a string method in Python used to count the occurrences of a substring within a given string.
		- **Syntax:** 
		  ```python
		  .count(substring, start, end)
		  ```
		- **Parameters:** 
			- `substring` (required): The substring whose occurrences you want to count within the string.
			- `start` (optional): The starting index for the search. If provided, the method will count occurrences only after this index. If not specified, the search starts from the beginning of the string.
			- `end` (optional): The ending index for the search. If provided, the method will count occurrences only up to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns the number of occurrences of the specified `substring` within the string.
		- **Return Type:** Integer
		- **Examples:**
			1. In this example, we use the .count() method to count the number of times a specific character ("o") appears in the string "Hello, how are you?". The method returns 3 because the character "o" appears three times in the given string.
				```python
				text = "Hello, how are you?"
				character_to_count = "o"
				count = text.count(character_to_count)
				print(count)  
				# Output: 3
				```
			1. In this example, we use the .count() method to count the number of times a specific substring ("aba") appears in the string "ababababab". The method returns 2 since the substring "aba" appears twice in the given string.
				```python
				text = "ababababab"
				substring_to_count = "ab"
				count = text.count(substring_to_count)
				print(count)  
				# Output: 5
				```
			1. This example is similar to the previous one, but it includes a note to clarify that the .count() method does not count overlapping occurrences of the substring. The method still returns 2, even if there are overlapping instances of the substring "aba" in the string "ababababab". This is because .count() counts non-overlapping occurrences only.
				```python
				text = "ababababab"
				substring_to_count = "aba"
				count_without_overlap = text.count(substring_to_count)
				print(count_without_overlap)  
				#  Output: 2
				```
		 - **Note:** The .count() method is handy when you need to find out how many times a particular substring appears in a larger string. It can be useful for tasks such as analyzing text data or checking the frequency of specific elements within a string.
	- **.find()**
		- **.find()** method is used to find the index of the first occurrence of a specified `substring` within a given string. If the substring is not found, it returns -1.
		- **Syntax:** 
			```python
			.find(substring, start, end)
			```
		- **Parameters:**
			- `substring` (required): The substring whose index you want to find within the string.
			- `start` (optional): The starting index for the search. If provided, the method will search for the substring only after this index. If not specified, the search starts from the beginning of the string.
			- `end` (optional): The ending index for the search. If provided, the method will search for the substring only up to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns the index of the first occurrence of the specified `substring` within the string. If the substring is not found, it returns -1.
		- **Return Type:** Integer
		- **Examples:
			1. Finding a substring in a string:
				```python
				original_string = "Hello, how are you?"
				substring = "how"
				index = original_string.find(substring)
				print(index)  # Output: 7
				```
			1. Checking if a substring exists in a string:
				```python
				original_string = "The quick brown fox jumps over the lazy dog."
				substring = "cat"
				index = original_string.find(substring)
				print(index)  # Output: -1 (Substring "cat" is not found in the original string)
				```
			1. Finding a substring with a starting index:
				```python
				original_string = "This is a test string. This is another test."
				substring = "is"
				start_index = 3
				index = original_string.find(substring, start_index)
				print(index)  # Output: 5 (The first occurrence of "is" after index 3 is found at index 5)
				```
- **.index(substring, start, end)**
- **Description:** The `.index()` method is similar to `.find()`, but it raises a `ValueError` if the specified `substring` is not found in the string, instead of returning -1.
- **Syntax:** 
```python
.index(substring, start, end)
```
- **Parameters:** The parameters are the same as for the `.find()` method (see above).
- **Return Value:** The method returns the index of the first occurrence of the specified `substring` within the string. If the substring is not found, it raises a `ValueError`.
- **Return Type:** Integer

- **.replace(old, new, count)**
- **Description:** The `.replace()` method is used to create a new string where all occurrences of the `old` substring are replaced with the `new` substring. Optionally, you can specify the `count` parameter to limit the number of replacements.
- **Syntax:** 
```python
.replace(old, new, count)
```
- **Parameters:**
- `old` (required): The substring to be replaced.
- `new` (required): The substring that will replace the occurrences of `old`.
- `count` (optional): The maximum number of replacements to be made. If not specified, all occurrences of `old` will be replaced.
- **Return Value:** The method returns a new string with the specified replacements.
- **Return Type:** String

- **.rfind(substring, start, end)**
- **Description:** The `.rfind()` method works similar to `.find()`, but it searches for the last occurrence of the specified `substring` within the string.
- **Syntax:** 
```python
.rfind(substring, start, end)
```
- **Parameters:** The parameters are the same as for the `.find()` method (see above).
- **Return Value:** The method returns the index of the last occurrence of the specified `substring` within the string. If the substring is not found, it returns -1.
- **Return Type:** Integer

- **.rindex(substring, start, end)**
- **Description:** The `.rindex()` method is similar to `.rfind()`, but it raises a `ValueError` if the specified `substring` is not found in the string, instead of returning -1.
- **Syntax:** 
```python
.rindex(substring, start, end)
```
- **Parameters:** The parameters are the same as for the `.rfind()` method (see above).
- **Return Value:** The method returns the index of the last occurrence of the specified `substring` within the string. If the substring is not found, it raises a `ValueError`.
- **Return Type:** Integer

These string methods are very useful for various string manipulation tasks, such as searching for substrings, replacing text, and handling string indices efficiently.

