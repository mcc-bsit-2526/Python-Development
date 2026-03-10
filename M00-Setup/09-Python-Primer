# 09 — Python Primer
### Python Development | MCC BSIT 2526

[Back to Setup Overview](./Environment-Setup.md)

---

Read this before opening Module 01. It gives you enough context about how Python works — and how it compares to languages you may already know — so that the actual modules make sense from the start.

There are no exercises here. Just read it and refer back when something is unclear.

---

## Table of Contents

1. [What Python Is](#1-what-python-is)
2. [How Python Runs Your Code](#2-how-python-runs-your-code)
3. [Running Code in VS Code](#3-running-code-in-vs-code)
4. [Python Syntax at a Glance](#4-python-syntax-at-a-glance)
5. [Python vs Java vs C](#5-python-vs-java-vs-c)
6. [Reading Error Messages](#6-reading-error-messages)
7. [VS Code Features Worth Knowing](#7-vs-code-features-worth-knowing)
8. [Quick Reference Card](#8-quick-reference-card)

---

## 1. What Python Is

Python is a **high-level, interpreted, dynamically-typed** programming language. Those three words matter:

**High-level** — Python is closer to human language than machine language. You write `print("Hello")` instead of managing memory addresses and registers. The language handles the low-level details for you.

**Interpreted** — Python runs your code line by line, directly, without a separate compile step. You write, you run, you see results immediately. This makes it fast to experiment with.

**Dynamically-typed** — You do not declare the type of a variable when you create it. Python figures out the type from the value you assign. You write `age = 20` instead of `int age = 20`.

### Where Python is used

- Web development — Instagram, Pinterest, and Spotify run on Python backends
- Data science and AI — most machine learning frameworks are Python-first
- Automation — scripting repetitive system tasks
- Cybersecurity — penetration testing tools and exploit frameworks
- DevOps — infrastructure automation and deployment scripts

As IT students, you will encounter Python in networking, security, data analytics, and systems administration — not just software development.

---

## 2. How Python Runs Your Code

Understanding this saves a lot of confusion later.

When you run a Python file, the interpreter reads it **top to bottom, one line at a time**. Each line is executed before moving to the next. There is no compile step, no `.class` file, no `.exe` — just your source file running directly.

```
your_file.py
     |
     v
Python Interpreter
     |
     v
Output (terminal / notebook)
```

This also means **errors stop execution at the line where they occur**. Everything above that line ran successfully. Everything below did not run at all.

```python
print("Line 1")   # runs
print("Line 2")   # runs
print(x)          # ERROR — x is not defined, stops here
print("Line 4")   # never runs
```

---

## 3. Running Code in VS Code

There are three ways to run Python code in VS Code. You will use all three at different times.

---

### Way 1 — Running a .py File

A `.py` file is a plain Python script. Write your code, save, and run the whole file.

**Create your first file:**

1. Create a new file in VS Code — `File → New File`
2. Save it as `hello.py`
3. Type this:

```python
print("Hello, world!")
print("My name is Juan.")
print(2 + 3)
```

**Run it — two options:**

Option A — press `Ctrl + F5`

Option B — open the terminal (`` Ctrl + ` ``) and type:
```bash
python hello.py       # Windows
python3 hello.py      # macOS / Linux
```

**Output:**
```
Hello, world!
My name is Juan.
5
```

---

### Way 2 — The REPL (Interactive Shell)

The REPL (Read-Eval-Print Loop) is an interactive Python session. You type one line at a time and see the result immediately. Useful for quick tests.

**Open it** — in the VS Code terminal:
```bash
python        # Windows
python3       # macOS / Linux
```

**Prompt:**
```
Python 3.12.0 ...
>>>
```

**Using it:**
```python
>>> 2 + 3
5
>>> name = "Maria"
>>> print(name)
Maria
>>> type(42)
<class 'int'>
```

**Exit:**
```python
>>> exit()
```

> ⚠️ Variables defined in the REPL are lost when you exit. Use a `.py` file or notebook for actual work.

---

### Way 3 — Jupyter Notebooks (.ipynb)

The primary format for this course. Each cell behaves like a mini REPL — run one cell at a time, output appears below it. Notebooks let you mix code and text in one document.

Run a cell: click the play button or press `Shift + Enter`.

---

### Comparison

| Method | Best for |
|--------|---------|
| `.py` file | Scripts, complete programs, assignments |
| REPL | Quick one-line experiments |
| Notebook | Learning, step-by-step exploration, this course |

---

## 4. Python Syntax at a Glance

These are the rules Python enforces that differ most from other languages.

---

### No Semicolons

Lines end with a newline, not a semicolon. You can add one and Python will not complain, but it is not conventional.

```python
# Correct
print("Hello")
print("World")

# Works but unnecessary
print("Hello");
print("World");
```

---

### No Curly Braces — Indentation Defines Blocks

In Java and C, curly braces `{}` define blocks of code. In Python, **indentation defines blocks**. This is not a style choice — it is enforced syntax.

```python
# Python — colon + indentation
if grade >= 75:
    print("Passed")
    print("Congratulations")
print("This is outside the block")
```

The standard is **4 spaces** per level. VS Code inserts this automatically when you press Tab after a colon.

> ⚠️ Inconsistent indentation causes `IndentationError`. Never mix tabs and spaces.

---

### No Type Declarations

Python infers the type from the value. You never write `int`, `String`, or `double` before a variable name.

```python
# Python
name = "Maria"
age  = 20
gpa  = 1.75
```

The type is attached to the **value**, not the variable. The same variable can hold different types at different times (though this is rarely a good idea in practice).

---

### Colons After Block Headers

Every statement that starts a block ends with a colon — `if`, `else`, `for`, `while`, `def`, `class`.

```python
if x > 0:
    print("positive")

for i in range(5):
    print(i)

def greet(name):
    print(f"Hello, {name}")
```

Forgetting the colon is one of the most common `SyntaxError` causes for beginners.

---

### Comments

```python
# Single-line comment

"""
Multi-line comment.
Python treats this as a string that is never assigned,
so it is effectively ignored.
"""
```

---

### Boolean Values Are Capitalized

Python uses `True` and `False` with a capital first letter. Lowercase `true` and `false` are `NameError`.

```python
is_enrolled = True    # correct
is_enrolled = true    # NameError
```

---

### None Instead of Null

Python uses `None` where Java uses `null` and C uses `NULL`.

```python
result = None
```

---

### No ++ Operator

Python does not have `i++` or `i--`. Use `i += 1` and `i -= 1`.

```python
i = 0
i += 1   # i is now 1
i -= 1   # i is now 0
```

---

## 5. Python vs Java vs C

The same program written in all three languages. Read across each section to see exactly what changes.

---

### Hello World

| | Code |
|-|------|
| **Java** | `System.out.println("Hello, world!");` |
| **C** | `printf("Hello, world!\n");` |
| **Python** | `print("Hello, world!")` |

---

### Variables

**Java**
```java
String name    = "Maria";
int    age     = 20;
double gpa     = 1.75;
boolean active = true;
```

**C**
```c
char  name[]  = "Maria";
int   age     = 20;
float gpa     = 1.75f;
int   active  = 1;       // no native bool
```

**Python**
```python
name   = "Maria"
age    = 20
gpa    = 1.75
active = True
```

---

### If / Else

**Java / C**
```java
if (grade >= 75) {
    System.out.println("Passed");
} else {
    System.out.println("Failed");
}
```

**Python**
```python
if grade >= 75:
    print("Passed")
else:
    print("Failed")
```

Differences: no parentheses required around the condition, no curly braces, colon at the end of each branch header.

---

### If / Else If / Else

**Java / C**
```java
if (grade <= 1.0) {
    System.out.println("Excellent");
} else if (grade <= 2.0) {
    System.out.println("Good");
} else {
    System.out.println("Needs improvement");
}
```

**Python**
```python
if grade <= 1.0:
    print("Excellent")
elif grade <= 2.0:
    print("Good")
else:
    print("Needs improvement")
```

Python uses `elif` instead of `else if`.

---

### For Loop

**Java / C**
```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

**Python**
```python
for i in range(5):
    print(i)
```

Python's `for` iterates over a sequence. `range(5)` produces `0, 1, 2, 3, 4`. There is no counter-with-condition syntax.

---

### While Loop

**Java / C**
```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

**Python**
```python
i = 0
while i < 5:
    print(i)
    i += 1
```

---

### Functions

**Java**
```java
public static int add(int a, int b) {
    return a + b;
}
```

**C**
```c
int add(int a, int b) {
    return a + b;
}
```

**Python**
```python
def add(a, b):
    return a + b
```

No return type, no parameter types, no `public static`. Just `def`, the name, and the parameters.

---

### Arrays / Lists

**Java**
```java
int[] scores = {85, 90, 78, 92};
System.out.println(scores[0]);
```

**C**
```c
int scores[] = {85, 90, 78, 92};
printf("%d\n", scores[0]);
```

**Python**
```python
scores = [85, 90, 78, 92]
print(scores[0])
```

Python calls them **lists**. They are zero-indexed like Java and C, but they resize automatically and can hold mixed types.

---

### Full Side-by-Side Summary

| Feature | Java | C | Python |
|---------|------|---|--------|
| Line ending | `;` required | `;` required | newline |
| Code blocks | `{}` | `{}` | indentation |
| Type declaration | required | required | not required |
| Condition syntax | `if (x > 0)` | `if (x > 0)` | `if x > 0:` |
| Else-if keyword | `else if` | `else if` | `elif` |
| Boolean literals | `true` / `false` | `1` / `0` | `True` / `False` |
| Null value | `null` | `NULL` | `None` |
| Increment | `i++` | `i++` | `i += 1` |
| Print | `System.out.println()` | `printf()` | `print()` |
| Function keyword | return type + name | return type + name | `def` |
| Entry point | `main()` required | `main()` required | none — runs top to bottom |
| Execution | compiled | compiled | interpreted |

---

### The Biggest Adjustment

If you are coming from Java or C, **the hardest habit to break is expecting curly braces**. In Python, indentation is not formatting — it is syntax. Misaligned indentation is a bug.

```python
# Correct — consistent 4-space indentation
if True:
    print("inside the block")
    print("still inside")
print("outside the block")

# Wrong — mixed indentation causes IndentationError
if True:
    print("inside")
  print("wrong — this is 2 spaces, not 4")
```

VS Code helps by auto-indenting after a colon. Let it do its job and do not manually adjust indentation unless you are certain.

---

## 6. Reading Error Messages

Errors are not failures — they are Python telling you exactly what went wrong. The skill is reading them correctly.

When an error occurs, Python prints a **traceback**:

```python
# Code
name = "Maria"
print(name + 5)
```

```
Traceback (most recent call last):
  File "hello.py", line 2, in <module>
    print(name + 5)
          ~~~~~~~~^~
TypeError: can only concatenate str (not "int") to str
```

**How to read it:**

1. Start at the **last line** — that is the actual error: `TypeError: can only concatenate str (not "int") to str`
2. Look at the **file and line number**: `line 2`
3. Look at the **highlighted code**: `print(name + 5)`
4. Fix it

---

### Common Error Types

| Error | What it means | Common cause |
|-------|--------------|-------------|
| `SyntaxError` | Python cannot parse the line | Missing colon, quote, or bracket |
| `IndentationError` | Wrong indentation | Mixed tabs/spaces, unexpected indent |
| `NameError` | Variable used before being defined | Typo in variable name, wrong scope |
| `TypeError` | Wrong type for the operation | Adding str and int, calling a non-function |
| `ValueError` | Right type, wrong value | `int("hello")`, `int("")` |
| `ZeroDivisionError` | Division by zero | `x / 0` |
| `IndexError` | Accessing a list index that does not exist | `scores[10]` when list has 4 items |
| `KeyError` | Accessing a dict key that does not exist | `student["grade"]` when key is missing |

---

## 7. VS Code Features Worth Knowing

---

### IntelliSense

As you type, VS Code suggests completions powered by Pylance. Press `Tab` or `Enter` to accept. It also shows function signatures when you open a parenthesis.

---

### Hover Documentation

Hover over any built-in like `print`, `len`, or `range` — VS Code shows a description, parameters, and return type inline.

---

### Problems Panel

Errors and warnings appear underlined in the editor. Open the full list with `Ctrl + Shift + M`. Fix these before running — most are caught before execution.

---

### Inline Error Lens

If you installed the **Error Lens** extension from Guide 02, errors appear inline next to the code as you type. This is faster than checking the Problems panel.

---

### Terminal

Open with `` Ctrl + ` ``. This is where you run `.py` files, activate virtual environments, install packages, and use Git. Keep it open while working.

---

### Find and Replace

`Ctrl + H` — find and replace across the file. Use `Ctrl + D` to select the next occurrence of the highlighted word — useful for renaming a variable in multiple places.

---

### Multiple Cursors

`Alt + Click` — places a cursor at each click point. Edit all positions simultaneously. Useful for adding the same text to multiple lines at once.

---

## 8. Quick Reference Card

```
RUNNING CODE
------------
.py file     Ctrl + F5
             python hello.py  (terminal)
REPL         python  (terminal) → >>>
Notebook     Shift + Enter on a cell


SYNTAX RULES
------------
No semicolons at line ends
No curly braces — use indentation (4 spaces)
No type declarations — Python infers type
Block headers end with colon:  if x > 0:
Boolean:  True / False  (capital)
Null:     None
Increment: i += 1  (no i++)


COMMENTS
--------
# single line
"""
multi-line
"""


ARITHMETIC
----------
+    addition          5 + 3   = 8
-    subtraction       5 - 3   = 2
*    multiplication    5 * 3   = 15
/    division          7 / 2   = 3.5   (always float)
//   floor division    7 // 2  = 3     (drops decimal)
%    modulo            7 % 2   = 1     (remainder)
**   exponentiation    2 ** 8  = 256


COMMON ERRORS
-------------
SyntaxError       missing colon, quote, or bracket
IndentationError  wrong or inconsistent indentation
NameError         variable used before being defined
TypeError         wrong type for operation (str + int)
ValueError        right type, wrong value  int("hello")
ZeroDivisionError division by zero


PYTHON vs JAVA/C
----------------
Java/C              Python
System.out.println  print()
{}                  indentation
int x = 5;          x = 5
true / false        True / False
null / NULL         None
i++                 i += 1
else if             elif
```

---

You are ready for Module 01.

[Back to Setup Overview](./README.md)
[Go to M01 — Variables and Data Types](../M01-Variables-and-Data-Types/README.md)
