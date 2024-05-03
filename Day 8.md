### Intro to Python

| Feature            | Description                                                                                                                                                          |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inventor          | Guido van Rossum, a Dutch programmer, created Python in the late 1980s. He named the language after the British comedy show "Monty Python's Flying Circus," showing his appreciation for its humor and to make the name memorable. |
| BDFL              | Guido van Rossum was affectionately known as Python's "Benevolent Dictator For Life" (BDFL) due to his influential leadership and decision-making role in the Python community.                                                 |
| High-level        | Python is designed to be easy to read and write, with a syntax that resembles natural language, making it accessible to beginners and experts alike.              |
| Interpreted        | Python code is executed line by line by an interpreter, which means you can run your code without needing to compile it first, making the development process faster.  |
| General-purpose   | Python is a versatile language that can be used for a wide range of applications, including web development, data analysis, scientific computing, automation, and more. |
| Dynamically-typed | Python is dynamically-typed, meaning you don't need to declare the type of a variable explicitly. Instead, Python infers the type of variables based on the assigned value. |
| Object-oriented   | Python supports object-oriented programming paradigms, allowing developers to create classes and objects, encapsulate data, and implement inheritance and polymorphism. |
| Extensive libraries | Python has a vast ecosystem of libraries and frameworks that provide pre-written code for various tasks, saving time and effort in development.                           |
| Community-driven  | Python has a large and active community of developers who contribute to its growth and provide support through forums, tutorials, and open-source projects.                |
| Portable          | Python code can run on different operating systems, including Windows, macOS, and Linux, making it portable and platform-independent.                                     |
| Scalable          | Python is scalable, meaning it can be used for small scripts as well as large-scale applications, thanks to its performance optimizations and support for parallelism.       |
| Language Diversity | Despite Python's popularity and versatility, other programming languages exist to address specific needs, preferences, and technical requirements. Different languages may offer better performance, lower-level system access, stronger static typing, or specialized domain-specific features. Additionally, historical factors, community preferences, and evolving technology trends contribute to the continued development and adoption of new programming languages. |


### Python's design philosophy

| Design Philosophy Point  | Main Description                                                                                                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Successor to ABC Language | Python aimed to build upon the ideas of the ABC language, aiming to appeal to Unix/C hackers by providing a language that is both powerful and easy to use.                   |
| Readability and Simplicity ("Pythonic" code) | Python prioritizes readability and simplicity in code, encouraging developers to write code that is easy to understand and maintain. This philosophy is sometimes referred to as writing "Pythonic" code. |
| Concise Syntax            | Python's syntax allows developers to express concepts in fewer lines of code compared to other languages. This leads to more concise and expressive programs, improving readability and reducing complexity.                 |

These points encapsulate Guido van Rossum's vision for Python and highlight its key principles of simplicity, readability, and expressiveness.

### Milestone

| Milestone                           | Description                                                                                                                                                                                                                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Python 2.0 (2000)                  | Introduced list comprehensions and garbage collection (GC).                                                                                                                                                                                                                                              |
| Python 3 (2008)                    | Major revision with emphasis on Unicode support, not fully backward compatible with Python 2.                                                                                                                                                                                                              |

**Python 2.0 (2000)**
- *Introduced list comprehensions*: List comprehensions provide a concise and expressive way to create lists in Python. Instead of writing multiple lines of code to create and populate a list, developers can use a single line of code, improving readability and reducing code verbosity.
- *Garbage collection (GC)*: Garbage collection is a memory management technique that automatically deallocates memory that is no longer in use, preventing memory leaks and improving overall memory efficiency. Python 2.0 introduced garbage collection to automate memory management tasks, reducing the burden on developers and improving the reliability of Python programs.

