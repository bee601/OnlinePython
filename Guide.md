# PyCode - Setup & User Guide

## 📦 Installation & Setup

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No installation or dependencies required!

### Getting Started

#### 1. **Direct Use (Easiest)**
```bash
# Download python-editor.html
# Double-click to open in your default browser
# Start coding immediately!
```

#### 2. **Local Server** (Recommended for Development)
```bash
# Navigate to the project directory
cd pycode

# Start a local server (Python 3)
python -m http.server 8000

# Open browser and visit:
# http://localhost:8000/python-editor.html
```

#### 3. **GitHub Pages** (For Sharing)
```bash
# 1. Create a GitHub repository
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/pycode.git
git push -u origin main

# 2. Enable GitHub Pages in repository settings
# Settings → Pages → Source: main branch → Save

# 3. Access at:
# https://yourusername.github.io/python-editor.html
```

---

## 🎮 How to Use

### Writing Code

1. **Open the editor** in your browser
2. **Type or paste Python code** in the left panel
3. **Click Run** (▶ button) or press `Ctrl/Cmd + Enter`
4. **View output** in the right panel

### Example: Simple Hello World
```python
print("Hello, World!")
```

Expected output:
```
Hello, World!
```

### Example: Working with Variables
```python
# Define variables
name = "Alice"
age = 30

# Print formatted output
print(f"{name} is {age} years old")
print(f"In 10 years, {name} will be {age + 10}")
```

Expected output:
```
Alice is 30 years old
In 10 years, Alice will be 40
```

### Example: Using Libraries
```python
import math
import json

# Math operations
radius = 5
area = math.pi * radius ** 2
print(f"Circle area: {area:.2f}")

# JSON manipulation
data = {"name": "Bob", "hobbies": ["coding", "gaming"]}
json_str = json.dumps(data)
print(json_str)
```

---

## 🔗 Sharing Your Code

### Step-by-Step Sharing

1. **Write your code** in the editor
2. **Click the Share button** (⚡) in the top-right
3. **Copy the generated URL** from the modal
4. **Share anywhere**: GitHub issues, discussions, Discord, emails, etc.

### What Gets Shared
- Your complete Python code
- URL is self-contained (no server needed to share!)
- Anyone can open, view, modify, and run it

### Example Share Flow
```
Original Code:
    print("Check this out!")
    
↓ Click Share ↓

Get URL:
    https://example.com/python-editor.html?code=cHJpbnQoIkNoZWNrIHRoaXMgb3V0ISIp
    
↓ Send to friend ↓

Friend opens URL:
    Can see your code AND run it immediately!
```

---

## 🐛 Troubleshooting

### "Python is loading..." takes too long
- **Solution**: First load takes time (30-60 seconds) as Pyodide initializes
- Subsequent runs are much faster
- Check your internet connection

### Code runs but no output appears
- **Check**: Did you use `print()`?
- Python code without `print()` won't show visible results
- Example:
```python
# ❌ No output visible
5 + 5

# ✅ Shows output
print(5 + 5)  # Output: 10
```

### ImportError: No module named 'X'
- **Reason**: Some modules aren't available in the browser
- **Solution**: Use only standard library modules that Pyodide supports
- Supported: `math`, `random`, `json`, `collections`, `re`, `itertools`, etc.
- Not supported: `requests`, `numpy`, `pandas`, `os`, `subprocess`

### Code seems to hang or freeze
- **Reason**: Infinite loop or very slow computation
- **Solution**: Reload the page (this clears the Python runtime)
- Add timeout logic to your code

### Error: "SyntaxError: invalid syntax"
- **Check**: Python syntax is correct
- Use proper indentation (4 spaces)
- Close all brackets, quotes, parentheses

---

## 📚 Supported Python Features

### ✅ Fully Supported

**Data Structures**
```python
# Lists
my_list = [1, 2, 3, 4, 5]
my_list.append(6)
print(my_list)

# Dictionaries
person = {"name": "Alice", "age": 30}
print(person["name"])

# Sets & Tuples
my_set = {1, 2, 3}
my_tuple = (1, 2, 3)

# List comprehensions
squares = [x**2 for x in range(10)]
print(squares)
```

**String Operations**
```python
text = "Hello, World!"
print(text.upper())
print(text.lower())
print(text.replace("World", "Python"))

# String formatting
name = "Bob"
age = 25
print(f"{name} is {age} years old")
```

**Control Flow**
```python
# If/Else
if age >= 18:
    print("Adult")
else:
    print("Minor")

# Loops
for i in range(5):
    print(i)

while counter < 10:
    print(counter)
    counter += 1
```

