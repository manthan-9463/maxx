# 1) What are the types of Applications?
=>
-Web Development: Building websites and web applications (e.g., Django, Flask).
-Data Science & Analytics: Data processing, analysis, and visualization (e.g., Pandas, NumPy, Matplotlib).
-Machine Learning & AI: Building models for predictions and AI (e.g., TensorFlow, PyTorch, scikit-learn).
-Scripting & Automation: Automating repetitive tasks (e.g., file handling, web scraping with BeautifulSoup).
-Game Development: Creating 2D and simple games (e.g., Pygame).
-Desktop GUI Applications: Building desktop apps (e.g., Tkinter, PyQt).
-Networking: Developing network applications and handling protocols (e.g., socket programming).
-Embedded Systems & IoT: Programming for small devices (e.g., MicroPython on microcontrollers).
-Scientific & Numeric Computing: Complex calculations and simulations (e.g., SciPy).
-Cybersecurity: Writing scripts for penetration testing and security analysis (e.g., Scapy).


# 2) What is programing?
=>
-Programming is the process of writing instructions (called code) for computers to execute. It involves creating sequences of commands and logic to solve problems, automate tasks, or create applications. Through programming, developers use languages like Python, Java, or C++ to build software, websites, games, and other digital systems.

# 3) What is Python?
=>
-Python is a popular programming language. It was created by Guido van Rossum, and released in 1991.

It is used for:

web development (server-side),
software development,
mathematics,
system scripting.

.. code:: ipython3

    # 4)  Write a Python program to check if a number is positive, negative or zero.
    
    # for user to enter number
    number = float(input("Enter a number: "))
    
    # condition to check number
    if number > 0:
        print("The number is positive.")
    elif number < 0:
        print("The number is negative.")
    else:
        print("The number is zero.")
    


.. parsed-literal::

    Enter a number:  5
    

.. parsed-literal::

    The number is positive.
    

.. code:: ipython3

    # 5)Write a Python program to get the Factorial number of given numbers.
    
    # function for factorial
    def factorial(num):
        # Check if the number is negative
        if num < 0:
            return "Factorial is not defined for negative numbers."
        # Check if the number is 0 or 1 
        elif num == 0 or num == 1:
            return 1
        else:
            # Initialize result to 1
            result = 1
            for i in range(2, num + 1):
                result *= i # Multiply result by the current number
            return result # Return the final factorial value
    
    # Prompt the user to enter a number
    number = int(input("Enter a number: "))
    print("The factorial of", number, "is:", factorial(number))
    


.. parsed-literal::

    Enter a number:  5
    

.. parsed-literal::

    The factorial of 5 is: 120
    

.. code:: ipython3

    # 6) Write a Python program to get the Fibonacci series of given range. 
    
    def fibonacci_series(n):
        # Initialize an empty list to store the Fibonacci sequence
        fib_sequence = []
        # Start with the first two numbers in the Fibonacci sequence: 0 and 1
        a, b = 0, 1
        # Loop until the list contains 'n' terms
        while len(fib_sequence) < n:
            # Append the current number to the sequence
            fib_sequence.append(a)
            # Update 'a' and 'b' for the next iteration
            # 'a' takes the value of 'b', and 'b' becomes the sum of 'a' and 'b'
            a, b = b, a + b
        # Return the complete Fibonacci sequence
        return fib_sequence
    
    # Prompt the user to input the number of terms for the Fibonacci series
    num_terms = int(input("Enter the number of terms for the Fibonacci series: "))
    # Call the function and print the Fibonacci series
    print("Fibonacci series of", num_terms, "terms:", fibonacci_series(num_terms))
    
    


.. parsed-literal::

    Enter the number of terms for the Fibonacci series:  5
    

.. parsed-literal::

    Fibonacci series of 5 terms: [0, 1, 1, 2, 3]
    

# 7) How memory is managed in Python? 
=>
In Python, memory management is handled by an internal memory manager and an automatic garbage collector.

1. Memory Allocation: Python allocates memory for objects dynamically in the heap. The memory manager controls this allocation for efficient usage.
2. Garbage Collection: Python’s garbage collector automatically frees memory for objects that are no longer in use. It uses *reference counting* and a *cyclic garbage collector* to detect and remove unused objects.

This system helps Python manage memory efficiently, ensuring resources are freed up as needed without requiring manual intervention from the programmer.

# 8) What is the purpose continuing statement in python?
=>
In Python, the continue statement is used to skip the current iteration of a loop and move to the next iteration. It is commonly used when you want to avoid executing the remaining code in a loop for a particular iteration based on a condition

.. code:: ipython3

    # 9) Write python program that swap two number with temp variable and without temp variable. 
    
    def swap_with_temp(a, b):
        # Use a temporary variable to hold the value of 'a'
        temp = a
        # Assign the value of 'b' to 'a'
        a = b
        # Assign the value of the temporary variable (original 'a') to 'b'
        b = temp
        # Return the swapped values
        return a, b
    
    # Prompt the user to input the first number
    num1 = int(input("Enter first number: "))
    # Prompt the user to input the second number
    num2 = int(input("Enter second number: "))
    
    # Call the swap_with_temp function to swap the values of num1 and num2
    num1, num2 = swap_with_temp(num1, num2)
    
    # Print the results after swapping
    print("After swapping (with temp):")
    print("First number:", num1)
    print("Second number:", num2)
    
    


.. parsed-literal::

    Enter first number:  5
    Enter second number:  2
    

.. parsed-literal::

    After swapping (with temp):
    First number: 2
    Second number: 5
    

.. code:: ipython3

    # 10) Write a Python program to find whether a given number is even or odd, print out an appropriate message to the user. 
    
    def check_even_odd(number):
        # Check if the number is divisible by 2
        if number % 2 == 0:
            # If true, return a message indicating the number is even
            return "The number is even."
        else:
            # If false, return a message indicating the number is odd
            return "The number is odd."
    
    # Prompt the user to input a number
    num = int(input("Enter a number: "))
    
    # Call the check_even_odd function with the user-provided number
    # and print the result
    print(check_even_odd(num))
    
    


.. parsed-literal::

    Enter a number:  5
    

.. parsed-literal::

    The number is odd.
    

.. code:: ipython3

    # 11) Write a Python program to test whether a passed letter is a vowel or not. 
    
    def check_vowel(letter):
        # Define a string containing all vowels (both uppercase and lowercase)
        vowels = 'a e i o u A E I O U'
        # Check if the input letter is present in the vowels string
        if letter in vowels:
            # Return a message indicating the letter is a vowel
            return f"The letter {letter} is a vowel."
        else:
            # Return a message indicating the letter is not a vowel
            return f"The letter {letter} is not a vowel."
    
    # Prompt the user to input a letter
    char = input("Enter a letter: ")
    
    # Check if the input is a single character and is an alphabetic letter
    if len(char) == 1 and char.isalpha():
        # Call the check_vowel function and print the result
        print(check_vowel(char))
    else:
        # Print an error message if the input is not valid
        print("Please enter a valid single letter.")
    
    


.. parsed-literal::

    Enter a letter:  L
    

.. parsed-literal::

    The letter L is not a vowel.
    

.. code:: ipython3

    # 12) Write a Python program to sum of three given integers. However, if two values are equal sum will be zero. 
    
    def sum_with_condition(a, b, c):
        # Check if any two numbers are equal
        if a == b or b == c or a == c:
            # If any pair is equal, return 0 as the result
            return 0
        else:
            # If all numbers are unique, return their sum
            return a + b + c
    
    # Prompt the user to input the first integer
    num1 = int(input("Enter first integer: "))
    # Prompt the user to input the second integer
    num2 = int(input("Enter second integer: "))
    # Prompt the user to input the third integer
    num3 = int(input("Enter third integer: "))
    
    # Call the sum_with_condition function with the three numbers
    result = sum_with_condition(num1, num2, num3)
    
    # Print the result of the function
    print("The result is:", result)
    
    


.. parsed-literal::

    Enter first integer:  5
    Enter second integer:  2
    Enter third integer:  5
    

.. parsed-literal::

    The result is: 0
    

