---
{"dg-publish":true,"permalink":"/python/python-reference/list-methods/"}
---

- ### Adding elements
	- **.append()**
		- **.append()** method is a list method in Python used to add an element to the end of an existing list.
		- **Syntax:**
	        ```python
	        list.append(element)
	        ```
		- **Parameters:**
			- `element` (required): The element to be added at the end of the list.
		- **Return Value:** This method doesn't return anything. It modifies the original list by adding the specified element to its end.
		- **Examples:**
			1. Adding an element to the end of a list:
	            ```python
	            numbers = [1, 2, 3, 4]
	            numbers.append(5)
	            print(numbers)
	            # Output: [1, 2, 3, 4, 5]
	            ```
	
			2. Appending a string to a list:
	            ```python
	            fruits = ["apple", "banana", "orange"]
	            fruits.append("grape")
	            print(fruits)
	            # Output: ['apple', 'banana', 'orange', 'grape']
	            ```
	
			3. Using .append() with an empty list:
	            ```python
	            empty_list = []
	            empty_list.append(10)
	            empty_list.append(20)
	            print(empty_list)
	            # Output: [10, 20]
	            ```
	- **.extend()**
		- **.extend()** method is a list method in Python used to add multiple elements from an iterable (e.g., list, tuple, string) to the end of an existing list.
		- **Syntax:**
			```python
			list.extend(iterable)
			```
		- **Parameters:**
			- `iterable` (required): An iterable containing elements to be added to the list.
		- **Return Value:** This method doesn't return anything. It modifies the original list by adding the elements from the iterable to its end.
		- **Examples:**
			1. Extending a list with another list:
				```python
				numbers = [1, 2, 3]
				additional_numbers = [4, 5, 6]
				numbers.extend(additional_numbers)
				print(numbers)
				# Output: [1, 2, 3, 4, 5, 6]
				```
			2. Extending a list with a tuple:
				```python
				fruits = ["apple", "banana"]
				additional_fruits = ("orange", "grape")
				fruits.extend(additional_fruits)
				print(fruits)
				# Output: ['apple', 'banana', 'orange', 'grape']
				```
			3. Extending a list with a string:
				```python
				my_list = [1, 2, 3]
				my_string = "hello"
				my_list.extend(my_string)
				print(my_list)
				# Output: [1, 2, 3, 'h', 'e', 'l', 'l', 'o']
				```
	- **.insert()**
		- **.insert()** method is a list method in Python used to insert an element at a specified index in an existing list.
		- **Syntax:**
			```python
			list.insert(index, element)
			```
		- **Parameters:**
			- `index` (required): The index at which the `element` will be inserted.
			- `element` (required): The element to be inserted into the list.
		- **Return Value:** This method doesn't return anything. It modifies the original list by inserting the specified `element` at the given `index`.
		- **Examples:**
			1. Inserting an element at the beginning of a list:
				```python
				numbers = [2, 3, 4]
				numbers.insert(0, 1)
				print(numbers)
				# Output: [1, 2, 3, 4]
				```
			2. Inserting an element in the middle of a list:
				```python
				letters = ['a', 'b', 'd']
				letters.insert(2, 'c')
				print(letters)
				# Output: ['a', 'b', 'c', 'd']
				```
			3. Inserting an element at the end of a list:
				```python
				fruits = ['apple', 'banana']
				fruits.insert(len(fruits), 'orange')
				print(fruits)
				# Output: ['apple', 'banana', 'orange']
				```
