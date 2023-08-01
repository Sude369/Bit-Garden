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
			3. Keep in mind that the `.capitalize()` method will not modify the original string but create a new string with the capitalized first character. If you want to change the original string itself, you should reassign the new string back to the original variable.
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
- ### Searching:
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
			2. Checking if a substring exists in a string:
				```python
				original_string = "The quick brown fox jumps over the lazy dog."
				substring = "cat"
				index = original_string.find(substring)
				print(index)  # Output: -1 (Substring "cat" is not found in the original string)
				```
			3. Finding a substring with a starting index:
				```python
				original_string = "This is a test string. This is another test."
				substring = "is"
				start_index = 3
				index = original_string.find(substring, start_index)
				print(index)  # Output: 5 (The first occurrence of "is" after index 3 is found at index 5)
				```
	- **.index()**
		- **.index()** method is similar to `.find()`, but it raises a `ValueError` if the specified `substring` is not found in the string, instead of returning -1.
		- **Syntax:** 
			```python
			.index(substring, start, end)
			```
		- **Parameters:**
			- `substring` (required): The substring whose index you want to find within the string.
			- `start` (optional): The starting index for the search. If provided, the method will search for the substring only after this index. If not specified, the search starts from the beginning of the string.
			- `end` (optional): The ending index for the search. If provided, the method will search for the substring only up to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns the index of the first occurrence of the specified `substring` within the string. If the substring is not found, it raises a `ValueError`.
		- **Return Type:** Integer
		- **Examples()**
			1. Finding the index of a substring:
				```python
				original_string = "Hello, how are you?"
				substring = "how"
				index = original_string.index(substring)
				print(index)  # Output: 7
				```
			2. Finding the index of a character:
				```python
				text = "Python"
				character = "t"
				index = text.index(character)
				print(index)  # Output: 2 (The first occurrence of 't' is at index 2)
				```
			3. Finding the index with a starting and ending index:
				```python
				original_string = "The quick brown fox jumps over the lazy dog."
				substring = "fox"
				start_index = 4
				end_index = 20
				index = original_string.index(substring, start_index, end_index)
				print(index)  # Output: 16 (Substring "fox" is found between index 16 and 18)
				```
	- **.replace()**
		- .replace() method is used to create a new string where all occurrences of the old substring are replaced with the new substring. Optionally, you can specify the count parameter to limit the number of replacements.
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
		- **Examples:**
			1. Simple replacement of a substring:
				```python
				original_string = "The quick brown fox jumps over the lazy dog."
				old_substring = "fox"
				new_substring = "cat"
				new_string = original_string.replace(old_substring, new_substring)
				print(new_string)
				# Output: "The quick brown cat jumps over the lazy dog."
				```
			1. Replacing all occurrences of a substring:
				```python
				original_string = "I love Python, Python is great!"
				old_substring = "Python"
				new_substring = "Java"
				new_string = original_string.replace(old_substring, new_substring)
				print(new_string)
				# Output: "I love Java, Java is great!"
				```
			1. Replacing with a specified maximum number of occurrences:
				```python
				original_string = "one one two one three one four"
				old_substring = "one"
				new_substring = "five"
				max_occurrences = 2
				new_string = original_string.replace(old_substring, new_substring, max_occurrences)
				print(new_string)
				# Output: "five five two one three one four"
				```
	- **.rfind()**
		- **.rfind()** method works similar to `.find()`, but it searches for the last occurrence of the specified `substring` within the string.
		- **Syntax:** 
			```python
			.rfind(substring, start, end)
			```
		- **Parameters:**- 
			- `substring` (required): The substring whose index you want to find within the string.
			- `start` (optional): The starting index for the search. If provided, the method will search for the substring only after this index. If not specified, the search starts from the beginning of the string.
			- `end` (optional): The ending index for the search. If provided, the method will search for the substring only up to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns the index of the last occurrence of the specified `substring` within the string. If the substring is not found, it returns -1.
		- **Return Type:** Integer
		- **Examples:**
			1. Finding the last occurrence of a substring:
				```python
				original_string = "apple orange banana orange apple"
				substring = "orange"
				index = original_string.rfind(substring)
				print(index)  # Output: 19 (The last occurrence of "orange" starts at index 19)
				```
			1. Finding the last occurrence with a starting and ending index:
				```python
				original_string = "Hello, how are you? I'm fine, thank you."
				substring = "you"
				start_index = 0
				end_index = 20
				index = original_string.rfind(substring, start_index, end_index)
				print(index)  # Output: 10 (The last occurrence of "you" within the range [0, 20) starts at index 10)
				```
			1. Finding the last occurrence of a character:
				```python
				text = "Python programming is fun!"
				character = "m"
				index = text.rfind(character)
				print(index)  # Output: 17 (The last occurrence of 'm' is at index 17)
				```
	- **.rindex()**
		- **.rindex()** method is similar to `.rfind()`, but it raises a `ValueError` if the specified `substring` is not found in the string, instead of returning -1.
		- **Syntax:** 
			```python
			.rindex(substring, start, end)
			```
		- **Parameters:** 
			- `substring` (required): The substring whose index you want to find within the string.
			- `start` (optional): The starting index for the search. If provided, the method will search for the substring only after this index. If not specified, the search starts from the beginning of the string.
			- `end` (optional): The ending index for the search. If provided, the method will search for the substring only up to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns the index of the last occurrence of the specified `substring` within the string. If the substring is not found, it raises a `ValueError`.
		- **Return Type:** Integer
		- **Examples:**
			1. Finding the last occurrence of a substring:
				```python
				original_string = "apple orange banana orange apple"
				substring = "orange"
				index = original_string.rindex(substring)
				print(index)  # Output: 19 (The last occurrence of "orange" starts at index 19)
				```
			1. Finding the last occurrence with a starting and ending index:
				```python
				original_string = "Hello, how are you? I'm fine, thank you."
				substring = "you"
				start_index = 0
				end_index = 20
				index = original_string.rindex(substring, start_index, end_index)
				print(index)  # Output: 10 (The last occurrence of "you" within the range [0, 20) starts at index 10)
				```
			1. Finding the last occurrence of a character:
				```python
				text = "Python programming is fun!"
				character = "m"
				index = text.rindex(character)
				print(index)  # Output: 17 (The last occurrence of 'm' is at index 17)
				```