.. code:: ipython3

    # 13) Write a Python program that will return true if the two given integer values are equal or their sum or difference is 5. 
    
    def check_condition(a, b):
        # Check if the two numbers are equal
        if a == b or a + b == 5 or abs(a - b) == 5:
            # Return True if any of the conditions are met
            return True
        else:
            # Return False if none of the conditions are met
            return False
    
    # Prompt the user to input the first integer
    num1 = int(input("Enter first integer: "))
    # Prompt the user to input the second integer
    num2 = int(input("Enter second integer: "))
    
    # Call the check_condition function with the two numbers
    # and check its return value
    if check_condition(num1, num2):
        # Print "True" if the function returns True
        print("True")
    else:
        # Print "False" if the function returns False
        print("False")
    


.. parsed-literal::

    Enter first integer:  5
    Enter second integer:  2
    

.. parsed-literal::

    False
    

.. code:: ipython3

    # 14) Write a python program to sum of the first n positive integers. 
    
    def sum_of_integers(n):
        # Calculate the sum of the first n positive integers using the formula n * (n + 1) / 2
        return n * (n + 1) // 2 
    
    # Prompt the user to input a positive integer
    n = int(input("Enter a positive integer n: "))
    
    # Check if the input is a positive integer
    if n > 0:
        # If valid, calculate the sum using the sum_of_integers function
        result = sum_of_integers(n)
        # Print the calculated sum
        print(f"The sum of the first {n} positive integers is: {result}")
    else:
        # Print an error message if the input is not a positive integer
        print("Please enter a positive integer.")
    
    


.. parsed-literal::

    Enter a positive integer n:  5
    

.. parsed-literal::

    The sum of the first 5 positive integers is: 15
    

.. code:: ipython3

    # 15) Write a Python program to calculate the length of a string. 
    
    def string_length(s):
        # Use the built-in len() function to calculate the length of the string
        return len(s)
    
    # Prompt the user to input a string
    string = input("Enter a string: ")
    
    # Call the string_length function with the user-provided string
    # and print the result
    print(f"The length of the string is: {string_length(string)}")
    
    


.. parsed-literal::

    Enter a string:  L
    

.. parsed-literal::

    The length of the string is: 1
    

.. code:: ipython3

    # 16) Write a Python program to count the number of characters (character frequency) in a string 
    
    def character_frequency(s):
        # Initialize an empty dictionary to store character frequencies
        freq = {}  
        # Iterate through each character in the string
        for char in s:
            # If the character is already in the dictionary, increment its count
            if char in freq:
                freq[char] += 1  
            else:
                # If the character is not in the dictionary, add it with a count of 1
                freq[char] = 1
        # Return the dictionary containing character frequencies
        return freq
    
    # Prompt the user to input a string
    string = input("Enter a string: ")
    
    # Call the character_frequency function with the input string
    result = character_frequency(string)
    
    # Print the character frequencies
    print("Character frequencies in the string:")
    # Loop through the dictionary and print each character and its count
    for char, count in result.items():
        print(f"'{char}': {count}")
    
    

# 17) What are negative indexes and why are they used? 
=>
Negative indexes in Python are used to access elements from the end of a sequence, such as a list, string, or tuple. Instead of starting from the beginning (index 0), negative indexes allow you to start counting from the last element of the sequence.

Convenience: They are helpful when you want to access elements from the end of a sequence without needing to know its length.
Readability: They make the code more concise and readable, especially when working with the last few elements of a sequence

.. code:: ipython3

    # 18) Write a Python program to count occurrences of a substring in a string. 
    
    def count_substring_occurrences(main_string, substring):
        # Use the built-in count() method to count how many times 'substring' appears in 'main_string'
        return main_string.count(substring)
    
    # Prompt the user to input the main string where we will search for the substring
    string = input("Enter the main string: ")
    
    # Prompt the user to input the substring they want to count within the main string
    substring = input("Enter the substring to count: ")
    
    # Call the count_substring_occurrences function to calculate the occurrences of the substring
    occurrences = count_substring_occurrences(string, substring)
    
    # Print the result, showing how many times the substring appears in the main string
    print(f"The substring '{substring}' occurs {occurrences} times in the main string.")
    
    


.. parsed-literal::

    Enter the main string:  MANTHAN
    Enter the substring to count:  MAN
    

.. parsed-literal::

    The substring 'MAN' occurs 1 times in the main string.
    

.. code:: ipython3

    # 19) Write a Python program to count the occurrences of each word in a given sentence.
    
    def word_count(string):
        # Split the input string into a list of words using space as a delimiter
        words = string.split()
        # Initialize an empty dictionary to store the frequency of each word
        word_freq = {}  
        # Loop through each word in the list of words
        for word in words:
            # If the word is already in the dictionary, increment its frequency
            if word in word_freq:
                word_freq[word] += 1
            else:
                # If the word is not in the dictionary, add it with a frequency of 1
                word_freq[word] = 1 
        # Return the dictionary containing the word frequencies
        return word_freq
    
    # Prompt the user to input a string of text
    string = input("Enter a string: ")
    
    # Call the word_count function with the input string and get the word frequencies
    result = word_count(string)
    
    # Print the word frequencies in the string
    print("Word frequencies in the string:")
    # Iterate over the dictionary and print each word along with its frequency
    for word, count in result.items():
        print(f"'{word}': {count}")
    
    


.. parsed-literal::

    Enter a string:  MANTHAN
    

.. parsed-literal::

    Word frequencies in the string:
    'MANTHAN': 1
    

.. code:: ipython3

    # 20) Write a Python program to get a single string from two given strings, separated by a space and swap the first two characters of each string. 
    
    def swap_first_two_chars(str1, str2):
        # Check if both strings have at least 2 characters
        if len(str1) >= 2 and len(str2) >= 2:
            # Swap the first two characters of each string
            str1 = str2[:2] + str1[2:]  # Replace the first two characters of str1 with the first two of str2
            str2 = str1[:2] + str2[2:]  # Replace the first two characters of str2 with the first two of str1
        # Return the modified strings, joined by a space
        return str1 + " " + str2
    
    # Prompt the user to input the first string
    string1 = input("Enter first string: ")
    # Prompt the user to input the second string
    string2 = input("Enter second string: ")
    
    # Call the swap_first_two_chars function to swap the first two characters of the strings
    result = swap_first_two_chars(string1, string2)
    
    # Print the result after swapping the first two characters of both strings
    print("Result after swapping first two characters:", result)
    


.. parsed-literal::

    Enter first string:  WELCOME TO PYTHON
    Enter second string:  HELLO PYTHON
    

.. parsed-literal::

    Result after swapping first two characters: HELCOME TO PYTHON HELLO PYTHON
    

.. code:: ipython3

    # 21) Write a Python program to add 'in' at the end of a given string (length should be at least 3). If the given string already ends with 'ing' then add 'ly' instead if the string length of the given string is less than 3, leave it unchanged. 
    
    def modify_string(s):
        # Check if the string length is less than 3
        if len(s) < 3:
            return s  # Return the string unchanged if its length is less than 3
        # Check if the string ends with 'ing'
        elif s.endswith('ing'):
            return s + 'ly'  # If it ends with 'ing', append 'ly' to the string
        else:
            return s + 'in'  # If it doesn't end with 'ing', append 'in' to the string
    
    # Prompt the user to enter a string
    string = input("Enter a string: ")
    
    # Call the modify_string function with the user's input and store the result
    modified_string = modify_string(string)
    
    # Print the modified string
    print("Modified string:", modified_string)
    
    


.. parsed-literal::

    Enter a string:  PYTHON
    

.. parsed-literal::

    Modified string: PYTHONin
    

.. code:: ipython3

    # 22) Write a Python function to reverses a string if its length is a multiple of 4. 
    
    def reverse_if_multiple_of_four(s):
        # Check if the length of the string is a multiple of 4
        if len(s) % 4 == 0:  
            # If true, return the string reversed using slicing (::-1)
            return s[::-1]  
        else:
            # If false, return the string unchanged
            return s  
    
    # Prompt the user to input a string
    string = input("Enter a string: ")
    
    # Call the reverse_if_multiple_of_four function to check the string's length and possibly reverse it
    result = reverse_if_multiple_of_four(string)
    
    # Print the result, which is either the reversed string or the original string
    print("Result:", result)
    


.. parsed-literal::

    Enter a string:  HELO
    

.. parsed-literal::

    Result: OLEH
    

