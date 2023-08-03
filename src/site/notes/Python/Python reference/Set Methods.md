---
{"dg-publish":true,"permalink":"/python/python-reference/set-methods/"}
---

- ### Element operation
	- **.add()**
		- The `.add()` method is a set method in Python used to insert a single element into a set. If the element is already present in the set, calling `.add()` with that element has no effect, and the set remains unchanged.
		- **Syntax:**
			```python
			set.add(element)
			```
		- **Parameters:** 
			- `element`: The element to be added to the set.
		- **Return Value:** 
			- This method does not return anything. It modifies the set in place by adding the specified `element` to it.
		- **Description:** 
			- The `.add()` method is used to insert a single element into a set.
			- If the `element` is not already present in the set, it will be added to the set. Otherwise, if the `element` is already present, calling `.add()` has no effect, and the set remains unchanged.
			- Unlike other set methods that accept iterables, `.add()` specifically takes a single element as an argument.
		- **Examples:**
			1. Adding an element to a set:
				```python
				numbers = {1, 2, 3}
				numbers.add(4)
				print(numbers)
				# Output: {1, 2, 3, 4}
				```
			2. Adding an existing element has no effect:
				```python
				colors = {'red', 'green', 'blue'}
				colors.add('green')
				print(colors)
				# Output: {'red', 'green', 'blue'}
				```
			3. Adding a new element to an empty set:
				```python
				empty_set = set()
				empty_set.add('hello')
				print(empty_set)
				# Output: {'hello'}
				```
	- **.remove()**
		- The `remove()` method is a set method in Python used to remove a specific element from a set. If the element is not present in the set, it raises a `KeyError`.
		- **Syntax:**
			```python
			set.remove(element)
			```
		- **Parameters:** 
			- `element`: The element to be removed from the set.
		- **Return Value:** 
			- This method does not return anything; it modifies the set by removing the specified element.
		- **Description:** 
			- The `remove()` method removes a given element from a set if it exists. If the element is not found in the set, it raises a `KeyError`.
			- Since sets are unordered collections of unique elements, the `remove()` method is used to specifically target and delete a particular element within the set.
			- If the element is successfully removed, the set will contain one less element. If the element is not present in the set, attempting to remove it will raise an error.
		- **Examples:**
			1. Removing an element from a set:
				```python
				my_set = {1, 2, 3, 4, 5}
				my_set.remove(3)
				print(my_set)
				# Output: {1, 2, 4, 5}
				```
			2. Trying to remove a non-existing element (raises `KeyError`):
				```python
				my_set = {1, 2, 4, 5}
				my_set.remove(3)  # Raises KeyError: 3
				```
			3. Removing an element that exists multiple times (only one occurrence is removed):
				```python
				my_set = {1, 2, 2, 3, 4}
				my_set.remove(2)
				print(my_set)
				# Output: {1, 3, 4}
				```
	- **.discard()**
		- The `discard()` method is a set method in Python used to remove a specific element from a set. If the element is not present in the set, calling `discard()` with that element has no effect, and the set remains unchanged.
		- **Syntax:**
			```python
			set.discard(element)
			```
		- **Parameters:** 
			- `element`: The element to be removed from the set.
		- **Return Value:** 
			- This method does not return anything; it modifies the set by removing the specified element if it exists.
		- **Description:** 
			- The `discard()` method removes a given element from a set if it exists. If the element is not found in the set, calling `discard()` has no effect, and the set remains unchanged.
			- Unlike the `remove()` method, `discard()` does not raise any error if the element is not present in the set. It silently ignores the operation and leaves the set unchanged.
			- The primary advantage of using `discard()` over `remove()` is that it avoids raising an error when attempting to remove a non-existing element, making it safer to use.
		- **Examples:**
			1. Removing an element from a set using `discard()`:
				```python
				my_set = {1, 2, 3, 4, 5}
				my_set.discard(3)
				print(my_set)
				# Output: {1, 2, 4, 5}
				```
			2. Trying to discard a non-existing element (no effect):
				```python
				my_set = {1, 2, 4, 5}
				my_set.discard(3)
				print(my_set)
				# Output: {1, 2, 4, 5}
				```
			3. Discarding an element that exists multiple times (only one occurrence is removed):
				```python
				my_set = {1, 2, 2, 3, 4}
				my_set.discard(2)
				print(my_set)
				# Output: {1, 3, 4}
				```
	- **.pop()**
		- The `pop()` method is a set method in Python used to remove and return an arbitrary element from a set. Since sets are unordered collections, the element returned by `pop()` is not guaranteed to be the same across multiple calls.
		- **Syntax:**
			```python
			set.pop()
			```
		- **Parameters:** 
			- This method does not accept any parameters.
		- **Return Value:** 
			- Returns the removed element from the set.
		- **Description:** 
			- The `pop()` method removes and returns an arbitrary element from the set. The removed element is not based on any specific order since sets are unordered.
			- If the set is empty, calling `pop()` raises a `KeyError`.
			- The primary use of `pop()` is to efficiently remove and access a random element from the set.
			- It's important to note that if you need to remove a specific element from the set, you should use the `remove()` or `discard()` method, as `pop()` doesn't allow you to target a specific element.
		- **Examples:**
			1. Removing and returning an arbitrary element from the set:
				```python
				my_set = {1, 2, 3, 4, 5}
				removed_element = my_set.pop()
				print(removed_element)
				print(my_set)
				# Output:
				# (Output may vary as it's an arbitrary element)
				# e.g., 1 (element removed)
				# {2, 3, 4, 5} (set after removal)
				```
			2. Removing and returning an arbitrary element from an empty set (raises `KeyError`):
				```python
				empty_set = set()
				removed_element = empty_set.pop()
				# Raises KeyError: 'pop from an empty set'
				```
			3. Using `pop()` in a loop to remove elements from a set until it's empty:
				```python
				my_set = {1, 2, 3, 4, 5}
				while my_set:
				    removed_element = my_set.pop()
				    print(f"Removed: {removed_element}, Remaining: {my_set}")
				# Output:
				# Removed: 1, Remaining: {2, 3, 4, 5}
				# Removed: 2, Remaining: {3, 4, 5}
				# Removed: 3, Remaining: {4, 5}
				# Removed: 4, Remaining: {5}
				# Removed: 5, Remaining: set()
				```