- ### Validation
	- **.endswith()**
		- **.endswith()** method checks whether a string ends with a specified `suffix`.
		- **Syntax:** 
			```python
			.endswith(suffix, start, end)
			```
		- **Parameters:**
			- `suffix` (required): The substring to check if it is at the end of the string.
			- `start` (optional): The starting index for the search. If provided, the method will check the substring only after this index. If not specified, the search starts from the beginning of the string.
			- `end` (optional): The ending index for the search. If provided, the method will check the substring only up to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns `True` if the string ends with the specified `suffix`, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text = "Hello, World!"
				suffix = "World!"
				print(text.endswith(suffix))  # Output: False (case-sensitive)
				```
			1. Example 2:
			```python
			text = "Hello, World!"
			suffix = "World!"
			print(text.endswith(suffix))  # Output: False (case-sensitive)
			```
			1. Example 3:
				```python
				text = "Python programming is fun!"
				suffix = "fun!"
				print(text.endswith(suffix))  # Output: True
				```
	- **.isalnum()**
		- **.isalnum()** method checks whether all characters in a string are alphanumeric (consisting of letters and numbers).
		- **Syntax:** 
			```python
			.isalnum()
			```
		- **Parameters:** The `.lower()` method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are alphanumeric, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Checking if a string ends with a specific suffix:
				```python
				file_name = "example.txt"
				suffix = ".txt"
				result = file_name.endswith(suffix)
				print(result)  
				# Output: True
				```
			2. Case-insensitive check:
				```python
				text = "Hello, World!"
				suffix = "world!"
				result = text.endswith(suffix)
				print(result)  # Output: False (The case doesn't match)
				result = text.endswith(suffix, 7)  # Specify a starting index for the check
				print(result)  
				# Output: True (The suffix "world!" matches at index 7)
				```
			3. Checking with multiple possible suffixes:
				```python
				file_name = "document.docx"
				suffixes = (".txt", ".pdf", ".docx")
				result = file_name.endswith(suffixes)
				print(result)  
				# Output: True (The file_name ends with ".docx" which is in the tuple)
				```
	- **.isalpha()**
		- **.isalpha ()** method checks whether all characters in a string are alphabetic (letters).
		- **Syntax:** 
			```python
			.isalpha()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are alphabetic, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example with alphabetic characters:
				```python
				text1 = "Hello"
				print(text1.isalpha())  # Output: True
				
				text2 = "Hello123"
				print(text2.isalpha())  # Output: False
				```
			2. Handling different letter cases:
				```python
				text = "Hello World"
				print(text.isalpha())  # Output: False
				print(text.isalpha() and text.replace(" ", "").isalpha())  # Output: True
				```
			3. Checking for an empty string:
				```python
				empty_string = ""
					print(empty_string.isalpha())  # Output: False
				```
	- **.isascii()**
		- **.isascii()** method checks whether all characters in a string are ASCII characters (in the range of 0 to 127).
		- **Syntax:** 
			```python
			.isascii()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are ASCII characters, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "Hello, World!"
				print(text1.isascii())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "こんにちは"
				print(text2.isascii())  # Output: False
				```
			3. Example 3:
				```python
				text3 = "12345"
				print(text3.isascii())  # Output: True
				```
	- **.isdecimal()**
		- **.isdecimal()** method checks whether all characters in a string are decimal characters (0-9).
		- **Syntax:** 
			```python
			.isdecimal()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are decimal characters, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "12345"
				print(text1.isdecimal())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "12.34"
				print(text2.isdecimal())  # Output: False
				```
			3. Example 3:
				```python
				text3 = "Hello"
				print(text3.isdecimal())  # Output: False
				```
			4. Example 4:
				```python
				complex_number = "3+4j"
				print(complex_number.isdecimal())  # Output: False
				```
	- **.isdigit()**
		- **.isdigit()** method checks whether all characters in a string are digits (0-9). Additionally, it returns `True` for some special digits like superscript and subscript digits.
		- **Syntax:** 
			```python
			.isdigit()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are digits, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "12345"
				print(text1.isdigit())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "12.34"
				print(text2.isdigit())  # Output: False
				```
			3. Example 3:
				```python
				text3 = "Hello"
				print(text3.isdigit())  # Output: False
				```
	- **.isidentifier()**
		- **.isidentifier()** method checks whether a string is a valid Python identifier (e.g., variable name, function name). It returns `True` if the string can be used as an identifier, otherwise it returns `False`.
		- **Syntax:** 
			```python
			.isidentifier()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if the string is a valid Python identifier, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "variable_name"
				print(text1.isidentifier())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "123abc"
				print(text2.isidentifier())  # Output: False
				
				text3 = "if"
				print(text3.isidentifier())  # Output: False
				```
			3. Example 3:
				```python
				text4 = "_private_variable"
				print(text4.isidentifier())  # Output: True
				```
	- **.islower()**
		- **.islower()** method checks whether all characters in a string are lowercase letters.
		- **Syntax:** 
			```python
			.islower()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are lowercase letters, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "hello"
				print(text1.islower())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "Hello"
				print(text2.islower())  # Output: False (contains an uppercase letter)
				```
			3. Example 3:
				```python
				text3 = "123abc"
				print(text3.islower())  # Output: True (non-alphabetic characters are ignored)
				```
	- **.isnumeric()**
		- **.isnumeric()** method checks whether all characters in a string are numeric characters (including digits, fractions, subscripts, superscripts, etc.).
		- **Syntax:** 
			```python
			.isnumeric()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are numeric, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "hello"
				print(text1.islower())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "Hello"
				print(text2.islower())  # Output: False (contains an uppercase letter)
				```
			3. Example 3:
				```python
				text3 = "123abc"
				print(text3.islower())  # Output: True (non-alphabetic characters are ignored)
				```
	- **.isprintable()**
		- **.isprintable()** method checks whether all characters in a string are printable (i.e., they don't require special interpretation for display).
		- **Syntax:** 
			```python
			.isprintable()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are printable, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "Hello, World!"
				print(text1.isprintable())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "Hello\nWorld"
				print(text2.isprintable())  # Output: False (contains a newline character)
				```
			3. Example 3:
				```python
				text3 = "12345"
				print(text3.isprintable())  # Output: True (all characters are printable)
				```
	- **.isspace()**
		- **.isspace()** method checks whether all characters in a string are whitespace characters (e.g., space, tab, newline).
		- **Syntax:** 
			```python
			.isspace()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are whitespace characters, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "   "
				print(text1.isspace())  # Output: True (contains only spaces)
				```
			2. Example 2:
				```python
				text2 = "\t\t\t"
				print(text2.isspace())  # Output: True (contains only tabs)
				```
			3. Example 3:
				```python
				text3 = "Hello, World!"
				print(text3.isspace())  # Output: False (contains non-whitespace characters)
				```
	- **.istitle()**
		- **.istitle()** method checks whether a string is in title case (i.e., each word starts with an uppercase letter and the rest of the characters are lowercase).
		- **Syntax:** 
			```python
			.istitle()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if the string is in title case, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "This Is Title Case"
				print(text1.istitle())  # Output: True
				```
			2. Example 2:
				```python
				text2 = "This Is Not Title Case"
				print(text2.istitle())  # Output: False (the word "Not" should be all lowercase)
				```
			3. Example 3:
				```python
				text3 = "Python 101"
				print(text3.istitle())  # Output: True (both "Python" and "101" start with uppercase letters)
				```
	- **.isupper()**
		- **.isupper()** method checks whether all characters in a string are uppercase letters.
		- **Syntax:** 
			```python
			.isupper()
			```
		- **Parameters:** The method doesn't take any parameters. It operates directly on the string to which it is applied.
		- **Return Value:** The method returns `True` if all characters in the string are uppercase letters, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text1 = "HELLO"
				print(text1.isupper())  # Output: True
				```
			1. Example 2:
				```python
				text2 = "Hello"
				print(text2.isupper())  # Output: False (contains a lowercase letter)
				```
			1. Example 3:
				```python
				text3 = "123ABC"
				print(text3.isupper())  # Output: True (non-alphabetic characters are ignored)
				```
	- **.startswith()**
		- **.startswith()** method checks whether a string starts with a specified `prefix`.
		- **Syntax:** 
			```python
			.startswith(prefix, start, end)
			```
		- **Parameters:**
		- `prefix` (required): The substring to check if it is at the beginning of the string.
		- `start` (optional): The starting index for the search. If provided, the method will check the substring only after this index. If not specified, the search starts from the beginning of the string.
		- `end` (optional): The ending index for the search. If provided, the method will check the substring onlyup to this index (exclusive). If not specified, the search continues until the end of the string.
		- **Return Value:** The method returns `True` if the string starts with the specified `prefix`, otherwise it returns `False`.
		- **Return Type:** Boolean
		- **Examples:**
			1. Example 1:
				```python
				text = "Hello, World!"
				prefix = "Hello"
				print(text.startswith(prefix))  # Output: True
				```
			2. Example 2:
				```python
				text = "Hello, World!"
				prefix = "world"
				print(text.startswith(prefix))  # Output: False (case-sensitive)
				```
			3. Example 3:
				```python
				text = "Python programming is fun!"
				prefix = "Py"
				print(text.startswith(prefix))  # Output: True
				```
- ### Formatting
	- **.center()**
		- **.center()** method is used to center a string within a specified width by padding it with a `fillchar` on both sides.
		- **Syntax:** 
			```python
			.center(width, fillchar)
			```
		- **Parameters:**
			- `width` (required): The total width of the centered string.
			- `fillchar` (optional): The character used for padding the string. If not specified, it defaults to a space.
		- **Return Value:** The method returns a new string that is centered within the specified `width`.
		- **Return Type:** String
		- **Examples:**
			1. Centering a String with Spaces:
				```python
				original_string = "Hello"
				width = 10
				
				# Center the original_string within a width of 10 characters using spaces.
				centered_string = original_string.center(width)
				print(centered_string)  # Output: '  Hello   '
				```
			2. Centering a String with Custom Padding Characters:
				```python
				original_string = "Python"
				width = 15
				padding_character = "*"
				
				# Center the original_string within a width of 15 characters using '*' as padding characters.
				centered_string = original_string.center(width, padding_character)
				print(centered_string)  # Output: '****Python****'
				```
			3. Centering a Numeric String with Leading Zeros:
				```python
				numeric_string = "42"
				width = 6
				
				# Center the numeric_string within a width of 6 characters using leading zeros.
				centered_numeric_string = numeric_string.center(width, "0")
				print(centered_numeric_string)  # Output: '0042  '
				```
	- **.expandtabs()**
		- **.expandtabs()** method is used to replace tab characters ('\t') in a string with spaces, based on the given `tabsize`.
		- **Syntax:** 
			```python
			.expandtabs(tabsize)
			```
		- **Parameters:**
			- `tabsize` (optional): The number of spaces to replace each tab character. If not specified, it defaults to 8.
		- **Return Value:** The method returns a new string with tab characters replaced by spaces.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				text = "Hello\tworld\texample"
				expanded_text = text.expandtabs()
				print(expanded_text)
				# Output: "Hello   world   example"
				```
			2. Example 2:
				```python
				text = "Apples\tOranges\tBananas"
				expanded_text = text.expandtabs(4)
				print(expanded_text)
				# Output: "Apples  Oranges Bananas"
				```
			3. Example 3:
				```python
				text = "First\tName\t   Age\tCountry"
				expanded_text = text.expandtabs(6)
				print(expanded_text)
				# Output: "First Name    Age    Country"
				```
	- **.format()**
		- **.format()** method is used for string formatting and substitution. It replaces placeholders in the string with corresponding values from `args` or `kwargs`.
		- **Syntax:** 
			```python
			.format(*args, **kwargs)
			```
		- **Parameters:**
			- `args` (optional): Positional arguments used for substitution in the string.
			- `kwargs` (optional): Keyword arguments used for substitution in the string.
		- **Return Value:** The method returns a new string with the placeholders replaced by the provided values.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				name = "Alice"
				age = 30
				occupation = "Engineer"
				sentence = "My name is {}, I am {} years old, and I work as an {}.".format(name, age, occupation)
				print(sentence)
				# Output: "My name is Alice, I am 30 years old, and I work as an Engineer."
				```
			2. Example 2:
				```python
				item = "book"
				price = 25.99
				sentence = "I bought a {0} for ${1:.2f}.".format(item, price)
				print(sentence)
				# Output: "I bought a book for $25.99."
				```
			3. Example 3:
				```python
				first_name = "Bob"
				last_name = "Smith"
				greeting = "Hello, {first} {last}! How are you today?".format(first=first_name, last=last_name)
				print(greeting)
				# Output: "Hello, Bob Smith! How are you today?"
				```
	- **.ljust()**
		- **.ljust()** method is used to left-align a string within a specified width by padding it with a `fillchar` on the right.
		- **Syntax:** 
			```python
			.ljust(width, fillchar)
			```
		- **Parameters:**
			- `width` (required): The total width of the left-aligned string.
			- `fillchar` (optional): The character used for padding the string. If not specified, it defaults to a space.
		- **Return Value:** The method returns a new string that is left-aligned within the specified `width`.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				text = "Hello"
				width = 10
				justified_text = text.ljust(width)
				print(justified_text)
				# Output: "Hello     "
				```
			2. Example 2:
				```python
				text = "Python"
				width = 12
				padding_char = '-'
				justified_text = text.ljust(width, padding_char)
				print(justified_text)
				# Output: "Python------"
				```
			3. Example 3:
				```python
				text = "Hello, World!"
				width = 5
				justified_text = text.ljust(width)
				print(justified_text)
				# Output: "Hello, World!"
				```
	- **.rjust()**
		- **.rjust()** method is used to right-align a string within a specified width by padding it with a `fillchar` on the left.
		- **Syntax:** 
			```python
			.rjust(width, fillchar)
			```
		- **Parameters:**
			- `width` (required): The total width of the right-aligned string.
			- `fillchar` (optional): The character used for padding the string. If not specified, it defaults to a space.
		- **Return Value:** The method returns a new string that is right-aligned within the specified `width`.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				text = "Hello"
				width = 10
				justified_text = text.rjust(width)
				print(justified_text)
				# Output: "     Hello"
				```
			2. Example 2:
				```python
				text = "Python"
				width = 12
				padding_char = '-'
				justified_text = text.rjust(width, padding_char)
				print(justified_text)
				# Output: "------Python"
				```
			3. Example 3:
				```python
				text = "Hello, World!"
				width = 5
				justified_text = text.rjust(width)
				print(justified_text)
				# Output: "Hello, World!"
				```
	- **.strip()**
		- **.strip()** method is used to remove leading and trailing characters specified in `chars` from a string. If `chars` is not provided, it removes leading and trailing whitespaces.
		- **Syntax:** 
			```python
			.strip(chars)
			```
		- **Parameters:**
			- `chars` (optional): The characters to be removed from the string. If not specified, it defaults to removing whitespaces.
		- **Return Value:** The method returns a new string with leading and trailing characters removed.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				text = "   Hello, World!   "
				cleaned_text = text.strip()
				print(cleaned_text)
				# Output: "Hello, World!"
				```
			2. Example 2:
				```python
				text = "###***##Hello, Python!##***###"
				cleaned_text = text.strip("#*")
				print(cleaned_text)
				# Output: "Hello, Python!"
				```
			3. Example 3:
				```python
				text = "~~~~~Let's get rid of tildes~~~~~"
				cleaned_text = text.strip("~")
				print(cleaned_text)
				# Output: "Let's get rid of tildes"
				```
	- **.lstrip()**
		- **.lstrip()** method is used to remove leading characters specified in `chars` from a string. If `chars` is not provided, it removes leading whitespaces.
		- **Syntax:** 
			```python
			.lstrip(chars)
			```
		- **Parameters:**
		- `chars` (optional): The characters to be removed from the left side of the string. If not specified, it defaults to removing whitespaces.
		- **Return Value:** The method returns a new string with leading characters removed.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				text = "   Hello, World!   "
				cleaned_text = text.lstrip()
				print(cleaned_text)
				# Output: "Hello, World!   "
				```
			2. Example 2:
				```python
				text = "###***##Hello, Python!##***###"
				cleaned_text = text.lstrip("#*")
				print(cleaned_text)
				# Output: "Hello, Python!##***###"
				```
			3. Example 3:
				```python
				text = "~~~~~Let's keep some tildes~~~~~"
				cleaned_text = text.lstrip("~")
				print(cleaned_text)
				# Output: "Let's keep some tildes~~~~~"
				```
	- **.rstrip()**
		- **.rstrip()** method is used to remove trailing characters specified in `chars` from a string. If `chars` is not provided, it removes trailing whitespaces.
		- **Syntax:** 
			```python
			.rstrip(chars)
			```
		- **Parameters:**
			- `chars` (optional): The characters to be removed from the right side of the string. If not specified, it defaults to removing whitespaces.
		- **Return Value:** The method returns a new string with trailing characters removed.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				text = "   Hello, World!   "
				cleaned_text = text.rstrip()
				print(cleaned_text)
				# Output: "   Hello, World!"
				```
			2. Example 2:
				```python
				text = "###***##Hello, Python!##***###"
				cleaned_text = text.rstrip("#*")
				print(cleaned_text)
				# Output: "###***##Hello, Python!"
				```
			3. Example 3:
				```python
				text = "~~~~~Let's keep some tildes~~~~~"
				cleaned_text = text.rstrip("~")
				print(cleaned_text)
				# Output: "~~~~~Let's keep some tildes"
				```
	- **.zfill()**
		- **.zfill()** method is used to pad a numeric string with zeros to the left, making it a specified `width`.
		- **Syntax:** 
			```python
			.zfill(width)
			```
		- **Parameters:**
			- `width` (required): The total width of the zero-padded string.
		- **Return Value:** The method returns a new string that is zero-padded to the specified `width`.
		- **Return Type:** String
		-  **Examples:**
			1. Example 1:
				```python
				number = "42"
				padded_number = number.zfill(5)
				print(padded_number)
				# Output: "00042"
				```
			2. Example 2:
				```python
				number = "7"
				padded_number = number.zfill(3)
				print(padded_number)
				# Output: "007"
				```
			3. Example 3:
				```python
				number = "1234"
				padded_number = number.zfill(8)
				print(padded_number)
				# Output: "00001234"
				```
- ### Splitting/Joining
	- **.join()**
		- **.join()** method is used to concatenate elements of an iterable (e.g., list, tuple) into a single string, using the string on which it is called as the separator.
		- **Syntax:** 
		```python
		separator_string.join(iterable)
		```
		- **Parameters:**
			- `separator_string` (required): The string used to separate the elements of the iterable when they are concatenated.
			- `iterable` (required): The iterable whose elements will be concatenated into a single string.
		- **Return Value:** The method returns a new string that is the concatenation of the elements in the iterable, separated by the `separator_string`.
		- **Return Type:** String
		- **Examples()**
			1. Example 1:
				```python
				words = ["apple", "banana", "orange"]
				result = ", ".join(words)
				print(result)
				# Output: "apple, banana, orange"
				```
			2. Example 2:
				```python
				characters = ('H', 'e', 'l', 'l', 'o')
				result = ''.join(characters)
				print(result)
				# Output: "Hello"
				```
			3. Example 3:
				```python
				text = "This is a sample text"
				separator = " | "
				result = separator.join(text.split())
				print(result)
				# Output: "This | is | a | sample | text"
				```
	- **.partition()**
		- **.partition()** method splits a string into three parts based on the first occurrence of a specified `separator`. The resulting three parts include the part before the separator, the separator itself, and the part after the separator.
		- **Syntax:** 
			```python
			.partition(separator)
			```
		- **Parameters:**
			- `separator` (required): The substring used to split the string into three parts.
		- **Return Value:** The method returns a tuple containing three elements: the part before the separator, the separator itself, and the part after the separator.
		- **Return Type:** Tuple
		- **Examples()**
			1. Example 1:
				```python
				text = "Python is fun"
				separator = "is"
				result = text.partition(separator)
				print(result)
				# Output: ('Python ', 'is', ' fun')
				```
			2. Example 2:
				```python
				text = "Hello, World!"
				separator = "z"
				result = text.partition(separator)
				print(result)
				# Output: ('Hello, World!', '', '')
				```
			3. Example 3:
				```python
				text = "apple|banana|orange"
				separator = "|"
				result = text.partition(separator)
				print(result)
				# Output: ('apple', '|', 'banana|orange')
				```
	- **.rpartition()**
		- **.rpartition()** method works similarly to `.partition()`, but it searches for the last occurrence of the specified `separator` in the string.
		- **Syntax:** 
			```python
			.rpartition(separator)
			```
		- **Parameters:**
			- `separator` (required): The substring used to split the string into three parts.
		- **Return Value:** The method returns a tuple containing three elements: the part before the last occurrence of the separator, the separator itself, and the part after the separator.
		- **Return Type:** Tuple
		- **Examples()**
			1. Example 1:
				```python
				text = "Python is fun"
				separator = "is"
				result = text.rpartition(separator)
				print(result)
				# Output: ('Python ', 'is', ' fun')
				```
			2. Example 2:
				```python
				text = "Hello, World!"
				separator = "z"
				result = text.rpartition(separator)
				print(result)
				# Output: ('', '', 'Hello, World!')
				```
			3. Example 3:
				```python
				text = "apple|banana|orange"
				separator = "|"
				result = text.rpartition(separator)
				print(result)
				# Output: ('apple|banana', '|', 'orange')
				```
	- **.rsplit()**
		- **.rsplit()** method is used to split a string into a list of substrings, starting from the right, based on the specified `separator`. The `maxsplit` parameter limits the number of splits made.
		- **Syntax:** 
			```python
			.rsplit(separator, maxsplit)
			```
		- **Parameters:**
			- `separator` (optional): The substring used to split the string. If not specified, the string is split on whitespace characters.
			- `maxsplit` (optional): The maximum number of splits to make. If not specified, there is no limit on the number of splits.
		- **Return Value:** The method returns a list of substrings resulting from the split.
		- **Return Type:** List
		- **Examples()**
			1. Example 1:
				```python
				text = "apple banana orange"
				result = text.rsplit()
				print(result)
				# Output: ['apple', 'banana', 'orange']
				```
			2. Example 2:
				```python
				text = "apple,banana,orange"
				result = text.rsplit(',')
				print(result)
				# Output: ['apple', 'banana', 'orange']
				```
			3. Example 3:
				```python
				text = "one,two,three,four,five"
				result = text.rsplit(',', 2)
				print(result)
				# Output: ['one,two,three', 'four', 'five']
				```
	- **.split()**
		- **.split()** method works similarly to `.rsplit()`, but it splits the string starting from the left.
		- **Syntax:** 
		```python
		.split(separator, maxsplit)
		```
		- **Parameters:**
			- `separator` (optional): The substring used to split the string. If not specified, the string is split on whitespace characters.
			- `maxsplit` (optional): The maximum number of splits to make. If not specified, there is no limit on the number of splits.
		- **Return Value:** The method returns a list of substrings resulting from the split.
		- **Return Type:** List
		- **Examples()**
			1. Example 1:
				```python
				text = "apple banana orange"
				result = text.split()
				print(result)
				# Output: ['apple', 'banana', 'orange']
				```
			2. Example 2:
				```python
				text = "apple,banana,orange"
				result = text.split(',')
				print(result)
				# Output: ['apple', 'banana', 'orange']
				```
			3. Example 3:
				```python
				text = "one,two,three,four,five"
				result = text.split(',', 2)
				print(result)
				# Output: ['one', 'two', 'three,four,five']
				```
	- **.splitlines()**
		- **.splitlines()** method is used to split a multi-line string into a list of lines, with an option to keep the line-ending characters (`\n`, `\r`, `\r\n`) at the end of each line.
		- **Syntax:** 
			```python
			.splitlines(keepends)
			```
		- **Parameters:**
			- `keepends` (optional): If set to `True`, the line-ending characters are kept at the end of each line. If set to `False` (default), the line-ending characters are not included in the result.
		- **Return Value:** The method returns a list of lines resulting from the split.
		- **Return Type:** List
		- **Examples()**
			1. Example 1:
				```python
				text = "Hello\nWorld\nExample"
				lines = text.splitlines()
				print(lines)
				# Output: ['Hello', 'World', 'Example']
				```
			2. Example 2:
				```python
				text = "Line 1\rLine 2\r\nLine 3\nLine 4"
				lines = text.splitlines()
				print(lines)
				# Output: ['Line 1', 'Line 2', 'Line 3', 'Line 4']
				```
			3. Example 3:
				```python
				text = "Line 1\n\nLine 2\nLine 3\n"
				lines = text.splitlines(True)
				print(lines)
				# Output: ['Line 1\n', '\n', 'Line 2', 'Line 3', '']
				```
- ### Other
	- **.encode()**
		- encode() method is used to encode a string using the specified encoding. It returns a bytes object representing the encoded version of the original string.
		- **Syntax**
	        ```python
	        .encode(encoding="utf-8", errors="strict")
	        ```
		- **Parameters**
			- `encoding` (optional): The encoding to use for encoding the string. Default is 'utf-8'.
			- `errors` (optional): How to handle encoding errors. Default is 'strict'.
		- **Return Value:** A bytes object containing the encoded version of the original string.
		- **Return Type:** ​Bytes
		- **Examples**
			1. Encode to UTF-8 (default):
				```python
	            text = "Hello, World!"
	            encoded_text = text.encode()
	            print(encoded_text)
	            # b'Hello, World!'
	            ```
			2. Encode Unicode to UTF-8:
				```python
				text = "こんにちは"
				encoded_text = text.encode("utf-8")
				print(encoded_text)
				# b'\xe3\x81\x93\xe3\x82\x93\xe3\x81\xab\xe3\x81\xa1\xe3\x81\xaf'
				```
			3. Encode to UTF-16:
				```python
				text = "Python 101"
				encoded_text = text.encode("utf-16")
				print(encoded_text)
				# b'\xff\xfeP\x00y\x00t\x00h\x00o\x00n\x00 \x001\x000\x001\x00'
				```
	- **.maketrans()**
		- **.maketrans()** method returns a translation table that maps each character in the given strings to its corresponding character in the translation. This table can be used with the translate() method to replace specified characters in a string.
		- **Syntax**
			```python
			.maketrans(x[, y[, z]])
			```
		- **Parameters**
			- x: Mapping of characters to replace. Can be a dictionary or string.
			- y: (Optional) String of characters to replace x with.
			- z: (Optional) String of characters to delete.
		- **Return Value:** Returns a translation table that maps characters from x to y and deletes z. This table can be used with translate() to perform the actual replacement.
		- **Return Type:** Dict
		- **Examples**
			1. Swap a and b:
				```python
				tbl = .maketrans('ab', 'ba')
				print('acb'.translate(tbl))
				# bca
				```
			2. Map vowels to numbers:
				```python
				tbl = .maketrans('aeiou', '12345')
				print('apple'.translate(tbl))
				# 1ppl2
				```
			3. Delete punctuation:
				```python
				tbl = .maketrans('', '', '.?!,')
				print('Text with punctuation.'.translate(tbl))
				# Text with punctuation
				```
	- **.translate()**
		- **.translate()** method returns a string where some characters are mapped to other characters based on a translation table.
		- **Syntax**
			```python
			.translate(table)
			```
		- **Parameters**
			- `table` (required): The translation table mapping characters to replace created by maketrans() or str.maketrans().
		- **Return Value:** A string with characters replaced according to the translation table.
		- **Return Type:** str
		- **Examples**
			1. Swap a and b:
				```python
				tbl = str.maketrans('ab', 'ba')
				print('acb'.translate(tbl))
				# bca
				```
			2. Map vowels to numbers:
				```python
				tbl = str.maketrans('aeiou', '12345')
				print('apple'.translate(tbl))
				# 1ppl2  
				```
			3. Delete punctuation:
				```python
				tbl = str.maketrans('', '', '.?!,')
				print('Text with punctuation.'.translate(tbl))
				# Text with punctuation
				```
	- **.encode()**
		- The `.encode()` method is used to encode a string using the specified encoding. It returns a bytes object representing the encoded version of the original string.
		- **Syntax**
			```python
			.encode(encoding="utf-8", errors="strict")
			```
		- **Parameters**
			- `encoding` (optional): The encoding to use for encoding the string. Default is 'utf-8'.
			- `errors` (optional): How to handle encoding errors. Default is 'strict'.
		- **Return Value:** A bytes object containing the encoded version of the original string.
		- **Return Type:** Bytes
		- **Examples**
			1. Encode to UTF-8 (default):
				```python
				text = "Hello, World!"
				encoded_text = text.encode()
				print(encoded_text)
				# b'Hello, World!'
				```
			2. Encode Unicode to UTF-8:
				```python
				text = "こんにちは"
				encoded_text = text.encode("utf-8")
				print(encoded_text)
				# b'\xe3\x81\x93\xe3\x82\x93\xe3\x81\xab\xe3\x81\xa1\xe3\x81\xaf'
				```
			3. Encode to UTF-16:
				```python
				text = "Python 101"
				encoded_text = text.encode("utf-16")
				print(encoded_text)
				# b'\xff\xfeP\x00y\x00t\x00h\x00o\x00n\x00 \x001\x000\x001\x00'
				```