.. code:: ipython3

    # 23) Write a Python program to get a string made of the first 2 and the last 2 chars from a given a string. If the string length is less than 2, return instead of the empty string.
    
    def first_and_last_two_chars(s):
        # Check if the string has less than 2 characters
        if len(s) < 2:
            # If the string is too short, return an empty string
            return ""  
        else:
            # If the string has 2 or more characters, return the first two and the last two characters concatenated
            return s[:2] + s[-2:]  
    
    # Prompt the user to input a string
    string = input("Enter a string: ")
    
    # Call the first_and_last_two_chars function to extract the first two and last two characters of the string
    result = first_and_last_two_chars(string)
    
    # Print the result, which is the concatenation of the first two and last two characters
    print("Result:", result)
    
    


.. parsed-literal::

    Enter a string:  MANTHAN
    

.. parsed-literal::

    Result: MAAN
    

.. code:: ipython3

    # 24) Write a Python function to insert a string in the middle of a string. 
    
    def insert_in_middle(original, to_insert):
        # Calculate the middle index of the original string
        middle_index = len(original) // 2  
        # Return a new string where 'to_insert' is placed in the middle of the original string
        return original[:middle_index] + to_insert + original[middle_index:]  
    
    # Prompt the user to input the original string
    original_string = input("Enter the original string: ")
    
    # Prompt the user to input the string they want to insert into the original string
    insert_string = input("Enter the string to insert: ")
    
    # Call the insert_in_middle function to insert 'insert_string' into 'original_string'
    result = insert_in_middle(original_string, insert_string)
    
    # Print the result, which is the original string with the inserted string in the middle
    print("Result:", result)
    
    


.. parsed-literal::

    Enter the original string:  WELCOME
    Enter the string to insert:  PYTHON
    

.. parsed-literal::

    Result: WELPYTHONCOME
    

# 25) What is List? How will you reverse a list?
=>
A list in Python is an ordered collection of items which can hold elements of different data types, such as integers, strings, and other objects. Lists are mutable, meaning their contents can be changed after they are created.

A list is defined by placing its elements inside square brackets [], and each element is separated by a comma.
Lists can hold heterogeneous data, which means you can store different data types in a single list.

-Reverse
There are several ways to reverse a list in Python. Here are some common methods:

1. Using the reverse() method (in-place reversal)
This method reverses the list in place and does not return a new list.
It modifies the original list.

2. Using slicing (creates a new reversed list)
This method creates a new list that is the reverse of the original one, leaving the original list unchanged.

3. Using the reversed() function (returns an iterator)
The reversed() function returns an iterator that can be converted into a list or used in a loop.

# 26) How will you remove last object from a list? 
=> 
1. Using the pop() method
The pop() method removes and returns the last element from the list. If no index is specified, it defaults to removing the last item

The pop() method not only removes the last element but also returns it, allowing you to capture or use the removed item.
If the list is empty and you call pop(), it will raise an IndexError

2. Using slicing
You can also use slicing to remove the last element of the list. This does not modify the list in place, but creates a new list without the last item.

This approach creates a new list that excludes the last item. The original list will be modified in the sense that it is now replaced with the new list.
The original list remains unchanged if slicing is used on a separate variable.

# 27) Suppose list1 is [2, 33, 222, 14, and 25], what is list1 [-1]? 
=>
In Python, negative indexing allows you to access elements from the end of a list. So, when you use list1[-1], it refers to the last element of the list.

Given that list1 = [2, 33, 222, 14, 25], here’s what happens:

list1[-1] will access the last element of the list, which is 25.


