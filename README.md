import math
import datetime

# Function Definitions
def list_operations():
    # Creating a list
    my_list = [1, 2, 3, 4, 5]

    # Append an element to the list
    my_list.append(6)

    # Extend the list with another list
    my_list.extend([7, 8, 9])

    # Insert an element at a specific position
    my_list.insert(0, 0)

    # Remove an element
    my_list.remove(0)

    # Pop an element from the list
    my_list.pop()

    # Clear the list
    my_list.clear()

    # Count the number of occurrences of an element
    count = my_list.count(1)

    # Sort the list
    my_list.sort()

    # Reverse the list
    my_list.reverse()

    print(my_list)

def dictionary_operations():
    # Creating a dictionary
    my_dict = {'a': 1, 'b': 2, 'c': 3}

    # Get the value of a key
    value = my_dict.get('a')

    # Add a key-value pair
    my_dict['d'] = 4

    # Update a value
    my_dict.update({'a': 10})

    # Remove a key-value pair
    del my_dict['a']

    # Get all keys
    keys = my_dict.keys()

    # Get all values
    values = my_dict.values()

    # Get all key-value pairs
    items = my_dict.items()

    # Check if a key exists
    exists = 'a' in my_dict

    # Clear the dictionary
    my_dict.clear()

    print(my_dict)

def tuple_operations():
    # Creating a tuple
    my_tuple = (1, 2, 3, 4, 5)

    # Access an element
    element = my_tuple[0]

    # Get the index of an element
    index = my_tuple.index(1)

    # Count the number of occurrences of an element
    count = my_tuple.count(1)

    # Get the length of the tuple
    length = len(my_tuple)

    # Get the smallest element
    smallest = min(my_tuple)

    # Get the largest element
    largest = max(my_tuple)

    # Convert the tuple to a list
    my_list = list(my_tuple)

    # Convert the list back to a tuple
    my_tuple = tuple(my_list)

    print(my_tuple)

def set_operations():
    # Creating a set
    my_set = {1, 2, 3, 4, 5}

    # Add an element
    my_set.add(6)

    # Remove an element
    my_set.remove(1)

    # Check if an element exists
    exists = 1 in my_set

    # Get the number of elements
    count = len(my_set)

    # Clear the set
    my_set.clear()

    # Union of two sets
    union = my_set.union({6, 7, 8})

    # Intersection of two sets
    intersection = my_set.intersection({2, 3, 4})

    # Difference of two sets
    difference = my_set.difference({2, 3, 4})

    # Symmetric difference of two sets
    sym_difference = my_set.symmetric_difference({2, 3, 4})

    print(my_set)

def check_odd_even(num):
    if num % 2 == 0:
        return "Even"
    else:
        return "Odd"

def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

def simple_interest(p, r, t):
    return (p * r * t) / 100

def compound_interest(p, r, t):
    return p * (1 + r / 100)**t

def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True

def greatest(a, b, c):
    return max(a, b, c)

def concat(s1, s2):
    return s1 + s2

def area_rectangle(length, breadth):
    return length * breadth

def area_square(side):
    return side * side

def area_circle(radius):
    return 3.14 * radius * radius

def first_n_even(n):
    return [i for i in range(2, n*2+1, 2)]

def first_n_odd(n):
    return [i for i in range(1, n*2, 2)]

def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=' ')
        a, b = b, a + b

def volume_cube(side):
    return side ** 3

def volume_cuboid(length, breadth, height):
    return length * breadth * height

def decimal_to_binary(n):
    return bin(n).replace("0b", "")

def binary_to_decimal(b):
    return int(b, 2)

def is_palindrome(n):
    return str(n) == str(n)[::-1]

def count_vowels(s):
    return sum([1 for char in s if char in 'aeiouAEIOU'])

def ascii_value(c):
    return ord(c)

def count_odd_even(n):
    odd = [i for i in range(1, n*2, 2)]
    even = [i for i in range(2, n*2+1, 2)]
    return odd, even

def reverse_string(s):
    return s[::-1]

def is_leap(year):
    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)

def sum_first_n(n):
    return n * (n + 1) // 2

def count_characters(s):
    return len(s)

def swap(a, b):
    a, b = b, a
    return a, b

def add_without_plus(a, b):
    while b != 0:
        carry = a & b
        a = a ^ b
        b = carry << 1
    return a