**Functions**
```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

print(greet("Alice"))
print(greet("Bob", "Hi"))
```

**Math & Logic**
```python
import math
import random

# Math functions
print(math.sqrt(16))
print(math.sin(math.pi / 2))

# Random numbers
print(random.randint(1, 100))
print(random.choice([1, 2, 3, 4, 5]))
```

**JSON Handling**
```python
import json

data = {"name": "Alice", "scores": [95, 87, 92]}
json_string = json.dumps(data)
parsed = json.loads(json_string)
print(parsed)
```

### ❌ NOT Supported

**File Operations**
```python
# Cannot use:
with open("file.txt") as f:
    content = f.read()
```

**Network Requests**
```python
# Cannot use:
import requests
response = requests.get("https://api.example.com")
```

**System Access**
```python
# Cannot use:
import os
import subprocess
os.system("echo hello")
```

**External Packages**
```python
# Cannot use (unless in Pyodide):
import numpy
import pandas
import requests
import flask
```

---

## 🎨 Customization Guide

### Change Colors

Edit the CSS variables in `python-editor.html` (around line 30):

```css
:root {
    --primary: #00d4ff;      /* Primary cyan color */
    --secondary: #ff006e;    /* Secondary magenta */
    --bg-dark: #0a0e27;      /* Dark background */
    --text-primary: #e0e6ff; /* Main text color */
    --text-secondary: #8892b0; /* Secondary text */
    --success: #00ff88;      /* Success/green */
    --error: #ff4757;        /* Error/red */
}
```

**Example: Dark Blue Theme**
```css
:root {
    --primary: #2563eb;      /* Blue */
    --secondary: #7c3aed;    /* Purple */
    --bg-dark: #0f172a;      /* Dark blue */
    --text-primary: #f1f5f9; /* White text */
    --success: #10b981;      /* Green */
    --error: #ef4444;        /* Red */
}
```

### Change Default Code

Find this section in the JavaScript:
```javascript
if (!codeEditor.value) {
    codeEditor.value = `# Python Editor - Schreib hier deinen Code!
print("🐍 Willkommen zu PyCode!")
...`;
    updateHighlight();
}
```

Replace with your own default code:
```javascript
if (!codeEditor.value) {
    codeEditor.value = `# Your default code here
print("Welcome to PyCode!")`;
    updateHighlight();
}
```

### Change Font

Find the `html, body` CSS rule and modify:
```css
html, body {
    font-family: 'JetBrains Mono', 'Courier New', monospace;
}
```

Popular monospace fonts:
- `'JetBrains Mono'`
- `'Cascadia Code'`
- `'IBM Plex Mono'`
- `'Ubuntu Mono'`
- `'Consolas'`

---

## 🚀 Advanced Usage

### Embedding in HTML

You can embed PyCode in your own website:

```html
<iframe src="https://your-site.com/python-editor.html" 
        width="100%" 
        height="600px"
        style="border: 1px solid #ccc;"></iframe>
```

### Pre-loading Code in Embed

```html
<iframe src="https://your-site.com/python-editor.html?code=cHJpbnQoIkhlbGxvIikK" 
        width="100%" 
        height="600px"></iframe>
```

### Creating Shareable Code Examples

```python
# Example for GitHub Issue
```python
# My code
numbers = [1, 2, 3, 4, 5]
print([x**2 for x in numbers])
```

**Try it online**: https://your-site.com/python-editor.html?code=...
```

---

## 📝 Tips & Tricks

### Tip 1: Use Clear Variable Names
```python
# Good
user_age = 25
user_name = "Alice"

# Avoid
a = 25
n = "Alice"
```

### Tip 2: Add Comments
```python
# Calculate area of circle
import math
radius = 5
area = math.pi * radius ** 2
print(f"Area: {area:.2f}")
```

### Tip 3: Test Step-by-Step
```python
# Build complex code gradually
# First: get data
data = [1, 2, 3, 4, 5]
print(data)

# Then: process it
squared = [x**2 for x in data]
print(squared)

# Finally: analyze
print(f"Sum: {sum(squared)}")
```

### Tip 4: Use F-strings for Output
```python
# Modern and readable
name = "Bob"
age = 30
print(f"{name} is {age} years old")

# Instead of
print(name + " is " + str(age) + " years old")
```

---

## 🤝 Getting Help

### Common Resources
- [Python Docs](https://python.org/docs)
- [Python Tutorial](https://docs.python.org/3/tutorial/)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/python)

### Reporting Issues
- Open an issue on GitHub
- Include code snippet that breaks
- Describe expected vs actual behavior
- Browser and OS information

---

**Happy coding! 🐍✨**