- ### Removing elements
	- **.clear()**
		- **.clear()** method is a list method in Python used to remove all elements from an existing list, effectively emptying the list.
		- **Syntax:**
	        ```python
	        list.clear()
	        ```
		- **Parameters:** This method does not take any parameters.
		- **Return Value:** This method does not return anything. It modifies the original list by removing all its elements.
		- **Examples:**
			1. Clearing all elements from a list:
	            ```python
	            numbers = [1, 2, 3, 4, 5]
	            numbers.clear()
	            print(numbers)
	            # Output: []
	            ```
			2. Clearing an empty list has no effect:
	            ```python
	            empty_list = []
	            empty_list.clear()
	            print(empty_list)
	            # Output: []
	            ```
			3. Clearing a list with mixed data types:
	            ```python
	            mixed_list = [1, 'hello', True, 3.14]
	            mixed_list.clear()
	            print(mixed_list)
	            # Output: []
	            ```
	- **.pop()**
		- The `.pop()` method is a list method in Python used to remove and return an element from a specific index in an existing list.
		- **Syntax:**
	        ```python
	        list.pop(index=-1)
	        ```
		- **Parameters:**
			- `index` (optional): The index from which the element will be removed and returned. If not provided, the last element is removed by default (index -1).
		- **Return Value:** The method returns the element that was removed from the list.
		- **Examples:**
			1. Removing and returning an element from the end of a list (default behavior):
	            ```python
	            numbers = [1, 2, 3, 4, 5]
	            popped_element = numbers.pop()
	            print(popped_element)
	            # Output: 5
	            print(numbers)
	            # Output: [1, 2, 3, 4]
	            ```
			2. Removing and returning an element from a specific index (index = 2):
	            ```python
	            letters = ['a', 'b', 'c', 'd']
	            popped_element = letters.pop(2)
	            print(popped_element)
	            # Output: 'c'
	            print(letters)
	            # Output: ['a', 'b', 'd']
	            ```
			3. Removing and returning the first element from the beginning of the list (index = 0):
	            ```python
	            fruits = ['apple', 'banana', 'orange']
	            popped_element = fruits.pop(0)
	            print(popped_element)
	            # Output: 'apple'
	            print(fruits)
	            # Output: ['banana', 'orange']
	            ```
	- **.remove()**
		- **.remove()** method is a list method in Python used to remove the first occurrence of a specified element from an existing list.
		- **Syntax:**
			```python
			list.remove(element)
			```
		- **Parameters:**
			- `element` (required): The element to be removed from the list.
		- **Return Value:** This method does not return anything. It modifies the original list by removing the specified element.
		- **Examples:**
			1. Removing an element from a list:
				```python
				numbers = [1, 2, 3, 4, 3, 5]
				numbers.remove(3)
				print(numbers)
				# Output: [1, 2, 4, 3, 5]
				```
			2. Attempting to remove an element not present in the list raises a ValueError:
				```python
				fruits = ['apple', 'banana', 'orange']
				fruits.remove('grape')
				# Output: ValueError: list.remove(x): x not in list
				```
			3. Removing a string element:
				```python
				words = ['apple', 'banana', 'cherry']
				words.remove('banana')
				print(words)
				# Output: ['apple', 'cherry']
				```
- ### Searching & Counting
	- **.count()**
		- The `.count()` method is a list method in Python used to count the occurrences of a specific element within a list.
		- **Syntax:**
			```python
			.count(element)
			```
		- **Parameters:**
			- `element` (required): The element whose occurrences you want to count within the list.
		- **Return Value:** The method returns the number of occurrences of the specified `element` within the list.
		- **Examples:**
			1. Counting the occurrences of an element in a list:
				```python
				numbers = [1, 2, 2, 3, 4, 2, 5, 2]
				element_to_count = 2
				count = numbers.count(element_to_count)
				print(count)
				# Output: 4
				```
			2. Counting the occurrences of a string element in a list:
				```python
				words = ['apple', 'banana', 'apple', 'orange', 'apple']
				element_to_count = 'apple'
				count = words.count(element_to_count)
				print(count)
				# Output: 3
				```
			3. Counting the occurrences of a specific element in a sublist:
				```python
				data = [[1, 2], [3, 4], [1, 2], [5, 6], [1, 2]]
				sublist_to_count = [1, 2]
				count = data.count(sublist_to_count)
				print(count)
				# Output: 3
				```
	- **.index()**
		- The `.index()` method is a list method in Python used to find the index of the first occurrence of a specified element within a list. Raises value error if the element is not found in the list.
		- **Syntax:**
			```python
			.index(element, start, end)
			```
		- **Parameters:**
			- `element` (required): The element whose index you want to find within the list.
			- `start` (optional): The starting index for the search. If provided, the method will search for the element only after this index. If not specified, the search starts from the beginning of the list.
			- `end` (optional): The ending index for the search. If provided, the method will search for the element only up to this index (exclusive). If not specified, the search continues until the end of the list.
		- **Return Value:** The method returns the index of the first occurrence of the specified `element` within the list.
		- **Examples:**
			1. Finding the index of an element in a list:
				```python
				numbers = [1, 2, 3, 4, 2, 5]
				element_to_find = 2
				index = numbers.index(element_to_find)
				print(index)
				# Output: 1
				```
			2. Finding the index of an element after a specific index:
				```python
				numbers = [1, 2, 3, 4, 2, 5]
				element_to_find = 2
				start_index = 2
				index = numbers.index(element_to_find, start_index)
				print(index)
				# Output: 4
				```
			3. Finding the index of an element within a specific range:
				```python
				numbers = [1, 2, 3, 4, 2, 5]
				element_to_find = 2
				start_index = 0
				end_index = 4
				index = numbers.index(element_to_find, start_index, end_index)
				print(index)
				# Output: 1
				```