def last_character(s):
    return s[-1]

def print_vowels(s):
    return [char for char in s if char in 'aeiouAEIOU']

def print_duplicates(s):
    duplicates = [char for char in s if s.count(char) > 1]
    return list(set(duplicates))

def number_pyramid(n):
    for i in range(n):
        print(' ' * (n - i - 1) + str(i+1) * (2*i + 1))

def number_pyramid_2(n):
    for i in range(n):
        print(' ' * (n - i - 1) + ' '.join(map(str, range(1, i+2))) + ' ' + ' '.join(map(str, range(i, 0, -1))))

def star_pyramid(n):
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2*i + 1))

def current_date_time():
    return datetime.datetime.now()

def inverted_pyramid(n):
    for i in range(n, 0, -1):
        print(' ' * (n - i) + '*' * (2*i - 1))

def string_to_chars(s):
    return list(s)

def chars_to_string(chars):
    return ''.join(chars)

def square_root(n):
    return math.sqrt(n)

def cube_root(n):
    return n ** (1/3)

def km_to_miles(km):
    return km * 0.621371

def multiplication_table(n):
    for i in range(1, 11):
        print(f'{n} x {i} = {n*i}')

def alphabet_pyramid(n):
    for i in range(n):
        print(' ' * (n - i - 1) + chr(65+i) * (2*i + 1))

