# 🐍 PyCode Pro - Complete User Guide

Welcome to **PyCode Pro** - a professional Python code editor and learning tool with syntax highlighting, templates, and command suggestions!

---

## 📋 Table of Contents

1. [Getting Started](#getting-started)
2. [Interface Overview](#interface-overview)
3. [Templates](#templates)
4. [Commands](#commands)
5. [Running Code](#running-code)
6. [Tips & Tricks](#tips--tricks)

---

## Getting Started

### What is PyCode Pro?

PyCode Pro is an **interactive Python editor** that allows you to:
- ✅ Write Python code in a modern editor
- ✅ Run Python code and see output instantly
- ✅ Learn from 15+ working example programs
- ✅ Access 40+ Python commands with descriptions
- ✅ Download your code as `.py` files
- ✅ Syntax highlighting for better readability

### Opening PyCode Pro

1. Open the `index.html` file in your web browser
2. The editor loads automatically with a default "Hello, World!" program
3. Your code is auto-saved to your browser!

---

## Interface Overview

### Main Components

```
┌─────────────────────────────────────────────────┐
│  🐍 PyCode Pro      [▶ Run] [⬇ Download] [Clear]│  ← Navbar
├──────────────────────────┬──────────────────────┤
│                          │                      │
│   Python Code Editor     │   Output Console     │  ← Main Area
│   (Left Panel)           │   (Right Panel)      │
│                          │                      │
├──────────────────────────┴──────────────────────┤
│ [📚 Templates]  [🔧 Commands]  ← Bottom Buttons│
└─────────────────────────────────────────────────┘
```

### The Navbar

- **🐍 PyCode Pro** - Logo/title
- **▶ Run** - Execute your code
- **⬇ Download** - Save code as `.py` file
- **Clear** - Clear the output panel

### Editor Panel (Left)

- Write and edit Python code here
- **Syntax highlighting** - Keywords, strings in different colors
- **Auto-save** - Code saved automatically to browser storage
- Indent properly with 4 spaces per level

### Output Panel (Right)

- Shows output from your program
- Displays errors if something goes wrong
- Clear with the "Clear" button

### Bottom Buttons

- **📚 Templates** - Open templates sidebar (15+ programs)
- **🔧 Commands** - Open commands sidebar (40+ commands)

---

## Templates

### What are Templates?

**Templates** are complete, working Python programs. Each demonstrates a Python concept or technique.

### How to Use Templates

1. Click **📚 Templates** button
2. Sidebar opens on the left
3. Choose a template - shows Name + Description
4. Click to load it into editor
5. Click **▶ Run** to execute

### Available Templates (15)

| Template | Description |
|----------|-------------|
| Hello World | Print text to screen |
| Numbers 1-5 | Loop with range() |
| Sum Numbers | Calculate list sum |
| Count to 10 | For loop demo |
| Multiplication | Multiply variables |
| Grades | If/else conditional |
| List Loop | Iterate through list |
| Even Numbers | Filter with modulo |
| Countdown | Reverse range loop |
| Average | Calculate average |
| If-Else | Conditional branches |
| Stars | Pattern printing |
| Times Table | Nested multiplication |
| Length Check | Get list length |
| Double Numbers | Loop with math |

---

## Commands

### What are Commands?

**Commands** are Python keywords and functions with descriptions. Click to insert them at your cursor.

### How to Use Commands

1. Click **🔧 Commands** button
2. Sidebar opens with all commands
3. Each shows: Name + Description
4. Click to insert at cursor position
5. Edit and complete the command

### Available Commands (40+)

#### Control Flow
- `print()` - Output text or numbers
- `for` - Loop through items
- `if` - Execute if condition true
- `else` - Execute if condition false
- `elif` - Check another condition

#### Data & Collections
- `[1, 2, 3]` - Create list
- `range()` - Sequence of numbers
- `len()` - Get length
- `sum()` - Add all items

#### String Methods
- `.upper()` - UPPERCASE text
- `.lower()` - lowercase text
- `.split()` - Split into words
- `.join()` - Combine list to text
- `.replace()` - Replace text
- `.strip()` - Remove spaces
- `.count()` - Count occurrences
- `.find()` - Find position

#### Operators
- `x + y` - Add numbers
- `x - y` - Subtract
- `x * y` - Multiply
- `x / y` - Divide
- `x % y` - Remainder
- `x == y` - Equal?
- `x > y` - Greater than?
- `x < y` - Less than?
- `x >= y` - Greater/equal?
- `x <= y` - Less/equal?
- `x != y` - Not equal?

#### Logic
- `and` - Both true
- `or` - At least one true
- `not` - Reverse true/false

#### Type Conversion
- `int()` - To integer
- `str()` - To text
- `max()` - Find largest
- `min()` - Find smallest
- `type()` - Check type

---

## Running Code

### Execute Your Programs

1. Write or load code
2. Click **▶ Run** button
3. Output appears in right panel
4. Errors show in red

### Downloading Code

1. Click **⬇ Download** button
2. File `code.py` downloads
3. Open in text editor or Python IDE
4. Run with: `python code.py`

### Clearing Output

1. Click **Clear** button
2. Output resets to "Ready"

---

## Learning Examples

### Example 1: Print Text

```python
print("Hello, World!")
print("Welcome to Python!")
```

**Output:**
```
Hello, World!
Welcome to Python!
```

### Example 2: Loop with Range

```python
for i in range(1, 6):
    print(i)
```

**Output:**
```
1
2
3
4
5
```

### Example 3: Variables and Math

```python
x = 10
y = 5
print(f"{x} + {y} = {x + y}")
```

**Output:**
```
10 + 5 = 15
```

### Example 4: If-Else

```python
score = 85
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
else:
    print("C")
```

**Output:**
```
B
```

### Example 5: List Sum

```python
numbers = [10, 20, 30, 40]
total = sum(numbers)
print(f"Total: {total}")
```

**Output:**
```
Total: 100
```

---

## Tips for Success

### 1. Start Simple
Begin with short programs (5-10 lines)

### 2. Use Templates
Learn from working examples

### 3. Read Descriptions
Every template and command has one

### 4. Indent Correctly
4 spaces per indentation level

### 5. Check Syntax
- Colons after `if:`, `for:`, etc.
- Matching parentheses
- Correct spelling

### 6. Use F-Strings
```python
name = "Alice"
print(f"Hello, {name}!")
```

### 7. Test Often
Run code frequently to catch errors early

### 8. Add Comments
```python
# This is a comment
x = 5  # Store a number
```

---

## Common Issues

| Problem | Solution |
|---------|----------|
| Code won't run | Check indentation and colons |
| Wrong output | Verify variable names and math |
| Weird characters | Check string quotes match |
| Loop not working | Ensure proper indentation |

---

## Quick Reference

### Data Types
- `"text"` - String
- `42` - Integer
- `3.14` - Float
- `[1, 2, 3]` - List
- `True/False` - Boolean

### Common Patterns

**Print variable:**
```python
x = 10
print(x)
```

**Loop 1-10:**
```python
for i in range(1, 11):
    print(i)
```

**Check condition:**
```python
if x > 5:
    print("Big")
else:
    print("Small")
```

**Sum a list:**
```python
nums = [1, 2, 3, 4, 5]
total = sum(nums)
print(total)
```

---

## Learning Path

**Step 1 - Beginner**
- Load "Hello World" template
- Load "Numbers 1-5" template
- Write your own print statements

**Step 2 - Intermediate**
- Load "Grades" template
- Load "Even Numbers" template
- Mix templates together

**Step 3 - Advanced**
- Write from scratch
- Use commands as reference
- Download and modify

---

## Features

✅ 15+ working templates
✅ 40+ commands with descriptions
✅ Syntax highlighting
✅ Auto-save to browser
✅ Download as .py
✅ Instant execution
✅ Error messages
✅ Modern design

---

## Keyboard Tips

- **Tab** - Indent
- **Shift+Tab** - Unindent
- **Ctrl+A** - Select all
- **Click Template** - Load program
- **Click Command** - Insert command

---

## Need Help?

1. Check this guide
2. Look at templates for examples
3. Read command descriptions
4. Start with a simple program
5. Build up gradually

---

**Happy Coding! 🚀**

*PyCode Pro - Making Python easy and fun*

Version 1.0