**Python 3 (2008)**
- *Major revision*: Python 3 was a significant update to the language, addressing various design flaws and inconsistencies present in Python 2. It introduced several new features and improvements aimed at making Python a more robust and modern programming language.
- *Emphasis on Unicode support*: Python 3 placed a strong emphasis on Unicode support, making it easier to work with international text and characters. Unicode support ensures that Python can handle a wide range of characters and symbols from different languages and writing systems, improving compatibility and usability for global audiences.
- *Not fully backward compatible with Python 2*: While Python 3 brought many enhancements, it also introduced changes that were not backward compatible with Python 2. This meant that existing Python 2 codebases required modifications to work with Python 3, leading to challenges and slower adoption initially. However, the benefits of Python 3, such as improved Unicode support and language consistency, ultimately outweighed the migration challenges, leading to widespread adoption over time.


### Python 3 Transition

| Transition Stage       | Description                                                                                                                                                                                                                                                |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Addressing Design Flaws and Enhancements | - Python 3 addressed fundamental design flaws in Python 2. <br>- Introduced improvements and new features. <br>- Emphasized Unicode support for better handling of international text. <br>- Enhanced syntax and language refinements for improved readability and maintainability. |
| Community Adoption     | - Transition to Python 3 was gradual. <br>- Community gradually embraced Python 3 supported by its enhancements. <br>- Active contribution from the Python community to update libraries and frameworks for Python 3 compatibility.                                        |
| Official End of Python 2 Support       | - Python 2 support officially ended in 2020. <br>- Deadline accelerated migration to Python 3. <br>- Developers encouraged to update codebases for continued updates, security patches, and community support.                                                           |

These points succinctly describe the Python 3 transition process, covering the reasons for transition, community involvement, and the impact of the official end of Python 2 support.

### Differences between declaration and assignment

| Aspect        | Declaration                                                                                                                                                                    | Assignment                                                                                                                                |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Definition    | Declaration introduces the existence of a variable to the compiler/interpreter without allocating memory or assigning a value.                                               | Assignment assigns a value to a variable, allocating memory if necessary.                                                                |
| Example       | ```python int num;``` (declares a variable named "num" of type integer in languages like C/C++)                                                                                | ```python num = 10;``` (assigns the value 10 to the variable "num" in Python)                                                            |
| Purpose       | Allows the compiler/interpreter to recognize the variable's name and type for subsequent use in the program.                                                                  | Assigns a value to a variable, allowing it to hold data that can be manipulated or referenced throughout the program.                    |
| Memory Usage  | Does not allocate memory.                                                                                                                                                      | Allocates memory to store the assigned value.                                                                                            |
| Usage         | Necessary in statically-typed languages like C/C++ where variable types must be explicitly declared before use. Not required in dynamically-typed languages like Python. | Essential in all programming languages to store data and perform operations on variables.                                               |

### Type conversion with examples for different data types:

| Data Type          | Example                              | Description                                                                                                                                                      |
|--------------------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer to Float  | `int_num = 10`<br>`float_num = float(int_num)` | Converts an integer to a floating-point number, preserving the integer value and adding a decimal point.                                                      |
| Float to Integer  | `float_num = 10.5`<br>`int_num = int(float_num)` | Converts a floating-point number to an integer, truncating the decimal part and keeping only the integer portion.                                             |
| Integer to String | `int_num = 10`<br>`str_num = str(int_num)`     | Converts an integer to a string, representing the numerical value as a sequence of characters.                                                                |
| Float to String   | `float_num = 10.5`<br>`str_num = str(float_num)` | Converts a floating-point number to a string, representing the numerical value as a sequence of characters.                                                  |
| String to Integer | `str_num = "10"`<br>`int_num = int(str_num)`     | Converts a string containing digits to an integer, extracting and converting the numerical value represented by the characters.                                |
| String to Float   | `str_num = "10.5"`<br>`float_num = float(str_num)` | Converts a string representing a floating-point number to a float, extracting and converting the numerical value represented by the characters, including the decimal point. |
| Boolean to Integer | `bool_val = True`<br>`int_val = int(bool_val)`   | Converts a boolean value to an integer, where `True` is converted to `1` and `False` is converted to `0`.                                                     |
| Integer to Boolean | `int_val = 1`<br>`bool_val = bool(int_val)`     | Converts an integer to a boolean value, where `0` is converted to `False`, and any non-zero value is converted to `True`.                                      |

