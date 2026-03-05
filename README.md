# 🐍 PyCode - Python Editor & Executor

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen.svg)
![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)

A modern, **browser-based Python editor** with live execution capabilities. Write, test, and share Python code—all without installation!

## ✨ Features

### 🎯 Core Functionality
- **Live Execution**: Execute Python code directly in your browser (powered by Pyodide)
- **Syntax Highlighting**: Real-time syntax highlighting for Python code
- **Output Capture**: All `print()` statements are captured and displayed live
- **Error Handling**: Clear error messages with proper formatting
- **Execution Time**: Display code execution time in milliseconds

### 🔗 Share & Collaborate
- **URL Sharing**: Code is automatically encoded and embedded in URLs
- **Persistent Links**: Share your code snippets with simple shareable links
- **One-Click Copy**: Share modal with easy copy-to-clipboard functionality
- **Perfect for GitHub**: Ideal for sharing code snippets in issues, discussions, and documentation

### 🎨 Design & UX
- **Modern Dark Theme**: Cyberpunk-inspired design with cyan and magenta accents
- **Responsive Layout**: Works seamlessly on desktop, tablet, and mobile
- **Smooth Animations**: Polished micro-interactions and transitions
- **Split View**: Editor on the left, output on the right
- **Custom Scrollbars**: Styled scrollbars that match the aesthetic

## 🚀 Quick Start

### Option 1: Online (Recommended)
Simply open `python-editor.html` in your browser. No server required!

```bash
# Clone the repository
git clone https://github.com/yourusername/pycode.git
cd pycode

# Open in browser
open python-editor.html
# or on Linux:
xdg-open python-editor.html
# or on Windows:
start python-editor.html
```

### Option 2: Using Python's Built-in Server
```bash
# Python 3.x
python -m http.server 8000

# Then visit: http://localhost:8000/python-editor.html
```

### Option 3: Deploy to GitHub Pages
1. Fork this repository
2. Rename to `yourusername.github.io` (or any name)
3. Push your changes
4. Access at `https://yourusername.github.io/python-editor.html`

## 📖 Usage Guide

### Basic Coding
1. Write Python code in the left editor panel
2. Click the **Run** button (▶) or press `Ctrl/Cmd + Enter`
3. See output in the right panel immediately

### Sharing Code
1. Write or edit your Python code
2. Click the **Share** button (⚡)
3. Copy the generated URL
4. Share it anywhere—anyone can open and modify your code

### Example Share URL
```
https://example.com/python-editor.html?code=cHJpbnQoIkhlbGxvIFdvcmxkISIp
```

## 💡 Examples

### Hello World
```python
print("Hello, World!")
```

### List Comprehension
```python
numbers = [1, 2, 3, 4, 5]
squares = [x**2 for x in numbers]
print(f"Squares: {squares}")
```

### Functions
```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

for i in range(10):
    print(fibonacci(i), end=" ")
```

### Data Processing
```python
data = {"name": "Alice", "age": 30, "skills": ["Python", "JavaScript"]}
print(f"Name: {data['name']}")
print(f"Age: {data['age']}")
print(f"Skills: {', '.join(data['skills'])}")
```

## 🛠️ Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Runtime**: [Pyodide](https://pyodide.org/) (Python in WebAssembly)
- **Syntax Highlighting**: [highlight.js](https://highlightjs.org/)
- **No Dependencies**: Pure client-side, no build tools required

## 🌟 How It Works

1. **Code Input**: You write Python in the editor
2. **Syntax Highlighting**: JavaScript highlights the code in real-time
3. **Execution**: Pyodide (Python compiled to WebAssembly) executes the code in your browser
4. **Output Capture**: JavaScript intercepts `sys.stdout` and displays results
5. **Sharing**: Code is Base64-encoded and added to the URL as a query parameter

## ⚠️ Limitations

- **No File System Access**: Cannot read/write local files
- **No Network Requests**: Cannot make HTTP requests (security sandbox)
- **Subset of Python**: Some standard library modules may not be available
- **Memory Limits**: Browser memory constraints apply
- **Execution Timeout**: Very long-running scripts may timeout

### Not Supported
```python
# ❌ File operations
with open("file.txt") as f:
    data = f.read()

# ❌ Network requests
import requests
response = requests.get("https://api.example.com")

# ❌ Some system modules
import os
import subprocess
```

### Well Supported
```python
# ✅ Data structures
lists, dicts, sets, tuples

# ✅ Math & logic
math, random, statistics

# ✅ String operations
str methods, re (regex)

# ✅ Functional programming
map, filter, lambda, list comprehensions

# ✅ JSON
import json

# ✅ Collections
from collections import defaultdict, Counter
```

## 🎨 Customization

### Change Color Scheme
Edit the CSS variables in `python-editor.html`:

```css
:root {
    --primary: #00d4ff;      /* Cyan */
    --secondary: #ff006e;    /* Magenta */
    --bg-dark: #0a0e27;      /* Background */
    --text-primary: #e0e6ff; /* Main text */
    --success: #00ff88;      /* Success color */
    --error: #ff4757;        /* Error color */
}
```

### Add Default Code
Replace the default code in the JavaScript section:

```javascript
if (!codeEditor.value) {
    codeEditor.value = `# Your default code here`;
    updateHighlight();
}
```

### Change Editor Font
Modify the font-family in CSS:

```css
html, body {
    font-family: 'Your-Font-Name', monospace;
}
```

## 🤝 Contributing

Contributions are welcome! Here's how to help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Ideas for Contributions
- [ ] Dark/Light theme toggle
- [ ] Code formatting (Black formatter)
- [ ] Multiple file support
- [ ] Code execution history
- [ ] Keyboard shortcuts reference modal
- [ ] Download code as `.py` file
- [ ] Import code from URL
- [ ] Collaborative editing (WebSocket)
- [ ] Code templates/snippets
- [ ] Line numbers in editor

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Pyodide**: For bringing Python to the browser
- **highlight.js**: For beautiful syntax highlighting
- **Modern Design Principles**: For the cyberpunk aesthetic

## 📞 Support & Feedback

- **Issues**: Report bugs on [GitHub Issues](https://github.com/yourusername/pycode/issues)
- **Discussions**: Join conversations on [GitHub Discussions](https://github.com/yourusername/pycode/discussions)

## 🗺️ Roadmap

### Version 1.1 (Coming Soon)
- [ ] Keyboard shortcuts
- [ ] Code formatting
- [ ] Multiple tabs/files
- [ ] Execution history

### Version 1.2 (Planned)
- [ ] Theme switcher
- [ ] Code snippets library
- [ ] Download as `.py` file
- [ ] Import from GitHub Gist

### Version 2.0 (Future)
- [ ] Collaborative editing
- [ ] Code comments & annotations
- [ ] Performance profiling
- [ ] Package management (pip alternative)

## 🔗 Related Links

- [Pyodide Documentation](https://pyodide.org/)
- [Python Official Docs](https://python.org/docs)
- [WebAssembly Info](https://webassembly.org/)

---

**Made with ❤️ for the Python community**

⭐ If you like this project, please consider giving it a star on GitHub!