def main():
    while True:
        print("\n1. List operations")
        print("2. Dictionary operations")
        print("3. Tuple operations")
        print("4. Set operations")
        print("5. Check odd-even number")
        print("6. Calculate the factorial of a given number")
        print("7. Calculate the simple interest")
        print("8. Calculate the compound interest")
        print("9. Check if a number is prime")
        print("10. Find the greatest of 3 numbers")
        print("11. Concatenate two strings")
        print("12. Calculate the area of rectangle, square, and circle")
        print("13. Find first n even numbers")
        print("14. Find first n odd numbers")
        print("15. Print Fibonacci series")
        print("16. Calculate the volume of cube and cuboid")
        print("17. Convert decimal number into binary and vice versa")
        print("18. Check if a number is palindrome")
        print("19. Count the vowel in a given string")
        print("20. Find the ASCII value of a given character")
        print("21. Count first n odd and even numbers")
        print("22. Reverse a string")
        print("23. Check if a year is leap or not")
        print("24. Calculate the sum of first n numbers")
        print("25. Calculate the number of characters in a string")
        print("26. Swap two numbers")
        print("27. Sum of two numbers without using arithmetic operator (+)")
        print("28. Print last character of a string")
        print("29. Print vowels in a string")
        print("30. Print duplicate characters from string")
        print("31. Print number pyramid patterns")
        print("32. Print number pyramid patterns")
        print("33. Print star pyramid patterns")
        print("34. Find the current date and time")
        print("35. Print the inverted pyramid")
        print("36. Convert given string to character and characters to string")
        print("37. Calculate square root and cube root of given number")
        print("38. Convert kilometer to miles")
        print("39. Swap two numbers")
        print("40. Print multiplication table of a given number")
        print("41. Print alphabet pyramid patterns")
        print("0. Exit")
        
        choice = int(input("\nEnter your choice: "))
        
        if choice == 1:
            list_operations()
        elif choice == 2:
            dictionary_operations()
        elif choice == 3:
            tuple_operations()
        elif choice == 4:
            set_operations()
        elif choice == 5:
            num = int(input("Enter a number: "))
            print(check_odd_even(num))
        elif choice == 6:
            n = int(input("Enter a number: "))
            print(factorial(n))
        elif choice == 7:
            p = float(input("Enter the principal amount: "))
            r = float(input("Enter the rate of interest: "))
            t = float(input("Enter the time (in years): "))
            print(simple_interest(p, r, t))
        elif choice == 8:
            p = float(input("Enter the principal amount: "))
            r = float(input("Enter the annual interest rate: "))
            t = float(input("Enter the time (in years): "))
            print(compound_interest(p, r, t))
        elif choice == 9:
            n = int(input("Enter a number: "))
            print(is_prime(n))
        elif choice == 10:
            a = int(input("Enter the first number: "))
            b = int(input("Enter the second number: "))
            c = int(input("Enter the third number: "))
            print(greatest(a, b, c))
        elif choice == 11:
            s1 = input("Enter the first string: ")
            s2 = input("Enter the second string: ")
            print(concat(s1, s2))
        elif choice == 12:
            length = float(input("Enter the length of the rectangle: "))
            breadth = float(input("Enter the breadth of the rectangle: "))
            print("Area of the rectangle:", area_rectangle(length, breadth))
            side = float(input("Enter the side of the square: "))
            print("Area of the square:", area_square(side))
            radius = float(input("Enter the radius of the circle: "))
            print("Area of the circle:", area_circle(radius))
        elif choice == 13:
            n = int(input("Enter a number: "))
            print(first_n_even(n))
        elif choice == 14:
            n = int(input("Enter a number: "))
            print(first_n_odd(n))
        elif choice == 15:
            n = int(input("Enter a number: "))
            fibonacci(n)
        elif choice == 16:
            side = float(input("Enter the side of the cube: "))
            print("Volume of the cube:", volume_cube(side))
            length = float(input("Enter the length of the cuboid: "))
            breadth = float(input("Enter the breadth of the cuboid: "))
            height = float(input("Enter the height of the cuboid: "))
            print("Volume of the cuboid:", volume_cuboid(length, breadth, height))
        elif choice == 17:
            n = int(input("Enter a decimal number: "))
            print("Binary representation:", decimal_to_binary(n))
            b = input("Enter a binary number: ")
            print("Decimal representation:", binary_to_decimal(b))
        elif choice == 18:
            n = int(input("Enter a number: "))
            print(is_palindrome(n))
        elif choice == 19:
            s = input("Enter a string: ")
            print("Number of vowels:", count_vowels(s))
        elif choice == 20:
            c = input("Enter a character: ")
            print("ASCII value:", ascii_value(c))
        elif choice == 21:
            n = int(input("Enter a number: "))
            odd, even = count_odd_even(n)
            print("First", n, "odd numbers:", odd)
            print("First", n, "even numbers:", even)
        elif choice == 22:
            s = input("Enter a string: ")
            print("Reversed string:", reverse_string(s))
        elif choice == 23:
            year = int(input("Enter a year: "))
            print(is_leap(year))
        elif choice == 24:
            n = int(input("Enter a number: "))
            print("Sum of first", n, "numbers:", sum_first_n(n))
        elif choice == 25:
            s = input("Enter a string: ")
            print("Number of characters:", count_characters(s))
        elif choice == 26:
            a = int(input("Enter the first number: "))
            b = int(input("Enter the second number: "))
            a, b = swap(a, b)
            print("After swapping:", a, b)
        elif choice == 27:
            a = int(input("Enter the first number: "))
            b = int(input("Enter the second number: "))
            print("Sum:", add_without_plus(a, b))
        elif choice == 28:
            s = input("Enter a string: ")
            print("Last character:", last_character(s))
        elif choice == 29:
            s = input("Enter a string: ")
            print("Vowels:", print_vowels(s))
        elif choice == 30:
            s = input("Enter a string: ")
            print("Duplicate characters:", print_duplicates(s))
        elif choice == 31:
            n = int(input("Enter a number: "))
            number_pyramid(n)
        elif choice == 32:
            n = int(input("Enter a number: "))
            number_pyramid_2(n)
        elif choice == 33:
            n = int(input("Enter a number: "))
            star_pyramid(n)
        elif choice == 34:
            print("Current date and time:", current_date_time())
        elif choice == 35:
            n = int(input("Enter a number: "))
            inverted_pyramid(n)
        elif choice == 36:
            s = input("Enter a string: ")
            print("Characters:", string_to_chars(s))
            chars = input("Enter characters separated by space: ").split()
            print("String:", chars_to_string(chars))
        elif choice == 37:
            n = float(input("Enter a number: "))
            print("Square root:", square_root(n))
            print("Cube root:", cube_root(n))
        elif choice == 38:
            km = float(input("Enter distance in kilometers: "))
            print("Distance in miles:", km_to_miles(km))
        elif choice == 39:
            a = int(input("Enter the first number: "))
            b = int(input("Enter the second number: "))
            a, b = swap(a, b)
            print("After swapping:", a, b)
        elif choice == 40:
            n = int(input("Enter a number: "))
            multiplication_table(n)
        elif choice == 41:
            n = int(input("Enter a number: "))
            alphabet_pyramid(n)
        elif choice == 0:
            break
        else:
            print("Invalid choice. Please try again.")