# 28) Differentiate between append () and extend () methods?
=>
The append() and extend() methods are both used to add elements to a list in Python, but they behave differently in terms of how they add elements.
Purpose: Adds a single element to the end of the list.
How it works: The element passed to append() is added as a single object, regardless of its type.
Syntax: list.append(element

Purpose: Adds each element from an iterable (e.g., list, tuple, string) to the end of the list individually.
How it works: The extend() method takes an iterable (like a list, tuple, or string) and adds each of its elements to the list.
Syntax: list.extend(iterable)

.. code:: ipython3

    # 29) Write a Python function to get the largest number, smallest num and sum of all from a list.
    
    def list_stats(numbers):
        # Check if the input list is empty
        if len(numbers) == 0:
            return "The list is empty"  # Return a message if the list is empty
        
        # Find the largest number in the list using the max() function
        largest = max(numbers)  
        # Find the smallest number in the list using the min() function
        smallest = min(numbers)  
        # Calculate the sum of all numbers in the list using the sum() function
        total_sum = sum(numbers)  
        
        # Return the largest, smallest, and the sum of the numbers
        return largest, smallest, total_sum
    
    
    # Example list of numbers
    numbers = [10, 20, 4, 45, 99]
    
    # Call the list_stats function to get the largest, smallest, and sum of the list
    largest, smallest, total_sum = list_stats(numbers)
    
    # Print the largest number from the list
    print(f"Largest number: {largest}")
    # Print the smallest number from the list
    print(f"Smallest number: {smallest}")
    # Print the sum of all numbers in the list
    print(f"Sum of all numbers: {total_sum}")
    
    


.. parsed-literal::

    Largest number: 99
    Smallest number: 4
    Sum of all numbers: 178
    

# 30) How will you compare two list?
=>
To compare two lists in Python:

1.Using ==: Compares both the order and elements of the lists.
2.Using !=: Checks if the lists are not equal.
3.Using is: Checks if both lists reference the same object in memory.
4.Using set(): Compares lists ignoring order and duplicates.
5.Using sorted(): Compares lists ignoring order, considering duplicates

.. code:: ipython3

    # 31) Write a Python program to count the number of strings where the string length is 2 or more and the first and last character are same from a given list of strings. 
    
    def count_matching_strings(str_list):
        # Initialize a counter to keep track of strings that meet the condition
        count = 0
        # Loop through each string in the list
        for s in str_list:
            # Check if the string has a length of 2 or more and if the first and last characters are the same
            if len(s) >= 2 and s[0] == s[-1]:  
                # If the condition is met, increment the count
                count += 1
        # Return the final count of matching strings
        return count
    
    # List of strings to check
    string_list = ['aba', 'xyz', 'aa', 'a', 'ab', 'cdc']
    
    # Call the count_matching_strings function to get the number of strings that meet the condition
    result = count_matching_strings(string_list)
    
    # Print the result, showing how many strings have length >= 2 and their first & last characters are the same
    print("Count of strings where length >= 2 and first & last character are the same:", result)
    
    


.. parsed-literal::

    Count of strings where length >= 2 and first & last character are the same: 3
    

.. code:: ipython3

    # 32) Write a Python program to remove duplicates from a list. 
    
    def remove_duplicates(lst):
        # Initialize an empty list to store unique items
        unique_list = []
        # Initialize an empty set to keep track of items that have already been encountered
        seen = set()
        # Iterate through each item in the input list
        for item in lst:
            # If the item has not been seen before, add it to the unique list and mark it as seen
            if item not in seen:
                unique_list.append(item)  # Add the item to the unique list
                seen.add(item)  # Add the item to the set of seen items
        # Return the list of unique items
        return unique_list
    
    # Input list with some duplicate values
    my_list = [1, 2, 2, 3, 4, 4, 5, 6, 6]
    
    # Call the remove_duplicates function to get the list with duplicates removed
    unique_list = remove_duplicates(my_list)
    
    # Print the result after removing duplicates from the list
    print("List after removing duplicates:", unique_list)
    
    


.. parsed-literal::

    List after removing duplicates: [1, 2, 3, 4, 5, 6]
    

.. code:: ipython3

    # 33) Write a Python program to check a list is empty or not.
    
    def is_empty(lst):
        # Check if the length of the list is 0
        return len(lst) == 0  # If the list is empty, return True, otherwise return False
    
    # Example of an empty list
    list1 = []
    # Example of a non-empty list
    list2 = [1, 2, 3]
    
    # Check if list1 is empty and print the result
    print("list 1 empty=", is_empty(list1))  
    # Check if list2 is empty and print the result
    print("list 2 empty=", is_empty(list2))  
     
    


.. parsed-literal::

    list 1 empty= True
    list 2 empty= False
    

.. code:: ipython3

    # 34) Write a Python function that takes two lists and returns true if they have at least one common member.
    
    def have_common_member(list1, list2):
        # Convert both lists to sets and check if they have any common elements using the intersection (&) operator
        return bool(set(list1) & set(list2))  # Return True if there's at least one common element, otherwise False
    
    # Example lists with some common and some different elements
    list1 = [1, 2, 3, 4]
    list2 = [3, 4, 5, 6]
    
    # Call the function to check if the two lists have any common members
    result = have_common_member(list1, list2)
    
    # Print the result, showing whether the lists share at least one common element
    print("Do the lists have at least one common member?", result)
    


.. parsed-literal::

    Do the lists have at least one common member? True
    

.. code:: ipython3

    # 35) Write a Python program to generate and print a list of first and last 5 elements where the values are square of numbers between 1 and 30. 
    
    def generate_squares():
        # Generate a list of squares of numbers from 1 to 30 using a list comprehension
        squares = [i**2 for i in range(1, 31)]
        
        # Extract the first 5 elements from the list of squares
        first_five = squares[:5]
        # Extract the last 5 elements from the list of squares
        last_five = squares[-5:]
        
        # Return the first and last five squares
        return first_five, last_five
    
    # Call the function to get the first and last five elements of the squares list
    first_five, last_five = generate_squares()
    
    # Print the first 5 squares
    print("First 5 elements:", first_five)
    # Print the last 5 squares
    print("Last 5 elements:", last_five)
    
    
    


.. parsed-literal::

    First 5 elements: [1, 4, 9, 16, 25]
    Last 5 elements: [676, 729, 784, 841, 900]
    

.. code:: ipython3

    # 36) Write a Python function that takes a list and returns a new list with unique elements of the first list.
    
    def get_unique_elements(lst):
        # Convert the list to a set to remove duplicates, then convert it back to a list
        return list(set(lst))  # The set removes duplicates, and list() converts the set back to a list
    
    # Example input list with some duplicate values
    input_list = [1, 2, 2, 3, 4, 4, 5, 6, 6]
    
    # Call the get_unique_elements function to remove duplicates from the input list
    unique_list = get_unique_elements(input_list)
    
    # Print the result, which is the input list with duplicates removed
    print("List with unique elements:", unique_list)
    


.. parsed-literal::

    List with unique elements: [1, 2, 3, 4, 5, 6]
    

.. code:: ipython3

    # 37) Write a Python program to convert a list of characters into a string.
    
    def list_to_string(char_list):
        # Use the join() method to concatenate the elements of the list into a single string
        return ''.join(char_list)  # The empty string '' is used as the separator to join the characters
    
    # Example list of characters
    char_list = ['H', 'e', 'l', 'l', 'o']
    
    # Call the list_to_string function to convert the list of characters into a string
    result_string = list_to_string(char_list)
    
    # Print the resulting string
    print("Converted string:", result_string)
    
    


.. parsed-literal::

    Converted string: Hello
    

.. code:: ipython3

    # 38) Write a Python program to select an item randomly from a list. 
    
    import random  # Import the random module to use random selection functions
    
    def select_random_item(lst):
        # Use random.choice() to select a random item from the given list
        return random.choice(lst)  # This returns a randomly selected element from the list
    
    # Example list from which a random item will be selected
    my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
    
    # Call the select_random_item function to randomly select an item from the list
    random_item = select_random_item(my_list)
    
    # Print the randomly selected item from the list
    print("Randomly selected item:", random_item)
    
    


.. parsed-literal::

    Randomly selected item: 9
    

.. code:: ipython3

    # 39) Write a Python program to find the second smallest number in a list. 
    
    def second_smallest(lst):
        # Convert the list to a set to remove duplicates, and then sort it in ascending order
        unique_lst = sorted(set(lst))  
        
        # Check if there are at least two unique elements
        if len(unique_lst) >= 2:
            return unique_lst[1]  # Return the second smallest element
        else:
            return "List does not have a second smallest element"  # Return a message if there's no second smallest element
    
    # Example list with some repeated elements
    my_list = [12, 35, 1, 10, 34, 1]
    
    # Call the second_smallest function to get the second smallest unique element
    result = second_smallest(my_list)
    
    # Print the result, which will be the second smallest element or a message if it doesn't exist
    print("Second smallest number:", result)
    
    


.. parsed-literal::

    Second smallest number: 10
    

.. code:: ipython3

    # 40) Write a Python program to get unique values from a list 
    
    def get_unique_values(lst):
        # Convert the list to a set to remove duplicates, then convert the set back to a list
        return list(set(lst))  # The set removes duplicates, and list() converts it back to a list
    
    # Example list with some duplicate values
    my_list = [1, 2, 2, 3, 4, 4, 5, 6, 6]
    
    # Call the get_unique_values function to remove duplicates from the list
    unique_values = get_unique_values(my_list)
    
    # Print the resulting list that contains only the unique values
    print("Unique values from the list:", unique_values)
    


.. parsed-literal::

    Unique values from the list: [1, 2, 3, 4, 5, 6]
    

.. code:: ipython3

    # 41) Function to check if a list contains a sublist
    
    def contains_sublist(main_list, sublist):
        # Use the any() function with a generator expression to check if any subsequence in the main list matches the sublist
        return any(main_list[i:i+len(sublist)] == sublist for i in range(len(main_list)-len(sublist)+1))
    
    # Example main list and sublist
    main_list = [1, 2, 3, 4, 5, 6]
    sublist = [3, 4, 5]
    
    # Call the contains_sublist function to check if the sublist is present in the main list
    result = contains_sublist(main_list, sublist)
    
    # Print the result, which is a boolean indicating whether the sublist exists in the main list
    print("Contain the sublist?", result)
    
    


.. parsed-literal::

    Contain the sublist? True
    

.. code:: ipython3

    # 42) Write a Python program to split a list into different variables. 
    
    # Given list with 5 elements
    my_list = [1, 2, 3, 4, 5]
    
    # Unpacking the list into individual variables
    a, b, c, d, e = my_list  # The list elements are assigned to variables a, b, c, d, and e
    
    # Printing each variable with its assigned value
    print("a:", a)  # Prints the value of 'a' (1)
    print("b:", b)  # Prints the value of 'b' (2)
    print("c:", c)  # Prints the value of 'c' (3)
    print("d:", d)  # Prints the value of 'd' (4)
    
    


.. parsed-literal::

    a: 1
    b: 2
    c: 3
    d: 4
    

# 43) )What is tuple? Difference between list and tuple. 
=>
A tuple is a built-in data structure in Python that can hold a collection of ordered, immutable items. Once a tuple is created, its elements cannot be modified, making it ideal for storing data that should remain constant.

Aspect	                     List	                                                  Tuple
Mutability	       Mutable (can be changed).	                         Immutable (cannot be changed).
Syntax	           Defined with square brackets []. 	                 Defined with parentheses ().
Performance	       Slower due to mutability.	                         Faster due to immutability.
Use Cases      	   Suitable for dynamic data.	                         Suitable for fixed/static data.
Methods	           Has more built-in methods (e.g., append, remove). 	 Fewer methods (e.g., count, index).
Memory Usage	   Consumes more memory.	                             Consumes less memory.

.. code:: ipython3

    # 44) Write a Python program to create a tuple with different data types. 
    
    # Defining a tuple with various data types (integer, string, float, boolean, list, dictionary, and another tuple)
    mixed_tuple = (42, "hello", 3.14, True, [1, 2, 3], {"key": "value"}, (7, 8))
    
    # Printing the entire tuple to show its contents
    print("Tuple with different data types:", mixed_tuple)
    
    # Loop through the tuple using enumerate() to get both index and item
    for index, item in enumerate(mixed_tuple):
        # Print the index, item, and the type of the item using type()
        print(f"Element at index {index} is {item} of type {type(item)}")
    
    


.. parsed-literal::

    Tuple with different data types: (42, 'hello', 3.14, True, [1, 2, 3], {'key': 'value'}, (7, 8))
    Element at index 0 is 42 of type <class 'int'>
    Element at index 1 is hello of type <class 'str'>
    Element at index 2 is 3.14 of type <class 'float'>
    Element at index 3 is True of type <class 'bool'>
    Element at index 4 is [1, 2, 3] of type <class 'list'>
    Element at index 5 is {'key': 'value'} of type <class 'dict'>
    Element at index 6 is (7, 8) of type <class 'tuple'>
    

.. code:: ipython3

    # 45) Write a Python program to unzip a list of tuples into individual lists. 
    
    # Defining a list of tuples, where each tuple contains an integer and a string
    tuple_list = [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]
    
    # Using the zip function with unpacking (*) to separate the elements of the tuples
    # zip(*tuple_list) essentially "unzips" the list of tuples into two separate lists
    list1, list2 = zip(*tuple_list)
    
    # Converting the results of zip (which are tuples) into lists
    list1 = list(list1)
    list2 = list(list2)
    
    # Printing the unzipped lists
    print("List 1:", list1)  # List 1 will contain the integers: [1, 2, 3, 4]
    print("List 2:", list2)  # List 2 will contain the characters: ['a', 'b', 'c', 'd']
    
    


.. parsed-literal::

    List 1: [1, 2, 3, 4]
    List 2: ['a', 'b', 'c', 'd']
    

.. code:: ipython3

    # 46) Write a Python program to convert a list of tuples into a dictionary. 
    
    # List of tuples where each tuple contains a key-value pair
    list_of_tuples = [("name", "manthan"), ("age", 25), ("city", "ahmedabad")]
    
    # Converting the list of tuples into a dictionary using the dict() function
    dictionary = dict(list_of_tuples)
    
    # Printing the converted dictionary
    print("Converted dictionary:", dictionary)
    


.. parsed-literal::

    Converted dictionary: {'name': 'manthan', 'age': 25, 'city': 'ahmedabad'}
    

# 47) How will you create a dictionary using tuples in python? 
=>
The dict() constructor takes an iterable of tuples where each tuple has two elements.
The first element becomes the key, and the second becomes the value in the dictionary


.. code:: ipython3

    # 48) Write a Python script to sort (ascending and descending) a dictionary by value.
    
    # Define a dictionary with fruit names as keys and quantities as values
    my_dict = {"apple": 3, "banana": 1, "cherry": 5, "date": 2}
    
    # Sorting the dictionary items in ascending order based on the value (second item of the tuple)
    # 'key=lambda item: item[1]' sorts by the second element (the quantity) of each key-value pair
    ascending = dict(sorted(my_dict.items(), key=lambda item: item[1]))
    
    # Sorting the dictionary items in descending order based on the value (second item of the tuple)
    # 'reverse=True' sorts the items in reverse (highest to lowest) based on the value
    descending = dict(sorted(my_dict.items(), key=lambda item: item[1], reverse=True))
    
    # Printing the original dictionary
    print("Original Dictionary:", my_dict)
    
    # Printing the dictionary sorted in ascending order based on the values
    print("Ascending Order:", ascending)
    
    # Printing the dictionary sorted in descending order based on the values
    print("Descending Order:", descending)
    
    


.. parsed-literal::

    Original Dictionary: {'apple': 3, 'banana': 1, 'cherry': 5, 'date': 2}
    Ascending Order: {'banana': 1, 'date': 2, 'apple': 3, 'cherry': 5}
    Descending Order: {'cherry': 5, 'apple': 3, 'date': 2, 'banana': 1}
    

.. code:: ipython3

    # 49) Write a Python script to concatenate following dictionaries to create a new one. 
    
    # Define three dictionaries with key-value pairs
    dict1 = {"a": 1, "b": 2}
    dict2 = {"c": 3, "d": 4}
    dict3 = {"e": 5, "f": 6}
    
    # Create a copy of dict1 to avoid modifying the original dict1
    concatenated_dict = dict1.copy()
    
    # Update the copied dictionary with the key-value pairs from dict2
    concatenated_dict.update(dict2)
    
    # Update the copied dictionary further with the key-value pairs from dict3
    concatenated_dict.update(dict3)
    
    # Print the concatenated dictionary containing elements from all three dictionaries
    print("Concatenated Dictionary:", concatenated_dict)
    
    


.. parsed-literal::

    Concatenated Dictionary: {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5, 'f': 6}
    

.. code:: ipython3

    # 50) Write a Python script to check if a given key already exists in a dictionary.
    
    # Define a dictionary with key-value pairs
    my_dict = {"name": "Alice", "age": 25, "city": "New York"}
    
    # Define the key that you want to check in the dictionary
    key_to_check = "age"
    
    # Check if the specified key exists in the dictionary
    if key_to_check in my_dict:
        # If the key exists, print a confirmation message
        print(f"The key '{key_to_check}' exists in the dictionary.")
    else:
        # If the key does not exist, print a message stating that
        print(f"The key '{key_to_check}' does not exist in the dictionary.")
    
    


.. parsed-literal::

    The key 'age' exists in the dictionary.
    

# 51) How Do You Traverse Through a Dictionary Object in Python? 

To traverse a dictionary in Python, you can iterate over its keys, values, or key-value pairs:

my_dict = " man "
Keys:
for key in my_dict:
    print(key)

Values:
for value in my_dict.values():
    print(value)

Key-Value Pairs:
for key, value in my_dict.items():
    print(key, value)

Sorted Keys:
for key in sorted(my_dict):
    print(key, my_dict[key])
    
These methods allow you to efficiently access and process dictionary elements.


# 52) How Do You Check the Presence of a Key in A Dictionary?

To check the presence of a key in a Python dictionary, use these methods:

1. Using the in Keyword
my_dict = {"name": "Alice", "age": 25, "city": "New York"}

if "name" in my_dict:
    print("Key 'name' exists.")
2. Using the not in Keyword
if "gender" not in my_dict:
    print("Key 'gender' does not exist.")
3. Using the .get() Method
if my_dict.get("name") is not None:
    print("Key 'name' exists.")
These methods are efficient and avoid errors like KeyError.

.. code:: ipython3

    # 53) Write a Python script to print a dictionary where the keys are numbers between 1 and 15. 
    
    # Create a dictionary with keys between 1 and 15, values are squares of keys
    my_dict = {key: key**2 for key in range(1, 16)}
    
    # Print the dictionary
    print("Dictionary:", my_dict)
    


.. parsed-literal::

    Dictionary: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81, 10: 100, 11: 121, 12: 144, 13: 169, 14: 196, 15: 225}
    