These examples demonstrate how different data types can be converted to one another in Python. Type conversion is a common operation in programming, allowing flexibility and compatibility between different types of data.

### Difference between implicit and explicit type conversion

**Implicit Type Conversion:**

In implicit type conversion, the Python interpreter automatically converts one data type to another when required. This conversion occurs when data types are compatible, and one type can be safely promoted to another without losing information.

| Conversion Type          | Description                                                                                                                                                        | Example                                                                                                                                                     |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Float to Integer        | Converts a floating-point number to an integer by truncating the decimal part.                                                                                     | `float_num = 10.5`<br>`int_num = float_num`<br>`print(int_num)`<br>Output: `10`                                                                         |
| Integer to Float        | Converts an integer to a floating-point number, adding a decimal point to represent the fractional part.                                                           | `int_num = 10`<br>`float_num = int_num`<br>`print(float_num)`<br>Output: `10.0`                                                                       |
| String to Integer/Float | Converts a string representing a numerical value to an integer or a float.                                                                                         | `num_str = "10"`<br>`num_int = num_str`<br>`num_float = num_str`<br>`print(num_int)`<br>Output: `10`<br>`print(num_float)`<br>Output: `10.0` |
| Boolean to Integer/Float | Converts a boolean value (`True` or `False`) to an integer or a float, where `True` is converted to `1` and `False` is converted to `0`.                             | `bool_val = True`<br>`int_val = bool_val`<br>`float_val = bool_val`<br>`print(int_val)`<br>Output: `1`<br>`print(float_val)`<br>Output: `1.0` |

**Explicit Type Conversion (Type Casting):**

In explicit type conversion, the user explicitly converts the data type of an object to the required data type using predefined functions like `int()`, `float()`, `str()`, etc.

| Conversion Type          | Description                                                                                                                                                 | Example                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| String to Integer/Float | Converts a string representing a numerical value to an integer or a float using predefined functions like `int()` or `float()`.                              | `num_str = "10"`<br>`num_int = int(num_str)`<br>`num_float = float(num_str)`<br>`print(num_int)`<br>Output: `10`<br>`print(num_float)`<br>Output: `10.0` |
| Integer/Float to String | Converts an integer or a float to a string using predefined function `str()`.                                                                               | `int_num = 10`<br>`float_num = 10.5`<br>`str_num_int = str(int_num)`<br>`str_num_float = str(float_num)`<br>`print(str_num_int)`<br>Output: `"10"`<br>`print(str_num_float)`<br>Output: `"10.5"` |
| Boolean to Integer/Float | Converts a boolean value (`True` or `False`) to an integer or a float explicitly using `int()` or `float()` functions.                           | `bool_val = True`<br>`int_val = int(bool_val)`<br>`float_val = float(bool_val)`<br>`print(int_val)`<br>Output: `1`<br>`print(float_val)`<br>Output: `1.0` |


### Rules and Best Practices for Naming Variables in Python

1. Start with a letter or an underscore (`_`).
2. No reserved keywords or built-in function names.
3. No spaces; use underscores (`_`), camelCase, or snake_case.
4. Use descriptive names for better code readability.
5. Use lowercase letters and snake_case for variable names.
6. Maintain consistency throughout the code.
7. Avoid shadowing built-in functions.
8. Strike a balance between short and long names.


### Operators that yield Boolean results in Python

#### Comparison Operators
- `==` (equal to)
- `!=` (not equal to)
- `>` (greater than)
- `<` (less than)
- `>=` (greater than or equal to)
- `<=` (less than or equal to)

#### Logical Operators
- `and` (returns True if both conditions are True)
- `or` (returns True if either condition is True)
- `not` (negates a Boolean expression)

#### Identity Operators
- `is` (returns True if both variables refer to the same object)
- `is not` (returns True if the variables refer to different objects)

#### Membership Operators
- `in` (returns True if the value is found in the sequence)
- `not in` (returns True if the value is not found in the sequence)