- ### Membership testing
	- **.issubset()**
		- The `issubset()` method is a set method in Python used to check whether a set is a subset of another set.
		- **Syntax:**
			```python
			set.issubset(other_set)
			```
		- **Operator:**
			- Alternatively, you can use the `<=` operator to check for subset membership.
			```python
			set <= other_set
			```
		- **Proper Subset Operator:**
			- A proper subset is a subset that is not equal to the original set. It means all elements of the subset are present in the original set, but the original set may have additional elements.
			- A set can be subset of itself but it can't be proper subset of itself
			- You can use the `<` operator to check if a set is a proper subset of another. It returns `True` if the set is a proper subset, otherwise `False`. 
			```python
			set < other_set
			```
		- **Parameters:** 
			- `other_set`: The set to compare against for subset membership.
		- **Return Value:** 
			- Returns `True` if the set is a subset (not equal) of `other_set`, otherwise `False`.
		- **Description:** 
			- The `issubset()` method checks whether all elements of the current set are present in the `other_set`.
			- If all elements of the set are also present in the `other_set`, it is considered a subset, and the method returns `True`.
			- If any elements of the set are not found in the `other_set`, it is not a subset, and the method returns `False`.
			- An empty set is always considered a subset of any set since it has no elements.
			- The `issubset()` method is useful to compare the membership of sets and to know if one set is a proper subset of another (i.e., it is not equal to the other set).
			- A set cannot be a proper subset of itself.
		- **Examples:**
			1. Checking if one set is a subset of another:
				```python
				set1 = {1, 2, 3}
				set2 = {1, 2, 3, 4, 5}
				
				result = set1.issubset(set2)
				print(result)
				# Output: True
				```
				```python
				# Using the <= operator
				result_operator = set1 <= set2
				print(result_operator)
				# Output: True
				```
			2. Using `issubset()` with an empty set:
				```python
				empty_set = set()
				other_set = {1, 2, 3}
				
				result = empty_set.issubset(other_set)
				print(result)
				# Output: True (empty set is a subset of any set)
				```
				```python
				# Using the <= operator with an empty set
				result_operator = empty_set <= other_set
				print(result_operator)
				# Output: True
				```
			3. Checking if one set is not a subset of another:
				```python
				set1 = {1, 2, 3}
				set2 = {4, 5, 6}
				
				result = set1.issubset(set2)
				print(result)
				# Output: False (set1 is not a subset of set2)
				```
				```python
				# Using the <= operator
				result_operator = set1 <= set2
				print(result_operator)
				# Output: False
				```
			4. Checking if one set is a proper subset of another:
				```python
				set3 = {1, 2}
				set4 = {1, 2, 3}
				
				result_proper = set3 < set4
				print(result_proper)
				# Output: True (set3 is a proper subset of set4)
				```
				```python
				# Using the < operator
				result_operator_proper = set3 < set4
				print(result_operator_proper)
				# Output: True
				```
	- **.issuperset()**
		- The `issuperset()` method is a set method in Python used to check whether a set is a superset of another set.
		- **Syntax:**
			```python
			set.issuperset(other_set)
			```
		- **Operator:**
			- Alternatively, you can use the `>=` operator to check for superset membership.
			```python
			set >= other_set
			```
		- **Proper Superset and Operator:**
			- A proper superset is a superset that is not equal to the original set. It means the original set contains all elements of the other set, but the proper superset may have additional elements that are not present in the original set.
			- You can use the `>` operator to check if a set is a proper superset of another. It returns `True` if the set is a proper superset, otherwise `False`.
			```python
			set > other_set
			```
		- **Parameters:** 
			- `other_set`: The set to compare against for superset membership.
		- **Return Value:** 
			- Returns `True` if the set is a superset of `other_set`, otherwise `False`.
		- **Description:** 
			- The `issuperset()` method checks whether all elements of the `other_set` are present in the current set.
			- If all elements of the `other_set` are also present in the current set, it is considered a superset, and the method returns `True`.
			- If any elements of the `other_set` are not found in the current set, it is not a superset, and the method returns `False`.
			- An empty set is always considered a superset of any set since it has no elements.
			- The `issuperset()` method is useful to compare the membership of sets and to know if one set is a superset of another (i.e., it contains all elements of the other set).
		- **Examples:**
			1. Checking if one set is a superset of another:
				```python
				set1 = {1, 2, 3, 4, 5}
				set2 = {1, 2, 3}
				
				result = set1.issuperset(set2)
				print(result)
				# Output: True (set1 is a superset of set2)
				```
				```python
				# Using the >= operator
				result_operator = set1 >= set2
				print(result_operator)
				# Output: True
				```
			2. Using `issuperset()` with an empty set:
				```python
				empty_set = set()
				other_set = {1, 2, 3}
				
				result = empty_set.issuperset(other_set)
				print(result)
				# Output: False (empty set is not a superset of any non-empty set)
				```
				```python
				# Using the >= operator with an empty set
				result_operator = empty_set >= other_set
				print(result_operator)
				# Output: False
				```
			3. Checking if one set is not a superset of another:
				```python
				set1 = {1, 2, 3}
				set2 = {4, 5, 6}
				
				result = set1.issuperset(set2)
				print(result)
				# Output: False (set1 is not a superset of set2)
				```
				```python
				# Using the >= operator
				result_operator = set1 >= set2
				print(result_operator)
				# Output: False
				```
			4. Checking if one set is a proper superset of another:
				```python
				set3 = {1, 2, 3, 4}
				set4 = {1, 2, 3}
				
				result_proper = set3 > set4
				print(result_proper)
				# Output: True (set3 is a proper superset of set4)
				```
				```python
				# Using the > operator
				result_operator_proper = set3 > set4
				print(result_operator_proper)
				# Output: True
				```
	- **.isdisjoint()**
		- The `isdisjoint()` method is a set method in Python used to check whether two sets have no elements in common.
		- **Syntax:**
			```python
			set.isdisjoint(other_set)
			```
		- **Parameters:** 
			- `other_set`: The set to compare against for disjointness.
		- **Return Value:** 
			- Returns `True` if the sets have no elements in common (i.e., they are disjoint), otherwise `False`.
		- **Description:** 
			- The `isdisjoint()` method checks whether two sets have any common elements.
			- If the sets have no elements in common, they are considered disjoint, and the method returns `True`.
			- If the sets have at least one common element, they are not disjoint, and the method returns `False`.
			- An empty set is always disjoint with any other set since it has no elements.
			- The `isdisjoint()` method is useful to determine if there are any shared elements between sets without finding the actual intersection.
		- **Examples:**
			1. Checking if two sets are disjoint:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {5, 6, 7}
				
				result = set1.isdisjoint(set2)
				print(result)
				# Output: True (set1 and set2 are disjoint)
				```
			2. Using `isdisjoint()` with an empty set:
				```python
				empty_set = set()
				other_set = {1, 2, 3}
				
				result = empty_set.isdisjoint(other_set)
				print(result)
				# Output: True (empty set and other_set are disjoint)
				```
			3. Checking if two sets are not disjoint:
				```python
				set1 = {1, 2, 3}
				set2 = {3, 4, 5}
				
				result = set1.isdisjoint(set2)
				print(result)
				# Output: False (set1 and set2 are not disjoint)
				```
- ### Set operation
	- **.union()**
		- The `union()` method is a set method in Python used to combine two or more sets into a new set containing all unique elements from both sets.
		- **Syntax:**
			```python
			set.union(other_set1, other_set2, ...)
			```
		- **Operator:**
			- The union operator `|` can also be used to combine two sets and create a new set containing all unique elements from both sets.
			```python
			result_set = set1 | set2
			```
		- **Parameters:** 
			- `other_set1`, `other_set2`, ...: The sets to be combined with the current set.
		- **Return Value:** 
			- Returns a new set that contains all the unique elements from the original set and all the other sets passed as arguments.
		- **Description:** 
			- The `union()` method creates a new set that contains all the unique elements present in the original set and the other sets provided as arguments.
			- It does not modify the original set; instead, it returns a new set with the combined elements.
			- If there are duplicate elements in the other sets, they will appear only once in the resulting set due to the unique property of sets.
			- The method is useful for combining multiple sets while ensuring that there are no duplicate elements in the result.
		- **Examples:**
			1. Using `union()` to combine two sets:
				```python
				set1 = {1, 2, 3}
				set2 = {3, 4, 5}
				
				result_set = set1.union(set2)
				print(result_set)
				# Output: {1, 2, 3, 4, 5}
				```
				```python
				# Using the | operator to perform union
				result_set_operator = set1 | set2
				print(result_set_operator)
				# Output: {1, 2, 3, 4, 5}
				```
			2. Using `union()` with multiple sets:
				```python
				set1 = {1, 2, 3}
				set2 = {3, 4, 5}
				set3 = {5, 6, 7}
				
				result_set = set1.union(set2, set3)
				print(result_set)
				# Output: {1, 2, 3, 4, 5, 6, 7}
				```
				```python
				# Using the | operator with multiple sets
				result_set_operator = set1 | set2 | set3
				print(result_set_operator)
				# Output: {1, 2, 3, 4, 5, 6, 7}
				```
			3. Using `union()` with an empty set:
				```python
				set1 = {1, 2, 3}
				empty_set = set()
				
				result_set = set1.union(empty_set)
				print(result_set)
				# Output: {1, 2, 3}
				```
				```python
				# Using the | operator with an empty set
				result_set_operator = set1 | empty_set
				print(result_set_operator)
				# Output: {1, 2, 3}
				```
	- **.intersection()**
		- The `intersection()` method is a set method in Python used to find the common elements between two or more sets.
		- **Syntax:**
			```python
			set.intersection(other_set1, other_set2, ...)
			```
		- **Operator:**
			- The intersection operator `&` can also be used to find the common elements between two sets and create a new set containing those elements.
			```python
			result_set = set1 & set2
			```
		- **Parameters:** 
			- `other_set1`, `other_set2`, ...: The sets to find the common elements with the current set.
		- **Return Value:** 
			- Returns a new set that contains the common elements present in both the original set and all the other sets passed as arguments.
		- **Description:** 
			- The `intersection()` method creates a new set that contains the elements common to the original set and all the other sets provided as arguments.
			- It does not modify the original set; instead, it returns a new set with the common elements.
			- If there are no common elements between the sets, the resulting set will be empty.
			- The method is useful for finding the intersection of multiple sets.
		- **Examples:**
			1. Using `intersection()` to find common elements between two sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5}
				
				result_set = set1.intersection(set2)
				print(result_set)
				# Output: {3, 4}
				```
				```python
				# Using the & operator to perform intersection
				result_set_operator = set1 & set2
				print(result_set_operator)
				# Output: {3, 4}
				```
			2. Using `intersection()` with multiple sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5}
				set3 = {4, 5, 6}
				
				result_set = set1.intersection(set2, set3)
				print(result_set)
				# Output: {4}
				```
				```python
				# Using the & operator with multiple sets
				result_set_operator = set1 & set2 & set3
				print(result_set_operator)
				# Output: {4}
				```
			3. Using `intersection()` with an empty set:
				```python
				set1 = {1, 2, 3}
				empty_set = set()
				
				result_set = set1.intersection(empty_set)
				print(result_set)
				# Output: set()
				```
				```python
				# Using the & operator with an empty set
				result_set_operator = set1 & empty_set
				print(result_set_operator)
				# Output: set()
				```
	- **.difference()**
		- The `difference()` method is a set method in Python used to create a new set containing the elements that are present in the current set but not in another set.
		- **Syntax:**
			```python
			set.difference(other_set)
			```
		- **Operator:**
			- The difference operator `-` can also be used to create a new set containing the elements that are present in the current set but not in another set.
			```python
			set1 - set2
			```
		- **Parameters:** 
			- `other_set`: The set to compare against for finding the difference.
		- **Return Value:** 
			- Returns a new set that contains the elements present in the current set but not in `other_set`.
		- **Description:** 
			- The `difference()` method creates a new set that contains the elements present in the current set but not in `other_set`.
			- It does not modify the original sets; instead, it returns a new set with the difference.
			- The method is useful for finding the unique elements that exist in one set but not in another set.
		- **Examples:**
			1. Using `difference()` to find the elements unique to one set:
				```python
				set1 = {1, 2, 3, 4, 5}
				set2 = {3, 4, 5, 6, 7}
				
				result_set = set1.difference(set2)
				print(result_set)
				# Output: {1, 2}
				```
				```python
				# Using the - operator to find the difference
				result_set_operator = set1 - set2
				print(result_set_operator)
				# Output: {1, 2}
				```
			2. Using `difference()` with an empty set:
				```python
				set1 = {1, 2, 3}
				empty_set = set()
				
				result_set = set1.difference(empty_set)
				print(result_set)
				# Output: {1, 2, 3}
				```
				```python
				# Using the - operator with an empty set
				result_set_operator = set1 - empty_set
				print(result_set_operator)
				# Output: {1, 2, 3}
				```
			3. Using `difference()` with multiple sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5}
				set3 = {4, 5, 6}
				
				result_set = set1.difference(set2, set3)
				print(result_set)
				# Output: {1, 2}
				
				# Using the - operator with multiple sets
				result_set_operator = set1 - set2 - set3
				print(result_set_operator)
				# Output: {1, 2}
				```
	- **.symmetric_difference()**
		- The `symmetric_difference()` method is a set method in Python used to find the elements that are unique to each set (not common to both sets) and create a new set containing those elements.
		- **Syntax:**
			```python
			set.symmetric_difference(other_set)
			```
		- **Operator:**
			- The symmetric difference operator `^` can also be used to find the elements that are unique to each set and create a new set containing those elements.
			```python
			result_set = set1 ^ set2
			```
		- **Parameters:** 
			- `other_set`: The set to find the elements that are unique to each set with the current set.
		- **Return Value:** 
			- Returns a new set that contains the elements that are unique to each set (present in one set but not in the other).
		- **Description:** 
			- The `symmetric_difference()` method creates a new set that contains the elements that are unique to each set (not common to both sets).
			- It does not modify the original set; instead, it returns a new set with the unique elements.
			- If there are no unique elements between the sets (i.e., both sets have the same elements), the resulting set will be empty.
			- The method is useful for finding the symmetric difference of two sets.
		- **Examples:**
			1. Using `symmetric_difference()` to find the elements that are unique to each set:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5}
				
				result_set = set1.symmetric_difference(set2)
				print(result_set)
				# Output: {1, 2, 5}
				```
				```python
				# Using the ^ operator to perform symmetric difference
				result_set_operator = set1 ^ set2
				print(result_set_operator)
				# Output: {1, 2, 5}
				```
			2. Using `symmetric_difference()` with an empty set:
				```python
				set1 = {1, 2, 3}
				empty_set = set()
				
				result_set = set1.symmetric_difference(empty_set)
				print(result_set)
				# Output: {1, 2, 3}
				```
				```python
				# Using the ^ operator with an empty set
				result_set_operator = set1 ^ empty_set
				print(result_set_operator)
				# Output: {1, 2, 3}
				```
			3. Using `symmetric_difference()` with multiple sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5}
				set3 = {4, 5, 6}
				
				result_set = set1.symmetric_difference(set2, set3)
				print(result_set)
				# Output: {1, 2, 5, 6}
				
				# Using the ^ operator with multiple sets
				result_set_operator = set1 ^ set2 ^ set3
				print(result_set_operator)
				# Output: {1, 2, 5, 6}
				```