.. code:: ipython3

    # 54) Write a Python program to check multiple keys exists in a dictionary.
    
    def check_keys_exist(dictionary, keys):
        # Check if all keys in the list exist in the dictionary
        return all(key in dictionary for key in keys)
    
    # Example dictionary
    my_dict = {"name": "Alice", "age": 25, "city": "New York"}
    
    # Keys to check
    keys_to_check = ["name", "age"]
    
    # Check and print result
    if check_keys_exist(my_dict, keys_to_check):
        print("All keys exist in the dictionary.")
    else:
        print("Some keys are missing.")
    


.. parsed-literal::

    All keys exist in the dictionary.
    

.. code:: ipython3

    # 55) Write a Python script to merge two Python dictionaries 
    
    # Define two dictionaries
    dict1 = {"name": "Alice", "age": 25}
    dict2 = {"city": "New York", "country": "USA"}
    
    # Merge dictionaries using the union operator (Python 3.9+)
    merged_dict = dict1 | dict2
    
    # Print the merged dictionary
    print("Merged Dictionary:", merged_dict)
    


.. parsed-literal::

    Merged Dictionary: {'name': 'Alice', 'age': 25, 'city': 'New York', 'country': 'USA'}
    

.. code:: ipython3

    # 56) Write a Python program to map two lists into a dictionary Sample output: Counter ({'a': 400, 'b': 400,’d’: 400, 'c': 300}).
    
    # Two sample lists
    keys = ['a', 'b', 'c', 'd']
    values = [400, 400, 300, 400]
    
    # Map the two lists into a dictionary
    result = dict(zip(keys, values))
    
    # Print the resulting dictionary
    print("Mapped Dictionary:", result)
    


.. parsed-literal::

    Mapped Dictionary: {'a': 400, 'b': 400, 'c': 300, 'd': 400}
    

.. code:: ipython3

    # 57) Write a Python program to find the highest 3 values in a dictionary 
    
    # Sample dictionary
    my_dict = {'a': 400, 'b': 300, 'c': 500, 'd': 700, 'e': 600}
    
    # Get the highest 3 values using sorted() and slicing
    highest_values = sorted(my_dict.values(), reverse=True)[:3]
    
    # Print the highest 3 values
    print("Highest 3 values:", highest_values)
    


