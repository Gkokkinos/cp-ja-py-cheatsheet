# C++ / Java / Python - Quick Syntax Reference

Personal cheatsheet for Java, C++ and Python as I swap between these languages often.

---

## Table of Contents

1. [Variables & Types](#variables--types)
2. [Operators](#operators)
3. [Control Flow](#control-flow)
4. [Loops](#loops)
5. [Functions / Methods](#functions--methods)
6. [Classes & OOP](#classes--oop)
7. [References & Pointers](#references--pointers)
8. [Collections](#collections)
9. [Strings](#strings)
10. [I/O](#io)
11. [Error Handling](#error-handling)

---

## Variables & Types

### Declaration & Typing
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Typing | Static | Static | Dynamic |
| Type hints | `auto x = 5;` | `var x = 5;` | `x: int = 5` |

```cpp
// C++
int age = 25;
float price = 19.99f;
double pi = 3.14159;
char grade = 'A';
bool isValid = true;
const int MAX = 100;
```

```java
// Java
int age = 25;
float price = 19.99f;
double pi = 3.14159;
char grade = 'A';
boolean isValid = true;
final int MAX = 100;
```

```python
# Python
age = 25
price = 19.99
pi = 3.14159
grade = 'A'
is_valid = True
MAX = 100
```

### Null / None
| Language | Syntax |
|----------|--------|
| C++ | `int* ptr = nullptr;` |
| Java | `String s = null;` |
| Python | `x = None` |

---

## Operators

### Arithmetic
| Operator | C++ | Java | Python |
|----------|-----|------|--------|
| Division | `10/3` = 3 (int) | `10/3` = 3 (int) | `10/3` = 3.333 |
| Floor division | `10/3` (int) | `10/3` (int) | `10//3` |
| Exponent | `pow(a,b)` | `Math.pow(a,b)` | `a**b` |

```cpp
// C++
int div = 10 / 3;
float fdiv = 10.f / 3;
int exp = pow(2, 3);
```

```java
// Java
int div = 10 / 3;
double fdiv = 10.0 / 3;
double exp = Math.pow(2, 3);
```

```python
# Python
div = 10 / 3
fdiv = 10 // 3
exp = 2 ** 3
```

### Compound Assignment
| Operator | C++ | Java | Python |
|----------|-----|------|--------|
| += | `x += y` | `x += y` | `x += y` |
| ++ | `x++` / `++x` | `x++` / `++x` | No |

```cpp
// C++
x += 5;
x++;
++x;
```

```java
// Java
x += 5;
x++;
++x;
```

```python
# Python
x += 5
# No ++ operator
x = x + 1
```

### Comparison
| Operator | C++ | Java | Python |
|----------|-----|------|--------|
| Equal | `==` | `==` | `==` |
| Not equal | `!=` | `!=` | `!=` |
| Identity | `==` (pointers) | `==` (reference) | `is` |

```cpp
// C++
if (x == y) { }
if (x != y) { }
if (ptr == nullptr) { }
```

```java
// Java
if (x == y) { }
if (x != y) { }
if (obj == null) { }
if (obj.equals(other)) { }
```

```python
# Python
if x == y: pass
if x != y: pass
if x is None: pass
if x is y: pass  # Same object
```

### Logical
| Operator | C++ | Java | Python |
|----------|-----|------|--------|
| AND | `&&` | `&&` | `and` |
| OR | `||` | `||` | `or` |
| NOT | `!` | `!` | `not` |

```cpp
// C++
if (x > 0 && y > 0) { }
if (x > 0 || y > 0) { }
if (!(x > 0)) { }
```

```java
// Java
if (x > 0 && y > 0) { }
if (x > 0 || y > 0) { }
if (!(x > 0)) { }
```

```python
# Python
if x > 0 and y > 0: pass
if x > 0 or y > 0: pass
if not x > 0: pass
```

### Ternary
| Operator | C++ | Java | Python |
|----------|-----|------|--------|
| Ternary | `cond ? a : b` | `cond ? a : b` | `a if cond else b` |

```cpp
// C++
int max = (a > b) ? a : b;
```

```java
// Java
int max = (a > b) ? a : b;
```

```python
# Python
max_val = a if a > b else b
```

---

## Control Flow

### If / Else
| Language | Syntax |
|----------|--------|
| C++ | `if (x) { } else if (y) { } else { }` |
| Java | `if (x) { } else if (y) { } else { }` |
| Python | `if x: ... elif y: ... else: ...` |

```cpp
// C++
if (age >= 18) {
    std::cout << "Adult";
} else if (age >= 13) {
    std::cout << "Teen";
} else {
    std::cout << "Child";
}
```

```java
// Java
if (age >= 18) {
    System.out.println("Adult");
} else if (age >= 13) {
    System.out.println("Teen");
} else {
    System.out.println("Child");
}
```

```python
# Python
if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teen")
else:
    print("Child")
```

### Switch / Match
| Language | Syntax |
|----------|--------|
| C++ | `switch(x) { case 1: break; default: }` |
| Java | `switch(x) { case 1 -> "one"; default -> "other"; }` |
| Python | `match x: case 1: ... case _: ...` |

```cpp
// C++
switch (grade) {
    case 'A':
        std::cout << "Excellent";
        break;
    case 'B':
        std::cout << "Good";
        break;
    default:
        std::cout << "Needs improvement";
}
```

```java
// Java
String result = switch (grade) {
    case 'A' -> "Excellent";
    case 'B' -> "Good";
    default -> "Needs improvement";
};
```

```python
# Python
match grade:
    case 'A':
        print("Excellent")
    case 'B':
        print("Good")
    case _:
        print("Needs improvement")
```

---

## Loops

### While
| Language | Syntax |
|----------|--------|
| C++ | `while (cond) { }` |
| Java | `while (cond) { }` |
| Python | `while cond: ...` |

```cpp
// C++
int i = 0;
while (i < 10) {
    std::cout << i << " ";
    i++;
}
```

```java
// Java
int i = 0;
while (i < 10) {
    System.out.print(i + " ");
    i++;
}
```

```python
# Python
i = 0
while i < 10:
    print(i, end=" ")
    i += 1
```

### Do-While
| Language | Syntax |
|----------|--------|
| C++ | `do { } while (cond);` |
| Java | `do { } while (cond);` |
| Python | No equivalent |

```cpp
// C++
int i = 0;
do {
    std::cout << i << " ";
    i++;
} while (i < 10);
```

```java
// Java
int i = 0;
do {
    System.out.print(i + " ");
    i++;
} while (i < 10);
```

### For Loop
| Language | Syntax |
|----------|--------|
| C++ | `for (int i=0; i<n; i++) { }` |
| Java | `for (int i=0; i<n; i++) { }` |
| Python | `for i in range(n): ...` |

```cpp
// C++
for (int i = 0; i < 10; i++) {
    std::cout << i << " ";
}
```

```java
// Java
for (int i = 0; i < 10; i++) {
    System.out.print(i + " ");
}
```

```python
# Python
for i in range(10):
    print(i, end=" ")
```

### For-Each
| Language | Syntax |
|----------|--------|
| C++ | `for (auto x : vec) { }` |
| Java | `for (var x : list) { }` |
| Python | `for x in list: ...` |

```cpp
// C++
#include <vector>
std::vector<int> nums = {1, 2, 3, 4, 5};
for (int num : nums) {
    std::cout << num << " ";
}
```

```java
// Java
import java.util.*;
List<Integer> nums = Arrays.asList(1, 2, 3, 4, 5);
for (int num : nums) {
    System.out.print(num + " ");
}
```

```python
# Python
nums = [1, 2, 3, 4, 5]
for num in nums:
    print(num, end=" ")
```

### Map / Filter / Reduce
| Language | Map | Filter | Reduce |
|----------|-----|--------|--------|
| C++ | `std::transform` | `std::copy_if` | `std::accumulate` |
| Java | `.map()` | `.filter()` | `.reduce()` |
| Python | `map()` | `filter()` | `functools.reduce()` |

```cpp
// C++
#include <algorithm>
#include <numeric>
#include <vector>

std::vector<int> nums = {1, 2, 3, 4, 5};
std::vector<int> doubled;

// Map - transform each element
std::transform(nums.begin(), nums.end(), std::back_inserter(doubled),
              [](int x) { return x * 2; });  // doubled = {2, 4, 6, 8, 10}

// Filter - copy_if
std::vector<int> evens;
std::copy_if(nums.begin(), nums.end(), std::back_inserter(evens),
            [](int x) { return x % 2 == 0; });  // evens = {2, 4}

// Reduce - accumulate
int sum = std::accumulate(nums.begin(), nums.end(), 0);  // sum = 15
```

```java
// Java
import java.util.*;
import java.util.stream.*;

List<Integer> nums = Arrays.asList(1, 2, 3, 4, 5);

// Map - transform each element
List<Integer> doubled = nums.stream()
    .map(x -> x * 2)
    .collect(Collectors.toList());  // doubled = {2, 4, 6, 8, 10}

// Filter - keep elements matching predicate
List<Integer> evens = nums.stream()
    .filter(x -> x % 2 == 0)
    .collect(Collectors.toList());  // evens = {2, 4}

// Reduce - combine elements
int sum = nums.stream()
    .reduce(0, (a, b) -> a + b);  // sum = 15

// ForEach - apply to each element
nums.forEach(x -> System.out.println(x));
```

```python
# Python
from functools import reduce

nums = [1, 2, 3, 4, 5]

# Map - transform each element
doubled = list(map(lambda x: x * 2, nums))  # doubled = [2, 4, 6, 8, 10]

# List comprehension (more Pythonic)
doubled = [x * 2 for x in nums]

# Filter - keep elements matching predicate
evens = list(filter(lambda x: x % 2 == 0, nums))  # evens = [2, 4]

# List comprehension for filter (more Pythonic)
evens = [x for x in nums if x % 2 == 0]

# Reduce - combine elements
sum_result = reduce(lambda a, b: a + b, nums)  # sum = 15

# ForEach - apply to each element
for num in nums:
    print(num)
```

---

## Functions / Methods

### Declaration
| Language | Syntax |
|----------|--------|
| C++ | `ret_type name(params) { }` |
| Java | `modifiers ret_type name(params) { }` |
| Python | `def name(params): ...` |

```cpp
// C++
int add(int a, int b) {
    return a + b;
}
```

```java
// Java
public int add(int a, int b) {
    return a + b;
}
```

```python
# Python
def add(a, b):
    return a + b
```

### Parameters
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Default args | `void f(int x=0)` | No (overload) | `def f(x=0)` |
| Varargs | `...` (C-style) | `type... args` | `*args` |
| Kwargs | No | No | `**kwargs` |

```cpp
// C++
int add(int a, int b = 0) {
    return a + b;
}

// C-style varargs
#include <cstdarg>
int calc_sum(int count, ...) {
    va_list args;
    va_start(args, count);
    int total = 0;
    for (int i = 0; i < count; i++)
        total += va_arg(args, int);
    va_end(args);
    return total;
}
```

```java
// Java
// Default args - use overloading
int add(int a) { return add(a, 0); }
int add(int a, int b) { return a + b; }

int sum(int... nums) {
    int total = 0;
    for (int num : nums) total += num;
    return total;
}
```

```python
# Python
def add(a, b=0):
    return a + b

def calc_sum(*nums):
    return sum(nums)

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

### Return Multiple Values
```cpp
// C++ - Return struct or use references
struct Pair { int min; int max; };
Pair getMinMax(int a, int b) {
    return {a < b ? a : b, a > b ? a : b};
}
```

```java
// Java - Return custom class or array
class Pair {
    int min; int max;
    Pair(int min, int max) { this.min = min; this.max = max; }
}
Pair getMinMax(int a, int b) {
    return new Pair(Math.min(a, b), Math.max(a, b));
}
```

```python
# Python - Return tuple
def get_min_max(a, b):
    return min(a, b), max(a, b)

min_val, max_val = get_min_max(3, 7)
```

### Lambdas
| Language | Syntax |
|----------|--------|
| C++ | `[capture](params) { body }` |
| Java | `(params) -> body` |
| Python | `lambda params: body` |

```cpp
// C++
auto square = [](int x) { return x * x; };
int result1 = square(5);  // 25

int y = 10;
auto addY = [y](int x) { return x + y; };
int result2 = addY(5);   // 15
```

```java
// Java
import java.util.function.*;
Function<Integer, Integer> square = x -> x * x;
int result1 = square.apply(5);  // 25

int y = 10;
Function<Integer, Integer> addY = x -> x + y;
int result2 = addY.apply(5);   // 15
```

```python
# Python
square = lambda x: x * x
result1 = square(5)  # 25

add_y = lambda x, y=10: x + y
result2 = add_y(5)   # 15
```

---

## Classes & OOP

### Class Declaration & Constructors
| Language | Class Syntax | Constructor Syntax |
|----------|--------------|-------------------|
| C++ | `class Name { ... };` | `Name(params) : member(val) { }` |
| Java | `public class Name { ... }` | `public Name(params) { this.member = val; }` |
| Python | `class Name:` | `def __init__(self, params): self.member = val` |

```cpp
// C++
class Person {
private:
    std::string name;
    int age;
public:
    Person(std::string n = "Unknown", int a = 0) : name(n), age(a) { }
    
    void print() {
        std::cout << name << " is " << age << " years old." << std::endl;
    }
};

// Object initialization
Person p1("Alice", 30);
Person p2;  // Uses defaults
```

```java
// Java
public class Person {
    private String name;
    private int age;
    
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public Person() { this("Unknown", 0); }
    
    public void print() {
        System.out.println(name + " is " + age + " years old.");
    }
}

// Object initialization
Person p1 = new Person("Alice", 30);
Person p2 = new Person();  // Uses defaults
```

```python
# Python
class Person:
    def __init__(self, name="Unknown", age=0):
        self.name = name
        self.age = age
    
    def print(self):
        print(f"{self.name} is {self.age} years old.")

# Object initialization
p1 = Person("Alice", 30)
p2 = Person()  # Uses defaults
```

### Inheritance
| Language | Syntax |
|----------|--------|
| C++ | `class Child : public Parent { ... };` |
| Java | `class Child extends Parent { ... }` |
| Python | `class Child(Parent):` |

```cpp
// C++
class Student : public Person {
public:
    int studentId;
    Student(std::string n, int a, int id) : Person(n, a), studentId(id) { }
};
```

```java
// Java
class Student extends Person {
    public int studentId;
    public Student(String name, int age, int studentId) {
        super(name, age);
        this.studentId = studentId;
    }
}
```

```python
# Python
class Student(Person):
    def __init__(self, name, age, student_id):
        super().__init__(name, age)
        self.student_id = student_id
```

### Method Override
| Language | C++ | Java | Python |
|----------|-----|------|--------|
| Override keyword | `override` | `@Override` | No keyword |

```cpp
// C++
class Dog : public Animal {
public:
    void makeSound() const override {
        std::cout << "Woof! Woof!" << std::endl;
    }
};
```

```java
// Java
class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof! Woof!");
    }
}
```

```python
# Python
class Dog(Animal):
    def make_sound(self):
        print("Woof! Woof!")
```

### Static & Class Methods
| Language | Static | Class Method |
|----------|--------|-------------|
| C++ | `static ret_type name() { }` | No |
| Java | `public static ret_type name() { }` | No |
| Python | `@staticmethod` | `@classmethod` |

```cpp
// C++
class Math {
public:
    static int square(int x) { return x * x; }
};
Math::square(5);
```

```java
// Java
public class Math {
    public static int square(int x) { return x * x; }
}
Math.square(5);
```

```python
# Python
class Math:
    @staticmethod
    def square(x):
        return x * x
    
    @classmethod
    def get_version(cls):
        return "1.0"

Math.square(5)
Math.get_version()
```

### Abstract Classes
| Language | Syntax |
|----------|--------|
| C++ | `virtual ret_type name() = 0;` |
| Java | `public abstract ret_type name();` |
| Python | `@abstractmethod def name(self):` |

```cpp
// C++
class Shape {
public:
    virtual double area() const = 0;
    virtual ~Shape() { }
};

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) { }
    double area() const override {
        return 3.14159 * radius * radius;
    }
};
```

```java
// Java
abstract class Shape {
    public abstract double area();
}

class Circle extends Shape {
    private double radius;
    public Circle(double radius) { this.radius = radius; }
    @Override
    public double area() {
        return Math.PI * radius * radius;
    }
}
```

```python
# Python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        import math
        return math.pi * self.radius * self.radius
```

---

## References & Pointers

### Pointers
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Pointers | Yes | No | No |
| Null | `nullptr` | `null` | `None` |

```cpp
// C++ - Pointers
int x = 10;
int* ptr = &x;
std::cout << *ptr;
*ptr = 20;

// Dynamic allocation
int* arr = new int[10];
delete[] arr;

int* nullPtr = nullptr;
if (nullPtr == nullptr) { }

// Pointer arithmetic
int nums[] = {1, 2, 3};
int* p = nums;
std::cout << *(p + 1);
```

### References
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Reference type | `int& ref = x;` | All objects are references | All variables are references |
| Nullable | No | Yes | Yes |
| Reassignable | No | Yes | Yes |

```cpp
// C++ - References
int y = 100;
int& ref = y;
ref = 200;     // Changes y to 200 (ref is an alias for y)

// Pass by reference
void modify(int& x) { x = 10; }
int a = 5;
modify(a);

// Const reference
const int& constRef = y;
```

**Note:** C++ references are aliases - once bound, they cannot be reassigned to a different object. Changing a reference changes the original variable.

```java
// Java - All objects are references
String s1 = new String("hello");
String s2 = s1;
s1 = null;       // s1 is now null, but s2 still points to "hello"

String nullRef = null;
if (nullRef == null) { }

// Reference vs value equality
String a = new String("hello");
String b = new String("hello");
a == b;           // false (different references)
a.equals(b);      // true (same value)
```

**Note:** Java references are like pointers - reassigning one variable doesn't affect others pointing to the same object.

```python
# Python - All variables are references
x = 10
y = x
x = None        # x is now None, but y still points to 10

if x is None: pass

# Reference vs value equality
a = [1, 2, 3]
b = [1, 2, 3]
c = a
a == b      # True (same value)
a is b      # False (different objects)
a is c      # True (same object)

# id() - get object identity
print(id(a))
```

**Note:** Python references are like pointers - reassigning one variable doesn't affect others pointing to the same object.

### Smart Pointers & Weak References
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Unique ownership | `unique_ptr<T>` | No | No |
| Shared ownership | `shared_ptr<T>` | No | No |
| Weak reference | `weak_ptr<T>` | `WeakReference<T>` | `weakref.ref()` |

```cpp
// C++ - Smart pointers
#include <memory>

// unique_ptr - exclusive ownership
std::unique_ptr<int> ptr = std::make_unique<int>(42);
// Automatically deleted when out of scope

// shared_ptr - shared ownership
std::shared_ptr<int> shared1 = std::make_shared<int>(100);
std::shared_ptr<int> shared2 = shared1;  // Both own the object
// Deleted when last shared_ptr goes out of scope

// weak_ptr - non-owning
std::weak_ptr<int> weak = shared1;
if (auto temp = weak.lock()) {
    // Use *temp if still exists
}
```

```java
// Java - Weak references
import java.lang.ref.*;

Person person = new Person("Alice", 30);
WeakReference<Person> weakRef = new WeakReference<>(person);

// If person is no longer strongly referenced, it can be GC'd
Person p = weakRef.get();  // May return null
```

```python
# Python - Weak references
import weakref

class MyClass: pass

obj = MyClass()
weak_ref = weakref.ref(obj)

print(weak_ref())  # <MyClass object>
del obj
print(weak_ref())  # None (collected)
```

---

## Collections

### Arrays / Lists
| Language | Type | Mutable |
|----------|------|---------|
| C++ | `int arr[5]` / `std::vector<T>` | `std::vector` yes |
| Java | `int[] arr` / `ArrayList<T>` | `ArrayList` yes |
| Python | `list` | Yes |

```cpp
// C++
int arr[5] = {1, 2, 3, 4, 5};

#include <vector>
std::vector<int> vec = {1, 2, 3};
vec.push_back(4);
vec.pop_back();
```

```java
// Java
// Array (fixed)
int[] arr = {1, 2, 3, 4, 5};

// ArrayList (dynamic)
import java.util.*;
ArrayList<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.remove(0);
```

```python
# Python
# List (dynamic)
lst = [1, 2, 3, 4, 5]
lst.append(6)
lst.pop()
lst.insert(0, 0)

# Slicing
sub = lst[1:3]      # [2, 3]
rev = lst[::-1]     # [5, 4, 3, 2, 1]
first = lst[0]      # 1
last = lst[-1]      # 5
```

### Sets
| Language | Type | Ordered |
|----------|------|---------|
| C++ | `std::set<T>` / `std::unordered_set<T>` | `set` yes |
| Java | `HashSet<T>` / `TreeSet<T>` | `TreeSet` yes |
| Python | `set` | No |

```cpp
// C++
#include <set>
#include <unordered_set>

std::set<int> nums = {3, 1, 4, 1, 5};  // {1, 3, 4, 5}

std::unordered_set<int> hashNums = {3, 1, 4, 1, 5};
```

```java
// Java
import java.util.*;

HashSet<Integer> nums = new HashSet<>();
nums.add(3);
nums.add(1);

TreeSet<Integer> sortedNums = new TreeSet<>();
sortedNums.add(3);
sortedNums.add(1);  // {1, 3}
```

```python
# Python
nums = {3, 1, 4, 1, 5}  # {1, 3, 4, 5}
nums.add(6)
nums.discard(3)

union = nums | {7, 8}
intersection = nums & {4, 5}
difference = nums - {4, 5}
```

### Sorting
| Language | Strings (A-Z) | Numbers (ascending) | Numbers (descending) |
|----------|---------------|---------------------|---------------------|
| C++ | `std::sort(vec.begin(), vec.end())` | `std::sort(vec.begin(), vec.end())` | `std::sort(vec.rbegin(), vec.rend())` |
| Java | `Collections.sort(list)` | `Collections.sort(list)` | `Collections.sort(list, Collections.reverseOrder())` |
| Python | `sorted(list)` or `list.sort()` | `sorted(list)` or `list.sort()` | `sorted(list, reverse=True)` or `list.sort(reverse=True)` |

```cpp
// C++
#include <algorithm>
#include <vector>
#include <string>

// Strings
std::vector<std::string> names = {"Charlie", "Alice", "Bob"};
std::sort(names.begin(), names.end());  // {"Alice", "Bob", "Charlie"}

// Numbers ascending
std::vector<int> nums = {5, 2, 8, 1};
std::sort(nums.begin(), nums.end());  // {1, 2, 5, 8}

// Numbers descending
std::sort(nums.rbegin(), nums.rend());  // {8, 5, 2, 1}
```

```java
// Java
import java.util.*;

// Strings
List<String> names = Arrays.asList("Charlie", "Alice", "Bob");
Collections.sort(names);  // ["Alice", "Bob", "Charlie"]

// Numbers ascending
List<Integer> nums = Arrays.asList(5, 2, 8, 1);
Collections.sort(nums);  // [1, 2, 5, 8]

// Numbers descending
Collections.sort(nums, Collections.reverseOrder());  // [8, 5, 2, 1]
```

```python
# Python
# Strings
names = ["Charlie", "Alice", "Bob"]
sorted_names = sorted(names)  # ['Alice', 'Bob', 'Charlie']
names.sort()  # Sorts in place

# Numbers ascending
nums = [5, 2, 8, 1]
sorted_nums = sorted(nums)  # [1, 2, 5, 8]
nums.sort()  # Sorts in place

# Numbers descending
sorted_nums_desc = sorted(nums, reverse=True)  # [8, 5, 2, 1]
nums.sort(reverse=True)  # Sorts in place
```

### Dictionaries / Maps
| Language | Type | Ordered |
|----------|------|---------|
| C++ | `std::map<K,V>` / `std::unordered_map<K,V>` | `map` yes |
| Java | `HashMap<K,V>` / `TreeMap<K,V>` | `TreeMap` yes |
| Python | `dict` | Yes (3.7+) |

```cpp
// C++
#include <map>
#include <unordered_map>

// Ordered map
std::map<std::string, int> ages;
ages["Alice"] = 30;
ages["Bob"] = 25;

// Hash map
std::unordered_map<std::string, int> hashAges;
hashAges["Alice"] = 30;
```

```java
// Java
import java.util.*;

// HashMap (unordered)
HashMap<String, Integer> ages = new HashMap<>();
ages.put("Alice", 30);
ages.put("Bob", 25);

// TreeMap (ordered)
TreeMap<String, Integer> sortedAges = new TreeMap<>();
sortedAges.put("Bob", 25);
sortedAges.put("Alice", 30);
```

```python
# Python
# dict (ordered in 3.7+)
ages = {"Alice": 30, "Bob": 25}
ages["Charlie"] = 35
alice_age = ages.get("Alice", 0)

# Iteration
for name, age in ages.items():
    print(f"{name}: {age}")
```

---

## Strings

### Formatting
| Language | Syntax |
|----------|--------|
| C++ | `std::format("{}, {}", a, b)` (C++20) |
| Java | `String.format("%d, %d", a, b)` |
| Python | `f"{a}, {b}"` |

```cpp
// C++
#include <string>
std::string s1 = "Hello";
std::string s2 = "World";

std::string s3 = s1 + " " + s2;
s1 += s2;

int len = s1.length();

char first = s1[0];

std::string sub = s1.substr(1, 4);

size_t pos = s1.find("lo");
bool contains = (s1.find("lo") != std::string::npos);

s1.replace(1, 3, "pp");
```

```java
// Java
String s1 = "Hello";
String s2 = "World";

String s3 = s1 + " " + s2;

// StringBuilder (mutable, more efficient)
StringBuilder sb = new StringBuilder();
sb.append("Hello");
sb.append(" ");
sb.append("World");

int len = s1.length();

char first = s1.charAt(0);

String sub = s1.substring(1, 5);

int pos = s1.indexOf("lo");
boolean contains = s1.contains("lo");

String replaced = s1.replace("llo", "pp");
```

```python
# Python
s1 = "Hello"
s2 = "World"

s3 = s1 + " " + s2

# f-strings (recommended)
s = f"{s1}, {s2}!"

len_s = len(s1)

first = s1[0]
last = s1[-1]
slice = s1[1:4]

sub = s1[1:5]

pos = s1.find("lo")  # Returns -1 if not found
contains = "lo" in s1

replaced = s1.replace("llo", "pp")

parts = s1.split(" ")

joined = " ".join(parts)

upper = s1.upper()
lower = s1.lower()

trimmed = "  hello  ".strip()
```

---

## I/O

### Console
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Output | `std::cout << "text";` | `System.out.println();` | `print()` |
| Input | `std::cin >> var;` | `new Scanner(System.in).next();` | `input()` |

```cpp
// C++
#include <iostream>

// Output
std::cout << "Hello, World!" << std::endl;
std::cout << "Value: " << 42 << std::endl;

// Input
int age;
std::cin >> age;
std::string name;
std::getline(std::cin, name);

// Formatting
#include <iomanip>
std::cout << std::setw(10) << 42 << std::endl;
```

```java
// Java
import java.util.Scanner;

// Output
System.out.println("Hello, World!");
System.out.printf("%d %f %s%n", 42, 3.14, "hello");

// Input
Scanner scanner = new Scanner(System.in);
String name = scanner.next();
int age = scanner.nextInt();
scanner.nextLine(); // Consume newline
```

```python
# Python

# Output
print("Hello, World!")
print(f"Value: {42}")

# Input
name = input("Enter name: ")
age = int(input("Enter age: "))
```

### Files
| Aspect | C++ | Java | Python |
|--------|-----|------|--------|
| Write | `std::ofstream` | `FileWriter` | `open(file, "w")` |
| Read | `std::ifstream` | `FileReader` | `open(file, "r")` |
| Context | Manual close | Try-with-resources | `with` statement |

```cpp
// C++
#include <fstream>

std::ofstream out("file.txt");
out << "Hello, File!" << std::endl;
out.close();

std::ifstream in("file.txt");
std::string line;
while (std::getline(in, line)) {
    std::cout << line << std::endl;
}
in.close();
```

```java
// Java
import java.io.*;

try (FileWriter writer = new FileWriter("file.txt")) {
    writer.write("Hello, File!\n");
}

try (BufferedReader reader = new BufferedReader(new FileReader("file.txt"))) {
    String line;
    while ((line = reader.readLine()) != null) {
        System.out.println(line);
    }
}
```

```python
# Python

with open("file.txt", "w") as f:
    f.write("Hello, File!\n")

with open("file.txt", "r") as f:
    for line in f:
        print(line, end="")
```

---

## Error Handling

### Try-Catch
| Language | Syntax |
|----------|--------|
| C++ | `try { } catch (const Type& e) { } catch (...) { }` |
| Java | `try { } catch (Type e) { } finally { }` |
| Python | `try: ... except Type as e: ... finally: ...` |

```cpp
// C++
#include <stdexcept>

try {
    int a = 10, b = 0;
    if (b == 0) throw std::runtime_error("Division by zero");
    int result = a / b;
} catch (const std::exception& e) {
    std::cerr << "Exception: " << e.what() << std::endl;
} catch (...) {
    std::cerr << "Unknown exception" << std::endl;
}
```

```java
// Java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.err.println("Division by zero: " + e.getMessage());
} catch (Exception e) {
    System.err.println("Exception: " + e.getMessage());
} finally {
    System.out.println("This always executes");
}
```

```python
# Python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Division by zero: {e}")
except Exception as e:
    print(f"Exception: {e}")
else:
    print("No exception")
finally:
    print("This always executes")
```

### Throw / Raise
| Language | Syntax |
|----------|--------|
| C++ | `throw Exception("msg");` |
| Java | `throw new Exception("msg");` |
| Python | `raise Exception("msg")` |

```cpp
// C++
#include <stdexcept>

// Standard exception
throw std::runtime_error("Error occurred");

// Custom exception
class MyException : public std::exception {
    std::string msg;
public:
    MyException(const std::string& m) : msg(m) {}
    const char* what() const noexcept override { return msg.c_str(); }
};
throw MyException("Custom error");
```

```java
// Java

throw new IllegalArgumentException("Invalid argument");

class MyException extends Exception {
    public MyException(String message) { super(message); }
}
throw new MyException("Custom error");

public void readFile() throws IOException {
    // ...
}
```

```python
# Python

raise ValueError("Invalid value")

class MyException(Exception):
    def __init__(self, message):
        super().__init__(message)

raise MyException("Custom error")

try:
    risky_operation()
except Exception as e:
    print(f"Logging: {e}")
    raise  // Re-raise
```

---