- ### Others
	- **.reverse()**
		- The `.reverse()` method is a list method in Python used to reverse the order of elements in an existing list. It modifies the original list in place, and no new list is created.
		- **Syntax:**
			```python
			list.reverse()
			```
		- **Parameters:** 
			- This method does not take any parameters.
		- **Return Value:** 
			- This method does not return anything. It modifies the original list by reversing the order of its elements.
		- **Description:** 
			- The `.reverse()` method changes the order of elements in the list, reversing the order of the elements so that the last element becomes the first, the second-to-last element becomes the second, and so on. The first element in the original list becomes the last element after the reversal.
			- The method does not create a new list but modifies the list in place. Therefore, be cautious while using this method, as it will alter the original list and any references to that list.
		- **Examples:**
			1. Reversing a list of numbers:
				```python
				numbers = [1, 2, 3, 4, 5]
				numbers.reverse()
				print(numbers)
				# Output: [5, 4, 3, 2, 1]
				```
			2. Reversing a list of strings:
				```python
				words = ['apple', 'banana', 'cherry']
				words.reverse()
				print(words)
				# Output: ['cherry', 'banana', 'apple']
				```
			3. Reversing a list with mixed data types:
				```python
				mixed_list = [1, 'apple', 3.14, True, 'orange']
				mixed_list.reverse()
				print(mixed_list)
				# Output: ['orange', True, 3.14, 'apple', 1]
				```
	- **.sort()**
		- The `.sort()` method is a list method in Python used to sort the elements of a list in ascending order. It modifies the original list in place.
		- **Syntax:**
			```python
			.sort(key, reverse)
			```
		- **Parameters:** 
			- `key` (optional): A function that specifies how the elements should be compared during sorting. If not provided, the elements are compared directly.
			- `reverse` (optional): A boolean value that indicates whether to sort the list in descending order (`True`) or ascending order (`False`, default).
		- **Return Value:** 
			- This method does not return anything. It modifies the original list by sorting its elements.
		- **Description:** 
			- The `.sort()` method arranges the elements of the list in ascending order. The elements are sorted based on their values, and the original order is changed in the process.
			- If the `key` parameter is provided, the elements are sorted based on the result of applying the `key` function to each element before comparison.
			- If the `reverse` parameter is set to `True`, the list will be sorted in descending order; otherwise, it will be sorted in ascending order (default).
			- The method modifies the original list directly and does not create a new list, so use it with caution as it will alter any references to that list.
		- **Examples:**
			1. Sorting a list of numbers in ascending order:
				```python
				numbers = [5, 2, 8, 1, 3]
				numbers.sort()
				print(numbers)
				# Output: [1, 2, 3, 5, 8]
				```
			2. Sorting a list of strings in ascending order:
				```python
				words = ['apple', 'banana', 'cherry', 'orange']
				words.sort()
				print(words)
				# Output: ['apple', 'banana', 'cherry', 'orange']
				```
			3. Sorting a list of tuples based on a custom key function:
				```python
				def get_second_element(item):
				return item[1]
				data = [(1, 5), (2, 2), (3, 8), (4, 1)]
				data.sort(key=get_second_element)
				print(data)
				# Output: [(4, 1), (2, 2), (1, 5), (3, 8)]
				```