.. parsed-literal::

    Highest 3 values: [700, 600, 500]
    

.. code:: ipython3

    # 58) Write a Python program to combine values in python list of dictionaries. 
         # Sample data: [{'item': 'item1', 'amount': 400}, {'item': 'item2', 'amount': 
         # 300}, o {'item': 'item1', 'amount': 750}] 
         # Expected Output:
         # • Counter ({'item1': 1150, 'item2': 300})
    
    from collections import Counter
    
    # Sample data: list of dictionaries
    data = [{'item': 'item1', 'amount': 400}, {'item': 'item2', 'amount': 300}, {'item': 'item1', 'amount': 750}]
    
    # Create a Counter to accumulate the sum of amounts for each item
    result = Counter()
    
    # Iterate through the list of dictionaries and update the counter
    for entry in data:
        result[entry['item']] += entry['amount']
    
    # Print the result
    print("Combined Values:", result)
    


.. parsed-literal::

    Combined Values: Counter({'item1': 1150, 'item2': 300})
    

.. code:: ipython3

    # 59) Write a Python program to create a dictionary from a string. 
        # Note: Track the count of the letters from the string 
    
    # Input string
    input_string = "hello world"
    
    # Create an empty dictionary to store the count of each letter
    letter_count = {}
    
    # Iterate through each character in the string
    for char in input_string:
        # Only consider alphabetic characters and ignore spaces
        if char.isalpha():
            # Increment the count of the letter in the dictionary
            letter_count[char] = letter_count.get(char, 0) + 1
    
    # Print the dictionary with letter counts
    print("Letter count dictionary:", letter_count)
    


.. parsed-literal::

    Letter count dictionary: {'h': 1, 'e': 1, 'l': 3, 'o': 2, 'w': 1, 'r': 1, 'd': 1}
    

.. code:: ipython3

    # 60) Sample string:
    #'    w3resource' Expected output:
    #     • {'3': 1,’s’: 1, 'r': 2, 'u': 1, 'w': 1, 'c': 1, 'e': 2, 'o': 1}
    
    from collections import Counter
    
    # Sample string
    sample_string = 'w3resource'
    
    # Count characters
    char_count = Counter(sample_string)
    
    # Print the result
    print(dict(char_count))
    
    


.. parsed-literal::

    {'w': 1, '3': 1, 'r': 2, 'e': 2, 's': 1, 'o': 1, 'u': 1, 'c': 1}
    

.. code:: ipython3

    # 61) Write a Python function to calculate the factorial of a number (a nonnegative integer) 
    
    def factorial(n):
        """
        Calculate the factorial of a nonnegative integer.
    
        Parameters:
        n (int): The nonnegative integer.
    
        Returns:
        int: The factorial of the number.
        """
        if n < 0:
            raise ValueError("Factorial is not defined for negative numbers.")
        elif n == 0 or n == 1:
            return 1
        else:
            result = 1
            for i in range(2, n + 1):
                result *= i
            return result
    
    # Example usage
    number = 5
    print(f"The factorial of {number} is {factorial(number)}")
    


.. parsed-literal::

    The factorial of 5 is 120
    

.. code:: ipython3

    # 62) Write a Python function to check whether a number is in a given range 
    
    def is_in_range(number, start, end):
        """
        Check if a number is in a given range [start, end].
    
        Parameters:
        number (int or float): The number to check.
        start (int or float): The start of the range.
        end (int or float): The end of the range.
    
        Returns:
        bool: True if the number is in the range, False otherwise.
        """
        return start <= number <= end
    
    # Example usage
    number = 5
    range_start = 1
    range_end = 10
    
    if is_in_range(number, range_start, range_end):
        print(f"{number} is in the range [{range_start}, {range_end}]")
    else:
        print(f"{number} is not in the range [{range_start}, {range_end}]")
    


.. parsed-literal::

    5 is in the range [1, 10]
    

.. code:: ipython3

    #63) Write a Python function to check whether a number is perfect or not. 
    
    def is_perfect_number(n):
        """
        Check whether a number is a perfect number.
    
        Parameters:
        n (int): The number to check.
    
        Returns:
        bool: True if the number is perfect, False otherwise.
        """
        if n <= 0:
            return False
    
        divisors_sum = sum(i for i in range(1, n) if n % i == 0)
        return divisors_sum == n
    
    # Example usage
    number = 6
    if is_perfect_number(number):
        print(f"{number} is a perfect number.")
    else:
        print(f"{number} is not a perfect number.")
    


.. parsed-literal::

    6 is a perfect number.
    

.. code:: ipython3

    # 64) Write a Python function that checks whether a passed string is palindrome or not 
    
    def is_palindrome(s):
        """
        Check whether a string is a palindrome.
    
        Parameters:
        s (str): The string to check.
    
        Returns:
        bool: True if the string is a palindrome, False otherwise.
        """
        # Remove spaces and convert to lowercase for consistent comparison
        cleaned_string = ''.join(c.lower() for c in s if c.isalnum())
        return cleaned_string == cleaned_string[::-1]
    
    # Example usage
    string = "A man, a plan, a canal, Panama"
    if is_palindrome(string):
        print(f'"{string}" is a palindrome.')
    else:
        print(f'"{string}" is not a palindrome.')
    


.. parsed-literal::

    "A man, a plan, a canal, Panama" is a palindrome.
    

# 65) How Many Basic Types of Functions Are Available in Python?  
=>
n Python, there are two basic types of functions:

1. Built-in Functions
These are functions provided by Python and are always available without the need to define them.
Examples:
print(): Prints a value.
len(): Returns the length of an object.
type(): Returns the type of an object.
input(): Gets user input.
sum(): Returns the sum of a sequence.
Python has over 70 built-in functions. You can find a full list here in the official Python documentation.

2. User-defined Functions
These are functions created by the user to perform specific tasks.

Defined using the def keyword.

Example:

python
Copy code
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!
Additional Categories of Functions:
While the basic classification is as above, user-defined functions can be further categorized based on how they handle inputs and outputs:

Functions with no arguments and no return value
Functions with arguments but no return value
Functions with arguments and return value
Functions with no arguments but return value
Summary
Basic types: Built-in and User-defined.
User-defined functions offer flexibility, while built-in functions cover common operations.

.. code:: ipython3

    # 66) How can you pick a random item from a list or tuple?
    
    import random
    
    # Example list
    my_list = [10, 20, 30, 40, 50]
    
    # Pick a random item
    random_item = random.choice(my_list)
    
    print(f"Randomly selected item: {random_item}")
    


.. parsed-literal::

    Randomly selected item: 40
    

.. code:: ipython3

    # 67) How can you pick a random item from a range?
    
    import random
    
    # Example list
    my_list = [10, 20, 30, 40, 50]
    
    # Pick a random item
    random_item = random.choice(my_list)
    
    print(f"Randomly selected item: {random_item}")
    


.. parsed-literal::

    Randomly selected item: 50
    

# 68) How can you get a random number in python?

n Python, you can use the random module to generate random numbers. Here are the most common ways to get random numbers:

1. Generate a Random Integer
Use random.randint(a, b) to generate a random integer between a and b (inclusive).
import random

# Generate a random integer between 1 and 10
random_integer = random.randint(1, 10)
print(f"Random Integer: {random_integer}")

2. Generate a Random Float
Use random.random() to generate a random float between 0.0 and 1.0.
import random

# Generate a random float between 0 and 1
random_float = random.random()
print(f"Random Float: {random_float}")

3. Generate a Random Float in a Specified Range
Use random.uniform(a, b) to generate a random float between a and b.
import random

# Generate a random float between 1.5 and 6.5
random_float_range = random.uniform(1.5, 6.5)
print(f"Random Float in Range: {random_float_range}")

4. Generate a Random Number from a Range
Use random.randrange(start, stop, step) to generate a random number from a range.import random

# Generate a random number from 0 to 9 (step 2)
random_range = random.randrange(0, 10, 2)
print(f"Random Number from Range: {random_range}")

5. Generate a Random Number from a Sequence
Use random.choice() to select a random item from a list, tuple, or range.import random

# Random number from a list
random_choice = random.choice([5, 10, 15, 20])
print(f"Random Choice: {random_choice}")