- ### Set operation (in place)
	- **.update()**
		- The `update()` method is a set method in Python used to modify a set by performing the union of sets. It adds elements from another set or iterable to the current set.
		- **Syntax:**
			```python
			set.update(other_set)
			```
		- **Augmented Assignment Operator:**
			- The union operator `|=` can also be used to perform the same operation of updating the set by performing the union.
			```python
			set1 |= other_set
			```
		- **Parameters:** 
			- `other_set`: The set or iterable containing elements to be added to the current set.
		- **Return Value:** 
			- This method does not return anything; it modifies the current set directly.
		- **Description:** 
			- The `update()` method adds elements from `other_set` or iterable to the current set.
			- It modifies the original set by performing the union, adding elements that are not already present in the current set.
			- The method is useful for extending the current set by adding new elements from another set or iterable.
		- **Examples:**
			1. Using `update()` to add elements from another set:
				```python
				set1 = {1, 2, 3}
				set2 = {3, 4, 5}
				
				set1.update(set2)
				print(set1)
				# Output: {1, 2, 3, 4, 5}
				```
				```python
				# Using the |= operator to perform union
				set1 |= set2
				print(set1)
				# Output: {1, 2, 3, 4, 5}
				```
			2. Using `update()` with an iterable (list):
				```python
				set1 = {1, 2, 3}
				new_elements = [3, 4, 5]
				
				set1.update(new_elements)
				print(set1)
				# Output: {1, 2, 3, 4, 5}
				```
				```python
				# Using the |= operator with an iterable (list)
				set1 |= new_elements
				print(set1)
				# Output: {1, 2, 3, 4, 5}
				```
			3. Using `update()` with multiple sets:
				```python
				set1 = {1, 2, 3}
				set2 = {3, 4, 5}
				set3 = {5, 6, 7}
				
				set1.update(set2, set3)
				print(set1)
				# Output: {1, 2, 3, 4, 5, 6, 7}
				
				# Using the |= operator with multiple sets
				set1 |= set2 | set3
				print(set1)
				# Output: {1, 2, 3, 4, 5, 6, 7}
				```
	- **.intersection_update()**
		- The `intersection_update()` method is a set method in Python used to modify a set by updating it with the intersection of sets. It keeps only the elements that are common in both the current set and another set or iterable.
		- **Syntax:**
			```python
			set.intersection_update(other_set)
			```
		- **Augmented Assignment Operator:**
			- The intersection operator `&=` can also be used to perform the same operation of updating the set with the intersection.
			```python
			set1 &= other_set
			```
		- **Parameters:**
			- `other_set`: The set or iterable with which the intersection is computed to update the current set.
		- **Return Value:**
			- This method does not return anything; it modifies the current set directly.
		- **Description:**
			- The `intersection_update()` method modifies the original set by keeping only the elements that are common between the current set and the `other_set`.
			- It updates the set in-place, discarding elements that are not present in both sets.
			- The method is useful for finding the intersection of two or more sets and updating the current set accordingly.
		- **Examples:**
			1. Using `intersection_update()` to find the intersection of two sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5, 6}
				
				set1.intersection_update(set2)
				print(set1)
				# Output: {3, 4}
				```
				```python
				# Using the &= operator to perform intersection
				set1 &= set2
				print(set1)
				# Output: {3, 4}
				```
			2. Using `intersection_update()` with an iterable (list):
				```python
				set1 = {1, 2, 3, 4}
				elements_to_keep = [2, 3, 5]
				
				set1.intersection_update(elements_to_keep)
				print(set1)
				# Output: {2, 3}
				```
				```python
				# Using the &= operator with an iterable (list)
				set1 &= elements_to_keep
				print(set1)
				# Output: {2, 3}
				```
			3. Using `intersection_update()` with multiple sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5, 6}
				set3 = {4, 5, 7}
				
				set1.intersection_update(set2, set3)
				print(set1)
				# Output: {4}
				
				# Using the &= operator with multiple sets
				set1 &= set2 & set3
				print(set1)
				# Output: {4}
				```
	- **.difference_update()**
		- The `difference_update()` method is a set method in Python used to modify a set by updating it with the difference of sets. It removes all elements that are common in both the current set and another set or iterable.
		- **Syntax:**
			```python
			set.difference_update(other_set)
			```
		- **Augmented Assignment Operator:**
			- The difference operator `-=` can also be used to perform the same operation of updating the set with the difference.
			```python
			set1 -= other_set
			```
		- **Parameters:**
			- `other_set`: The set or iterable with which the difference is computed to update the current set.
		- **Return Value:**
			- This method does not return anything; it modifies the current set directly.
		- **Description:**
			- The `difference_update()` method modifies the original set by removing all elements that are common between the current set and the `other_set`.
			- It updates the set in-place, keeping only the elements that are not present in the `other_set`.
			- The method is useful for finding the difference between two sets and updating the current set accordingly.
		- **Examples:**
			1. Using `difference_update()` to find the difference of two sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5, 6}
				
				set1.difference_update(set2)
				print(set1)
				# Output: {1, 2}
				```
				```python
				# Using the -= operator to perform difference
				set1 -= set2
				print(set1)
				# Output: {1, 2}
				```
			2. Using `difference_update()` with an iterable (list):
				```python
				set1 = {1, 2, 3, 4}
				elements_to_remove = [2, 3]
				
				set1.difference_update(elements_to_remove)
				print(set1)
				# Output: {1, 4}
				```
				```python
				# Using the -= operator with an iterable (list)
				set1 -= elements_to_remove
				print(set1)
				# Output: {1, 4}
				```
			3. Using `difference_update()` with multiple sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5, 6}
				set3 = {4, 5, 7}
				
				set1.difference_update(set2, set3)
				print(set1)
				# Output: {1, 2}
				
				# Using the -= operator with multiple sets
				set1 -= set2 | set3
				print(set1)
				# Output: {1, 2}
				```
	- **.symmetric_difference_update()**
		- The `symmetric_difference_update()` method is a set method in Python used to modify a set by updating it with the symmetric difference of sets. It removes elements that are present in both sets and adds elements that are present in only one of the sets.
		- **Syntax:**
			```python
			set.symmetric_difference_update(other_set)
			```
		- **Augmented Assignment Operator:**
			- The symmetric difference assignment operator `^=` can also be used to perform the same operation of updating the set with the symmetric difference.
			```python
			set1 ^= other_set
			```
		- **Parameters:**
			- `other_set`: The set or iterable with which the symmetric difference is computed to update the current set.
		- **Return Value:**
			- This method does not return anything; it modifies the current set directly.
		- **Description:**
			- The `symmetric_difference_update()` method modifies the original set by removing elements that are common in both the current set and the `other_set`, and adding elements that are unique to either set.
			- It updates the set in-place, keeping only the elements that are not shared between the two sets.
			- The method is useful for finding the symmetric difference between two sets and updating the current set accordingly.
		- **Examples:**
			1. Using `symmetric_difference_update()` to find the symmetric difference of two sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5, 6}
				
				set1.symmetric_difference_update(set2)
				print(set1)
				# Output: {1, 2, 5, 6}
				```
				```python
				# Using the ^= operator to perform symmetric difference
				set1 ^= set2
				print(set1)
				# Output: {1, 2, 5, 6}
				```
			2. Using `symmetric_difference_update()` with an iterable (list):
				```python
				set1 = {1, 2, 3, 4}
				elements_to_add = [3, 4, 5]
				
				set1.symmetric_difference_update(elements_to_add)
				print(set1)
				# Output: {1, 2, 5}
				```
				```python
				# Using the ^= operator with an iterable (list)
				set1 ^= set(elements_to_add)
				print(set1)
				# Output: {1, 2, 5}
				```
			3. Using `symmetric_difference_update()` with multiple sets:
				```python
				set1 = {1, 2, 3, 4}
				set2 = {3, 4, 5, 6}
				set3 = {4, 5, 7}
				
				set1.symmetric_difference_update(set2, set3)
				print(set1)
				# Output: {1, 2, 6}
				
				# Using the ^= operator with multiple sets
				set1 ^= set2 ^ set3
				print(set1)
				# Output: {1, 2, 6}
				```
- ### Copy
	- **.copy()**
		- The `copy()` method is a set method in Python used to create a shallow copy of a set.
		- **Syntax:**
			```python
			set.copy()
			```
		- **Parameters:**
			- This method does not accept any parameters.
		- **Return Value:**
			- Returns a new set that is a shallow copy of the original set.
		- **Description:**
			- The `copy()` method creates a new set that contains all the elements of the original set.
			- The copy is shallow, which means it creates a new set but does not duplicate the elements inside the set. Both the original set and the copied set share the same elements, so changes made to one set will not affect the other.
			- Shallow copying is useful when you want to create a new set with the same elements as an existing set, but you don't want them to be the same object in memory.
		- **Examples:**
			1. Creating a shallow copy of a set:
				```python
				set1 = {1, 2, 3}
				set2 = set1.copy()
				
				print(set1)
				# Output: {1, 2, 3}
				
				print(set2)
				# Output: {1, 2, 3}
				
				# The two sets are different objects in memory
				print(set1 is set2)
				# Output: False
				```
			2. Modifying the original set after copying:
				```python
				set1 = {1, 2, 3}
				set2 = set1.copy()
				
				set1.add(4)
				print(set1)
				# Output: {1, 2, 3, 4}
				
				print(set2)
				# Output: {1, 2, 3} (set2 remains unchanged)
				```
			3. Creating a copy of an empty set:
				```python
				empty_set = set()
				copied_set = empty_set.copy()
				
				print(empty_set)
				# Output: set()
				
				print(copied_set)
				# Output: set()
				```
