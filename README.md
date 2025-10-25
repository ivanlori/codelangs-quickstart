# Programming Languages Quickstart Guide

A comprehensive collection of quickstart guides for various programming languages. Each section provides essential syntax, concepts, and examples to help you get up and running quickly with different programming languages.

## Table of Contents

### Languages

- [JavaScript](#javascript)
- [Python](#python)
- [C++](#c++)

### JavaScript Sections

- [Variables](#variables)
- [Data Types](#data-types)
- [Functions](#functions)
- [Control Flow](#control-flow)
- [Arrays](#arrays)
- [Objects](#objects)
- [Events](#events)

### Python Sections

- [Python](#python)
- [Python Variables](#python-variables)
- [Python Data Types](#python-data-types)
- [Python Functions](#python-functions)
- [Python Control Flow](#python-control-flow)
- [Python Collections](#python-collections)
- [Python Classes](#python-classes)
- [Python Exception Handling](#python-exception-handling)
- [Python Comprehensions](#python-comprehensions)

### C++ Sections

- [C++](#c++)
- [C++ Variables](#c-variables)
- [C++ Data Types](#c-data-types)
- [C++ Functions](#c-functions)
- [C++ Control Flow](#c-control-flow)
- [C++ Arrays and Vectors](#c-arrays-and-vectors)
- [C++ Classes](#c-classes)
- [C++ Pointers and References](#c-pointers-and-references)
- [C++ Exception Handling](#c-exception-handling)
- [C++ STL Containers](#c-stl-containers)

---

## JavaScript

Essential JavaScript syntax and concepts to get you started quickly.

## Variables

```javascript
// Three ways to declare variables
var oldWay = "avoid using var";
let changeable = "can be reassigned";
const constant = "cannot be reassigned";

// Block scope with let and const
let name = "John";
const age = 30;
```

## Data Types

```javascript
// Primitive types
let string = "Hello World";
let number = 42;
let boolean = true;
let nullValue = null;
let undefinedValue = undefined;
let symbol = Symbol("id");

// Check type
console.log(typeof string); // "string"
console.log(typeof number); // "number"
```

## Functions

```javascript
// Function declaration
function greet(name) {
  return `Hello, ${name}!`;
}

// Function expression
const add = function (a, b) {
  return a + b;
};

// Arrow function (ES6+)
const multiply = (a, b) => a * b;

// Arrow function with block
const divide = (a, b) => {
  if (b === 0) return "Cannot divide by zero";
  return a / b;
};

// Usage
console.log(greet("Alice")); // "Hello, Alice!"
console.log(add(5, 3)); // 8
```

## Control Flow

```javascript
// If/else
let score = 85;
if (score >= 90) {
  console.log("A grade");
} else if (score >= 80) {
  console.log("B grade");
} else {
  console.log("Keep studying");
}

// Ternary operator
const message = score >= 80 ? "Pass" : "Fail";

// Switch statement
const day = "Monday";
switch (day) {
  case "Monday":
    console.log("Start of work week");
    break;
  case "Friday":
    console.log("TGIF!");
    break;
  default:
    console.log("Regular day");
}

// Loops
for (let i = 0; i < 5; i++) {
  console.log(i);
}

let count = 0;
while (count < 3) {
  console.log(count);
  count++;
}
```

## Arrays

```javascript
// Creating arrays
const fruits = ["apple", "banana", "orange"];
const numbers = [1, 2, 3, 4, 5];

// Common methods
fruits.push("grape"); // Add to end
fruits.pop(); // Remove from end
fruits.unshift("mango"); // Add to beginning
fruits.shift(); // Remove from beginning

// Array methods
const doubled = numbers.map((n) => n * 2);
const evens = numbers.filter((n) => n % 2 === 0);
const sum = numbers.reduce((acc, n) => acc + n, 0);

// Iteration
fruits.forEach((fruit) => console.log(fruit));

for (const fruit of fruits) {
  console.log(fruit);
}
```

## Objects

```javascript
// Object literal
const person = {
  name: "Alice",
  age: 30,
  city: "New York",
  greet: function () {
    return `Hello, I'm ${this.name}`;
  },
};

// Accessing properties
console.log(person.name); // Dot notation
console.log(person["age"]); // Bracket notation

// Adding/modifying properties
person.email = "alice@email.com";
person.age = 31;

// Destructuring
const { name, age } = person;
console.log(name, age);

// Object methods
const keys = Object.keys(person);
const values = Object.values(person);
```

## Events

```javascript
// Adding event listeners
const button = document.querySelector("#myButton");

button.addEventListener("click", function (event) {
  console.log("Button clicked!");
  event.preventDefault(); // Prevent default behavior
});

// Arrow function event handler
button.addEventListener("click", (e) => {
  console.log("Clicked!", e.target);
});

// Common events: click, mouseover, keydown, submit, load
document.addEventListener("DOMContentLoaded", function () {
  console.log("Page loaded");
});
```

## Python

Essential Python syntax and concepts to get you started quickly.

### Python Variables

```python
# Variables are dynamically typed
name = "Alice"
age = 30

# Variables can change type
count = 0
count = "zero"

# Constants (by convention, use ALL_CAPS)
MAX_SIZE = 1000
PI = 3.14159

# Type hints (optional but recommended)
number: int = 42
pi: float = 3.14159
```

### Python Data Types

```python
# Basic types
integer = 42                    # int
float_num = 3.14               # float
boolean = True                 # bool
string = "Hello World"         # str
none_value = None              # NoneType

# Complex types
complex_num = 3 + 4j           # complex

# Collections
my_list = [1, 2, 3, 4, 5]      # list
my_tuple = (1, 2, 3)           # tuple (immutable)
my_set = {1, 2, 3}             # set (unique values)
my_dict = {"key": "value"}     # dict

# Type checking
print(type(integer))           # <class 'int'>
print(isinstance(integer, int)) # True

# Tuple unpacking
x, y, z = my_tuple
first = my_list[0]
```

### Python Functions

```python
# Basic function
def greet(name):
    print(f"Hello, {name}!")

# Function with return value
def add(a, b):
    return a + b

# Function with type hints
def multiply(a: int, b: int) -> int:
    return a * b

# Default parameters
def greet_with_title(name, title="Mr."):
    return f"Hello, {title} {name}!"

# Variable arguments
def sum_all(*args):
    return sum(args)

# Keyword arguments
def create_user(**kwargs):
    return kwargs

# Lambda functions
square = lambda x: x * x
add_lambda = lambda a, b: a + b

# Usage
greet("Alice")
result = add(5, 3)
print(sum_all(1, 2, 3, 4))  # 10
user = create_user(name="Alice", age=30)
```

### Python Control Flow

```python
# If statements
number = 6
if number % 2 == 0:
    print("Even")
else:
    print("Odd")

# Elif
score = 85
if score >= 90:
    print("A grade")
elif score >= 80:
    print("B grade")
else:
    print("Keep studying")

# Ternary operator
message = "Pass" if score >= 80 else "Fail"

# For loops
for i in range(5):
    print(i)

# Iterate over collections
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)

for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")

# While loop
count = 0
while count < 3:
    print(count)
    count += 1

# List comprehensions
squares = [x**2 for x in range(5)]
evens = [x for x in range(10) if x % 2 == 0]
```

### Python Collections

```python
# Lists (mutable, ordered)
fruits = ["apple", "banana", "orange"]
fruits.append("grape")          # Add to end
fruits.insert(0, "mango")       # Insert at index
fruits.remove("banana")         # Remove by value
popped = fruits.pop()           # Remove and return last

# List slicing
first_two = fruits[:2]
last_two = fruits[-2:]
reversed_list = fruits[::-1]

# Dictionaries
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

# Dictionary operations
person["email"] = "alice@email.com"  # Add/update
age = person.get("age", 0)           # Get with default
keys = person.keys()
values = person.values()
items = person.items()

# Sets (unique, unordered)
numbers = {1, 2, 3, 4, 5}
numbers.add(6)
numbers.discard(3)

# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2          # {1, 2, 3, 4, 5}
intersection = set1 & set2   # {3}
difference = set1 - set2     # {1, 2}

# Tuples (immutable, ordered)
coordinates = (10, 20)
x, y = coordinates  # Unpacking
```

### Python Classes

```python
# Define a class
class User:
    # Class variable
    user_count = 0
    
    def __init__(self, username, email):
        self.username = username
        self.email = email
        self.active = True
        self.sign_in_count = 1
        User.user_count += 1
    
    # Instance method
    def greet(self):
        return f"Hello, I'm {self.username}"
    
    def is_active(self):
        return self.active
    
    # Class method
    @classmethod
    def get_user_count(cls):
        return cls.user_count
    
    # Static method
    @staticmethod
    def validate_email(email):
        return "@" in email
    
    # String representation
    def __str__(self):
        return f"User({self.username}, {self.email})"

# Create instances
user1 = User("alice", "alice@email.com")
user2 = User("bob", "bob@email.com")

# Use methods
print(user1.greet())
print(User.get_user_count())  # 2

# Inheritance
class AdminUser(User):
    def __init__(self, username, email, permissions):
        super().__init__(username, email)
        self.permissions = permissions
    
    def grant_permission(self, permission):
        self.permissions.append(permission)

admin = AdminUser("admin", "admin@email.com", ["read", "write"])
```

### Python Exception Handling

```python
# Basic try-except
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")

# Multiple exceptions
try:
    number = int(input("Enter a number: "))
    result = 10 / number
except ValueError:
    print("Invalid number format")
except ZeroDivisionError:
    print("Cannot divide by zero")
except Exception as e:
    print(f"Unexpected error: {e}")
else:
    print(f"Result: {result}")
finally:
    print("Cleanup code here")

# Raising exceptions
def validate_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative")
    if age > 150:
        raise ValueError("Age seems unrealistic")
    return age

# Custom exceptions
class CustomError(Exception):
    def __init__(self, message):
        self.message = message
        super().__init__(self.message)

# File handling with context manager
try:
    with open("file.txt", "r") as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print("File not found")
```

### Python Comprehensions

```python
# List comprehensions
squares = [x**2 for x in range(10)]
evens = [x for x in range(20) if x % 2 == 0]
words = ["hello", "world", "python"]
lengths = [len(word) for word in words]

# Nested comprehensions
matrix = [[i*j for j in range(3)] for i in range(3)]

# Dictionary comprehensions
word_lengths = {word: len(word) for word in words}
squared_dict = {x: x**2 for x in range(5)}

# Set comprehensions
unique_lengths = {len(word) for word in words}

# Generator expressions (memory efficient)
squares_gen = (x**2 for x in range(1000000))  # Lazy evaluation
sum_squares = sum(x**2 for x in range(100))

# Conditional comprehensions
positive_squares = [x**2 for x in range(-5, 6) if x > 0]
categorized = ["even" if x % 2 == 0 else "odd" for x in range(10)]
```

---

## C++

Essential C++ syntax and concepts to get you started quickly.

### C++ Variables

```cpp
#include <iostream>

// Variables with explicit types
int age = 30;
double pi = 3.14159;
char letter = 'A';
bool is_active = true;

// Constants
const int MAX_SIZE = 1000;
constexpr double E = 2.71828;  // Compile-time constant

// Auto type deduction (C++11+)
auto number = 42;        // int
auto price = 19.99;      // double
auto name = "Alice";     // const char*

// References (aliases)
int original = 10;
int& ref = original;     // ref is an alias for original

// Pointers
int* ptr = &original;    // ptr points to original
int value = *ptr;        // Dereference pointer
```

### C++ Data Types

```cpp
// Fundamental types
int integer = 42;                  // Usually 32-bit
long long big_int = 1234567890LL;  // 64-bit
float float_num = 3.14f;           // 32-bit float
double double_num = 3.14159;       // 64-bit float
char character = 'X';              // Single character
bool flag = true;                  // Boolean

// Strings (C++98+)
#include <string>
std::string text = "Hello World";
std::string name("Alice");

// Arrays
int numbers[5] = {1, 2, 3, 4, 5};
int matrix[3][3] = {{1,2,3}, {4,5,6}, {7,8,9}};

// Modern arrays (C++11+)
#include <array>
std::array<int, 5> modern_array = {1, 2, 3, 4, 5};

// Type checking
#include <typeinfo>
std::cout << typeid(integer).name() << std::endl;

// Structured bindings (C++17+)
auto [x, y] = std::make_pair(10, 20);
```

### C++ Functions

```cpp
#include <iostream>

// Basic function
void greet(const std::string& name) {
    std::cout << "Hello, " << name << "!" << std::endl;
}

// Function with return value
int add(int a, int b) {
    return a + b;
}

// Function overloading
int multiply(int a, int b) {
    return a * b;
}

double multiply(double a, double b) {
    return a * b;
}

// Default parameters
void greet_with_title(const std::string& name, const std::string& title = "Mr.") {
    std::cout << "Hello, " << title << " " << name << "!" << std::endl;
}

// Pass by reference
void increment(int& value) {
    value++;
}

// Function templates
template<typename T>
T maximum(T a, T b) {
    return (a > b) ? a : b;
}

// Lambda functions (C++11+)
auto square = [](int x) { return x * x; };
auto add_lambda = [](int a, int b) -> int { return a + b; };

// Usage
greet("Alice");
int result = add(5, 3);
int num = 5;
increment(num);  // num becomes 6
int max_val = maximum(10, 20);
```

### C++ Control Flow

```cpp
// If statements
int number = 6;
if (number % 2 == 0) {
    std::cout << "Even" << std::endl;
} else {
    std::cout << "Odd" << std::endl;
}

// Switch statement
char grade = 'B';
switch (grade) {
    case 'A':
        std::cout << "Excellent!" << std::endl;
        break;
    case 'B':
        std::cout << "Good job!" << std::endl;
        break;
    default:
        std::cout << "Keep studying!" << std::endl;
}

// For loops
for (int i = 0; i < 5; i++) {
    std::cout << i << " ";
}

// Range-based for loop (C++11+)
int numbers[] = {1, 2, 3, 4, 5};
for (const auto& num : numbers) {
    std::cout << num << " ";
}

// While loop
int count = 0;
while (count < 3) {
    std::cout << count << std::endl;
    count++;
}

// Do-while loop
int x = 0;
do {
    std::cout << x << std::endl;
    x++;
} while (x < 3);
```

### C++ Arrays and Vectors

```cpp
#include <vector>
#include <iostream>

// Traditional arrays
int static_array[5] = {1, 2, 3, 4, 5};
static_array[0] = 10;  // Modify element

// Vectors (dynamic arrays)
std::vector<int> numbers = {1, 2, 3, 4, 5};
numbers.push_back(6);           // Add to end
numbers.pop_back();             // Remove from end
numbers.insert(numbers.begin(), 0); // Insert at beginning

// Vector operations
std::cout << "Size: " << numbers.size() << std::endl;
std::cout << "First: " << numbers.front() << std::endl;
std::cout << "Last: " << numbers.back() << std::endl;

// Iterating
for (size_t i = 0; i < numbers.size(); i++) {
    std::cout << numbers[i] << " ";
}

// Range-based iteration
for (const auto& num : numbers) {
    std::cout << num << " ";
}

// Iterator-based iteration
for (auto it = numbers.begin(); it != numbers.end(); ++it) {
    std::cout << *it << " ";
}

// Multi-dimensional vectors
std::vector<std::vector<int>> matrix(3, std::vector<int>(3, 0));
matrix[1][1] = 5;
```

### C++ Classes

```cpp
#include <string>
#include <iostream>

class User {
private:
    std::string username;
    std::string email;
    bool active;
    static int user_count;  // Class variable

public:
    // Constructor
    User(const std::string& username, const std::string& email) 
        : username(username), email(email), active(true) {
        user_count++;
    }
    
    // Copy constructor
    User(const User& other) 
        : username(other.username), email(other.email), active(other.active) {
        user_count++;
    }
    
    // Destructor
    ~User() {
        user_count--;
    }
    
    // Getter methods
    const std::string& getUsername() const { return username; }
    const std::string& getEmail() const { return email; }
    bool isActive() const { return active; }
    
    // Setter methods
    void setActive(bool status) { active = status; }
    
    // Member function
    void greet() const {
        std::cout << "Hello, I'm " << username << std::endl;
    }
    
    // Static method
    static int getUserCount() {
        return user_count;
    }
};

// Initialize static member
int User::user_count = 0;

// Inheritance
class AdminUser : public User {
private:
    std::vector<std::string> permissions;
    
public:
    AdminUser(const std::string& username, const std::string& email)
        : User(username, email) {
        permissions.push_back("read");
        permissions.push_back("write");
    }
    
    void grantPermission(const std::string& permission) {
        permissions.push_back(permission);
    }
    
    // Override base class method
    void greet() const override {
        std::cout << "Hello, I'm admin " << getUsername() << std::endl;
    }
};

// Usage
User user1("alice", "alice@email.com");
AdminUser admin("admin", "admin@email.com");
user1.greet();
std::cout << "Total users: " << User::getUserCount() << std::endl;
```

### C++ Pointers and References

```cpp
#include <memory>

// Raw pointers
int value = 42;
int* ptr = &value;        // Pointer to value
int deref = *ptr;         // Dereference pointer
*ptr = 50;                // Modify through pointer

// Pointer arithmetic
int array[5] = {1, 2, 3, 4, 5};
int* array_ptr = array;   // Points to first element
int second = *(array_ptr + 1);  // Access second element

// References (aliases)
int original = 10;
int& ref = original;      // ref is an alias for original
ref = 20;                 // original is now 20

// Smart pointers (C++11+)
// Unique pointer (exclusive ownership)
std::unique_ptr<int> unique_ptr = std::make_unique<int>(42);
int unique_value = *unique_ptr;

// Shared pointer (shared ownership)
std::shared_ptr<int> shared_ptr1 = std::make_shared<int>(42);
std::shared_ptr<int> shared_ptr2 = shared_ptr1;  // Shared ownership

// Weak pointer (non-owning reference)
std::weak_ptr<int> weak_ptr = shared_ptr1;

// Dynamic memory allocation (avoid if possible)
int* dynamic_array = new int[10];
// ... use array ...
delete[] dynamic_array;  // Don't forget to free memory!

// Better: use containers or smart pointers instead
std::vector<int> safe_array(10);  // Automatically managed
```

### C++ Exception Handling

```cpp
#include <stdexcept>
#include <iostream>

// Basic try-catch
try {
    int result = 10 / 0;  // This won't throw in C++, but let's pretend
} catch (const std::exception& e) {
    std::cout << "Exception: " << e.what() << std::endl;
}

// Multiple catch blocks
void risky_function(int value) {
    if (value < 0) {
        throw std::invalid_argument("Negative value not allowed");
    }
    if (value == 0) {
        throw std::runtime_error("Zero value causes problems");
    }
}

try {
    risky_function(-1);
} catch (const std::invalid_argument& e) {
    std::cout << "Invalid argument: " << e.what() << std::endl;
} catch (const std::runtime_error& e) {
    std::cout << "Runtime error: " << e.what() << std::endl;
} catch (const std::exception& e) {
    std::cout << "General exception: " << e.what() << std::endl;
} catch (...) {
    std::cout << "Unknown exception caught" << std::endl;
}

// Custom exception class
class CustomException : public std::exception {
private:
    std::string message;
public:
    CustomException(const std::string& msg) : message(msg) {}
    
    const char* what() const noexcept override {
        return message.c_str();
    }
};

// RAII (Resource Acquisition Is Initialization)
class FileHandler {
private:
    FILE* file;
public:
    FileHandler(const std::string& filename) {
        file = fopen(filename.c_str(), "r");
        if (!file) {
            throw std::runtime_error("Cannot open file");
        }
    }
    
    ~FileHandler() {
        if (file) {
            fclose(file);
        }
    }
    
    // Disable copy to prevent double deletion
    FileHandler(const FileHandler&) = delete;
    FileHandler& operator=(const FileHandler&) = delete;
};
```

### C++ STL Containers

```cpp
#include <vector>
#include <map>
#include <set>
#include <queue>
#include <stack>
#include <algorithm>

// Vector (dynamic array)
std::vector<int> numbers = {1, 2, 3, 4, 5};
numbers.push_back(6);
numbers.erase(numbers.begin());  // Remove first element

// Map (key-value pairs, ordered)
std::map<std::string, int> scores;
scores["Alice"] = 95;
scores["Bob"] = 87;
scores.insert({"Charlie", 92});

for (const auto& pair : scores) {
    std::cout << pair.first << ": " << pair.second << std::endl;
}

// Unordered map (hash table, C++11+)
#include <unordered_map>
std::unordered_map<std::string, int> fast_scores;
fast_scores["Alice"] = 95;

// Set (unique elements, ordered)
std::set<int> unique_numbers = {1, 2, 3, 2, 1};  // Will contain {1, 2, 3}
unique_numbers.insert(4);

// Queue (FIFO)
std::queue<int> q;
q.push(1);
q.push(2);
int front = q.front();  // 1
q.pop();

// Stack (LIFO)
std::stack<int> s;
s.push(1);
s.push(2);
int top = s.top();      // 2
s.pop();

// Priority queue (max heap by default)
std::priority_queue<int> pq;
pq.push(3);
pq.push(1);
pq.push(4);
int max_val = pq.top(); // 4

// Algorithms
std::vector<int> data = {3, 1, 4, 1, 5, 9, 2, 6};

// Sort
std::sort(data.begin(), data.end());

// Find
auto it = std::find(data.begin(), data.end(), 4);
if (it != data.end()) {
    std::cout << "Found 4 at position " << (it - data.begin()) << std::endl;
}

// Count
int count_ones = std::count(data.begin(), data.end(), 1);

// Transform
std::vector<int> squares(data.size());
std::transform(data.begin(), data.end(), squares.begin(), [](int x) { return x * x; });
```