6. Generate Random Numbers with Gaussian Distribution
Use random.gauss(mu, sigma) to generate random numbers with a Gaussian distribution.import random

# Generate a random number with mean=0 and standard deviation=1
random_gaussian = random.gauss(0, 1)
print(f"Random Gaussian: {random_gaussian}")



.. code:: ipython3

    # 69) How will you set the starting value in generating random numbers?
    
    import random
    
    # Set the seed
    random.seed(42)
    
    # Generate random numbers
    print(random.randint(1, 10))  # Always the same for a given seed
    print(random.random())        # Always the same for a given seed
     


.. parsed-literal::

    2
    0.025010755222666936
    

.. code:: ipython3

    # 70) How will you randomize the items of a list in place?
    
    import random
    
    # Example list
    my_list = [1, 2, 3, 4, 5]
    
    # Shuffle the list in place
    random.shuffle(my_list)
    
    print(f"Shuffled List: {my_list}")
    


.. parsed-literal::

    Shuffled List: [4, 5, 1, 2, 3]
    

# 71) What is File function in python? What are keywords to create and write file. 
=>
In Python, working with files is a common task, and it can be done using the built-in open() function. The open() function is used to open a file and returns a file object, which you can use to read from or write to the file.

File Functions in Python
open(): Used to open a file, either for reading, writing, or appending. This function returns a file object that can be used to interact with the file.
close(): Used to close a file after operations are done.
read(): Reads the entire content of a file.
readline(): Reads the file line by line.
write(): Writes content to a file.
writelines(): Writes a list of strings to a file.
Keywords for Creating and Writing to a File
When opening a file using open(), you need to specify the mode. The most commonly used modes for creating and writing to a file are:

'w': Open the file for writing. If the file exists, it will be overwritten; if it does not exist, a new file will be created.
'a': Open the file for appending. If the file exists, data is appended to it; if the file does not exist, it is created.
'x': Open the file for exclusive creation. If the file already exists, the operation will fail.

# 72) Write a Python program to read an entire text file. 
# =>
#     To read an entire text file in Python, you can use the open() function along with the read() method.
#     Here's a simple program that demonstrates how to read the entire contents of a file:

# Open the file in read mode
with open('example.txt', 'r') as file:
    # Read the entire file content
    content = file.read()

# Print the content of the file
print(content)


.. code:: ipython3

    # 73)  Write a Python program to append text to a file and display the text.
    
    # Define the text to append
    text_to_append = "This is the new text being appended to the file.\n"
    
    # Open the file in append mode
    with open('example.txt', 'a') as file:
        file.write(text_to_append)
    
    # Open the file in read mode to display the updated content
    with open('example.txt', 'r') as file:
        content = file.read()
    
    # Display the updated content of the file
    print("Updated content of the file:")
    print(content)
    


.. parsed-literal::

    Updated content of the file:
    This is the new text being appended to the file.
    
    

.. code:: ipython3

    # 74) Write a Python program to read first n lines of a file.
    
    def read_first_n_lines(filename, n):
        try:
            # Open the file in read mode
            with open(filename, 'r') as file:
                # Read and print the first n lines
                for i in range(n):
                    line = file.readline()
                    if line:  # If line is not empty
                        print(line, end='')  # Print without adding an extra newline
                    else:
                        print(f"End of file reached after {i} lines.")
                        break
        except FileNotFoundError:
            print(f"The file {filename} does not exist.")
    
    # Example usage
    filename = 'example.txt'
    n = 5  # Number of lines to read
    read_first_n_lines(filename, n)
    


.. parsed-literal::

    This is the new text being appended to the file.
    End of file reached after 1 lines.
    

.. code:: ipython3

    # 75) Write a Python program to read last n lines of a file. 
    
    from collections import deque
    
    def read_last_n_lines(filename, n):
        try:
            with open(filename, 'r') as file:
                # Use deque to store the last n lines
                last_n_lines = deque(file, maxlen=n)
            
            # Print the last n lines
            for line in last_n_lines:
                print(line, end='')  # Print without adding an extra newline
        except FileNotFoundError:
            print(f"The file {filename} does not exist.")
    
    # Example usage
    filename = 'example.txt'
    n = 5  # Number of lines to read
    read_last_n_lines(filename, n)
    


.. parsed-literal::

    This is the new text being appended to the file.
    

.. code:: ipython3

    # 76) Write a Python program to read a file line by line and store it into a list.
    
    def read_file_to_list(filename):
        try:
            with open(filename, 'r') as file:
                # Read lines from the file and store them in a list
                lines = file.readlines()
            
            # Return the list of lines
            return lines
        except FileNotFoundError:
            print(f"The file {filename} does not exist.")
            return []
    
    # Example usage
    filename = 'example.txt'
    lines = read_file_to_list(filename)
    
    # Print the list of lines
    for line in lines:
        print(line, end='')  # The end='' avoids adding extra newlines, as each line already has one.
    


.. parsed-literal::

    This is the new text being appended to the file.
    

.. code:: ipython3

    # 77) Write a Python program to read a file line by line store it into a variable.
    
    def read_file_to_variable(filename):
        content = ""  # Initialize an empty string to store the content
        try:
            with open(filename, 'r') as file:
                # Read each line and store it in the variable
                for line in file:
                    content += line  # Append each line to the content variable
            return content
        except FileNotFoundError:
            print(f"The file {filename} does not exist.")
            return ""
    
    # Example usage
    filename = 'example.txt'
    content = read_file_to_variable(filename)
    
    # Print the content of the file
    print(content)
    
    


.. parsed-literal::

    This is the new text being appended to the file.
    
    

.. code:: ipython3

    # 78) Write a python program to find the longest words. 
    
    def find_longest_word(text):
        # Split the text into words (considering spaces as delimiters)
        words = text.split()
        
        # Initialize the longest word as an empty string
        longest_word = ""
        
        # Iterate through the words to find the longest one
        for word in words:
            # Update the longest word if the current word is longer
            if len(word) > len(longest_word):
                longest_word = word
                
        return longest_word
    
    # Example usage
    text = "Python programming is both fun and challenging."
    longest_word = find_longest_word(text)
    
    print("The longest word is:", longest_word)
    


.. parsed-literal::

    The longest word is: challenging.
    

.. code:: ipython3

    # 79) Write a Python program to count the number of lines in a text file. 
    
    def count_lines_in_file(filename):
        try:
            # Open the file in read mode
            with open(filename, 'r') as file:
                # Initialize line count to 0
                line_count = 0
                
                # Iterate through each line in the file
                for line in file:
                    line_count += 1  # Increment the line count for each line
                
            return line_count
        except FileNotFoundError:
            print(f"The file {filename} does not exist.")
            return 0
    
    # Example usage
    filename = 'example.txt'
    num_lines = count_lines_in_file(filename)
    
    # Print the number of lines
    print(f"The number of lines in the file '{filename}' is: {num_lines}")
    


.. parsed-literal::

    The number of lines in the file 'example.txt' is: 1
    

.. code:: ipython3

    # 80) Write a Python program to count the frequency of words in a file. 
    
    from collections import Counter
    import string
    
    def count_word_frequency(filename):
        try:
            # Open the file in read mode
            with open(filename, 'r') as file:
                # Read the entire content of the file
                text = file.read()
                
                # Remove punctuation from the text
                text = text.translate(str.maketrans('', '', string.punctuation))
                
                # Convert the text to lowercase to ensure case-insensitivity
                text = text.lower()
                
                # Split the text into words
                words = text.split()
                
                # Count the frequency of each word using Counter
                word_count = Counter(words)
            
            return word_count
        except FileNotFoundError:
            print(f"The file {filename} does not exist.")
            return {}
    
    # Example usage
    filename = 'example.txt'  # Replace with your filename
    word_frequencies = count_word_frequency(filename)
    
    # Print the word frequencies
    for word, frequency in word_frequencies.items():
        print(f"'{word}': {frequency}")
    
      
    


.. parsed-literal::

    'this': 1
    'is': 1
    'the': 2
    'new': 1
    'text': 1
    'being': 1
    'appended': 1
    'to': 1
    'file': 1
    

.. code:: ipython3

    # 81) Write a Python program to write a list to a file. 
    
    def write_list_to_file(filename, data_list):
        try:
            # Open the file in write mode ('w'), will create or overwrite the file
            with open(filename, 'w') as file:
                # Write each item of the list to the file
                for item in data_list:
                    file.write(f"{item}\n")  # Write each item followed by a newline
            
            print(f"The list has been successfully written to {filename}.")
        except Exception as e:
            print(f"An error occurred: {e}")
    
    # Example usage
    filename = 'output.txt'  # Specify the file name
    data_list = ['apple', 'banana', 'cherry', 'date']  # Example list to write
    
    write_list_to_file(filename, data_list)
    
    


.. parsed-literal::

    The list has been successfully written to output.txt.
    

.. code:: ipython3

    # 82) Write a Python program to copy the contents of a file to another file. 
    
    import shutil
    
    def copy_file_contents(source_filename, destination_filename):
        try:
            # Use shutil to copy the file contents
            shutil.copy(source_filename, destination_filename)
            print(f"Contents of {source_filename} have been copied to {destination_filename}.")
        except FileNotFoundError:
            print(f"The file {source_filename} does not exist.")
        except Exception as e:
            print(f"An error occurred: {e}")
    
    # Example usage
    source_filename = 'source.txt'
    destination_filename = 'destination.txt'
    
    copy_file_contents(source_filename, destination_filename)
    
    


.. parsed-literal::

    The file source.txt does not exist.
    

# 83) Explain Exception handling? What is an Error in Python?

Exception Handling in Python
Exception handling is a mechanism in Python to gracefully handle runtime errors, allowing the program to continue execution or terminate in a controlled way. Instead of the program crashing when an error occurs, you can handle it using try, except, and optionally finally blocks.

Components of Exception Handling:
try block:

The code that might raise an exception is placed inside the try block.
except block:

The code that handles the exception is written in the except block. Different exceptions can be handled by using specific exception types.
else block (optional):

Executes if no exception occurs in the try block.
finally block (optional):

Executes regardless of whether an exception occurs or not, often used for cleanup.

What is an Error in Python?
In Python, an error is a problem in the program that causes it to stop executing. Errors are broadly categorized into two types:

Syntax Errors:

These occur when the Python parser detects incorrect syntax.
Example:
if True
    print("Hello")
(Missing colon in if statement will cause a syntax error.)
Exceptions:

These occur when a syntactically correct program tries to perform an operation that is not allowed.
Example:
print(10 / 0)
(This will raise a ZeroDivisionError.)
Common Types of Exceptions:
ZeroDivisionError: Division by zero.
ValueError: Invalid value for an operation.
TypeError: Operation applied to an object of an inappropriate type.
IndexError: Accessing an invalid index in a sequence.
KeyError: Accessing a non-existent key in a dictionary.
FileNotFoundError: Attempting to access a file that doesn’t exist.
                                                                     

# 84) How many except statements can a try-except block have? Name Some built-in exception classes: 

A try block can have multiple except statements to handle different exceptions. Each except statement can handle a specific exception or a group of exceptions. Python will match the exception raised with the except blocks in the order they appear, and the first match is executed.
Some Built-In Exception Classes in Python
Here’s a list of commonly used built-in exception classes in Python:

BaseException (Parent class for all exceptions)
Exception (Base class for most exceptions derived from BaseException)
ArithmeticError (Base class for arithmetic errors)
ZeroDivisionError: Division or modulo by zero.
OverflowError: Numeric operation exceeds its limit.
FloatingPointError: Issues with floating-point operations.
AttributeError: Accessing an attribute that doesn’t exist.
ImportError: Failure to import a module.
ModuleNotFoundError: A specific subclass of ImportError.
IndexError: Accessing an invalid index in a sequence (e.g., list, tuple).
KeyError: Accessing a non-existent key in a dictionary.
TypeError: Operation applied to an object of an inappropriate type.
ValueError: Operation receives a valid type but an invalid value.
FileNotFoundError: File operation requested on a non-existent file.
IOError: Input/output operation failure.
OSError: Errors related to the operating system.
NameError: Accessing a variable that is not defined.
UnboundLocalError: Referencing a local variable before assignment.
RuntimeError: Generic runtime error.
StopIteration: Raised by iterators to signal the end of iteration.
SyntaxError: Python syntax is invalid.
IndentationError: Incorrect indentation.
TabError: Mixing tabs and spaces.
MemoryError: Memory allocation failure.
RecursionError: Exceeding the maximum recursion depth.

# 85) When will the else part of try-except-else be executed? 

he else part of a try-except-else block is executed only if no exception occurs in the try block. If an exception is raised and caught by any of the except blocks, the else block will not be executed.

Flow of Execution:
try block: The code inside the try block is executed first.
except block: If an exception occurs in the try block, the corresponding except block is executed, and the else block is skipped.
else block: If no exception occurs in the try block, the else block is executed.
finally block (if present): The finally block is executed regardless of whether an exception occurred or not.


# 86) Can one block of except statements handle multiple exception?

Yes, a single except block can handle multiple exceptions in Python. 
This is done by specifying the exceptions in a tuple within the except block. 
If an exception occurs and matches any of the exceptions in the tuple, the corresponding except block will handle it.

In this example:

ValueError occurs if the input is not a valid integer.
ZeroDivisionError occurs if the user enters 0.

Key Points:
The exceptions in the tuple are treated as an OR condition, meaning the block will handle any of the specified exceptions.
The variable (e.g., as e) captures the exception object, which can be used to retrieve details about the error.

# 87) When is the finally block executed? 

The finally block in Python is executed regardless of whether an exception occurred or not in the try block. It is primarily used for cleanup actions, such as closing files, releasing resources, or other necessary final steps.

When Is the finally Block Executed?
No Exception Occurs:

If the code in the try block runs successfully without raising an exception, the finally block is executed after the try block completes.
Exception Is Raised and Handled:

If an exception occurs in the try block and is caught by an except block, the finally block is executed after the except block finishes.
Exception Is Raised but Not Handled:

If an exception occurs in the try block and is not caught by any except block, the finally block is still executed before the program terminates with the uncaught exception.
During return, break, or continue:

If a return, break, or continue statement is encountered in the try or except block, the finally block is executed before the control flow leaves the try block.

# 88) What happens when „1‟== 1 is executed?

When the expression "1" == 1 is executed in Python, it evaluates to False.

Why Does This Happen?
Data Type Mismatch:

"1" is a string, while 1 is an integer.
The == operator checks for both value and type.
Since the types differ (str vs int), Python evaluates the expression as False.
No Implicit Type Conversion:

Python does not automatically convert one data type to another when using ==.
It directly compares the operands' values and types.

.. code:: ipython3

    # 89) How Do You Handle Exceptions with Try/Except/Finally in Python? Explain with coding snippets. 
    
    #In Python, you can handle exceptions using the try, except, and finally blocks. This structure allows you to:
    
    # Write code that might raise an exception in the try block.
    # Handle specific exceptions or general exceptions in the except block(s).
    # Execute cleanup or mandatory actions in the finally block, regardless of whether an exception occurred.
    
    try:
        number = int(input("Enter a number: "))
        result = 10 / number
        print(f"Result: {result}")
    except ZeroDivisionError:
        print("Error: You cannot divide by zero.")
    except ValueError:
        print("Error: Invalid input! Please enter an integer.")
    finally:
        print("Execution completed.")
    


.. parsed-literal::

    Enter a number:  5
    

.. parsed-literal::

    Result: 2.0
    Execution completed.
    

.. code:: ipython3

    # 90) Write python program that user to enter only odd numbers, else will raise an exception.
    
    class NotOddNumberError(Exception):
        """Custom exception for invalid (non-odd) numbers."""
        pass
    
    def enter_odd_number():
        try:
            # Prompt user to enter a number
            number = int(input("Enter an odd number: "))
            
            # Check if the number is even
            if number % 2 == 0:
                raise NotOddNumberError(f"{number} is not an odd number!")
            
            # If valid, print success message
            print(f"Thank you! {number} is an odd number.")
        
        except NotOddNumberError as e:
            print(f"Error: {e}")
        except ValueError:
            print("Error: Invalid input! Please enter a valid integer.")
    
    # Run the program
    enter_odd_number()
    


.. parsed-literal::

    Enter an odd number:  5
    

.. parsed-literal::

    Thank you! 5 is an odd number.
    
