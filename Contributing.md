# Contributing to PyCode

Thank you for your interest in contributing to PyCode! This document provides guidelines and instructions for contributing.

## 🎯 Code of Conduct

Be respectful, inclusive, and constructive in all interactions. We welcome contributors of all experience levels.

## 🚀 Getting Started

### Fork & Clone
```bash
# Fork the repository on GitHub
# Then clone your fork
git clone https://github.com/YOUR-USERNAME/pycode.git
cd pycode
```

### Create a Branch
```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

## 📝 Types of Contributions

### 🐛 Bug Reports
Found a bug? Create an issue with:
- **Description**: What's the problem?
- **Steps to reproduce**: How to trigger it?
- **Expected behavior**: What should happen?
- **Actual behavior**: What actually happens?
- **Browser & OS**: Which environment?

### 💡 Feature Requests
Have an idea? Open an issue with:
- **Description**: What feature?
- **Use case**: Why is it needed?
- **Example usage**: How would it work?

### 🔧 Code Contributions

#### Areas for Improvement
- [ ] Dark/Light theme toggle
- [ ] Keyboard shortcuts (Ctrl+S to save, Ctrl+Enter to run)
- [ ] Code formatting (Black formatter integration)
- [ ] Multiple file/tab support
- [ ] Execution history panel
- [ ] Keyboard shortcuts reference modal
- [ ] Download code as `.py` file
- [ ] Import code from GitHub Gist
- [ ] Line numbers in editor
- [ ] Code minimap
- [ ] Undo/Redo functionality
- [ ] Search & replace
- [ ] Snippet templates
- [ ] Performance improvements
- [ ] Accessibility improvements

#### Before You Start
1. Check existing issues to avoid duplicate work
2. Discuss major changes in an issue first
3. Keep commits atomic and focused

#### Making Changes
```bash
# Make your changes
# Test thoroughly in multiple browsers
# Keep code clean and commented

# Stage your changes
git add .

# Commit with clear message
git commit -m "Add: feature description" 
# or
git commit -m "Fix: bug description"
# or  
git commit -m "Refactor: improvement description"
```

#### Commit Message Format
```
<type>: <subject>

<body (optional)>
```

Types: `Add`, `Fix`, `Refactor`, `Docs`, `Style`, `Test`, `Performance`

Examples:
- `Add: dark/light theme toggle`
- `Fix: syntax highlighting for f-strings`
- `Refactor: output display logic`
- `Docs: update README with examples`

### 📚 Documentation

Help improve docs:
- Update README with clearer examples
- Add FAQ section
- Create video tutorials
- Improve comments in code
- Write blog posts about features

## ✅ Pull Request Process

1. **Update your branch** with latest main
   ```bash
   git fetch origin
   git rebase origin/main
   ```

2. **Write a clear PR title** and description
   ```
   Title: Add dark/light theme toggle
   
   Description:
   - Adds theme preference in settings
   - Saves preference to localStorage
   - Includes smooth transition animation
   - Tested on Chrome, Firefox, Safari
   ```

3. **Ensure quality**
   - Test in multiple browsers (Chrome, Firefox, Safari, Edge)
   - Test on desktop and mobile
   - No console errors or warnings
   - Code is properly formatted

4. **Create the PR**
   ```bash
   git push origin feature/your-feature-name
   # Visit GitHub and click "Create Pull Request"
   ```

5. **Respond to feedback**
   - Review comments respectfully
   - Make requested changes
   - Re-push to update PR

## 🧪 Testing Your Changes

### Manual Testing Checklist
- [ ] Feature works as expected
- [ ] No JavaScript errors in console
- [ ] Tested on Chrome
- [ ] Tested on Firefox
- [ ] Tested on Safari
- [ ] Tested on mobile device
- [ ] Backward compatible (doesn't break existing features)

### Browser Testing
```bash
# Use multiple browsers or BrowserStack for testing
# Minimum browser versions:
# - Chrome 90+
# - Firefox 88+
# - Safari 14+
# - Edge 90+
```

## 🎨 Code Style Guidelines

### HTML
```html
<!-- Use semantic HTML -->
<button id="runBtn" class="btn-primary">Run</button>

<!-- Proper indentation (2 spaces for HTML) -->
<div class="container">
  <div class="header">
    <h1>Title</h1>
  </div>
</div>
```

### CSS
```css
/* Use CSS variables */
color: var(--text-primary);
background: var(--bg-dark);

/* Group related properties */
.button {
  /* Layout */
  padding: 10px 20px;
  display: flex;
  align-items: center;
  
  /* Appearance */
  background: var(--primary);
  border: none;
  border-radius: 6px;
  
  /* Typography */
  font-size: 14px;
  font-weight: 600;
  
  /* Interaction */
  cursor: pointer;
  transition: all 0.2s ease;
}
```

### JavaScript
```javascript
// Use descriptive variable names
const codeEditor = document.getElementById('code');

// Use const by default, let if needed
const TIMEOUT = 5000;

// Add comments for complex logic
function executeCode(code) {
    // Capture stdout before execution
    const capture = new OutputCapture();
    
    // Run the code
    try {
        pyodide.runPythonAsync(code);
    } catch (error) {
        console.error('Execution error:', error);
    }
}

// Use template literals
const message = `${count} items found`;

// Keep functions focused and small
function updateOutput(text, type) {
    const line = document.createElement('div');
    line.className = `output-line ${type}`;
    line.textContent = text;
    return line;
}
```

## 📊 Project Structure
```
pycode/
├── python-editor.html       # Main application
├── README.md                # Main documentation
├── GUIDE.md                 # User guide
├── CONTRIBUTING.md          # This file
├── LICENSE                  # MIT License
├── .gitignore               # Git ignore rules
└── examples/                # Example code snippets
    ├── hello-world.py
    ├── list-comprehension.py
    ├── fibonacci.py
    └── data-processing.py
```

## 🔍 Code Review

### What We Look For
- ✅ Works as intended
- ✅ Doesn't break existing features
- ✅ Code is clean and understandable
- ✅ Follows project style guidelines
- ✅ Performance is acceptable
- ✅ Properly documented/commented

### Providing Feedback
Be constructive and specific:
```
✅ Good feedback:
"This could be more performant by caching the DOM element. See: [link]"

❌ Bad feedback:
"This code sucks"
```

## 📈 Development Tips

### Debugging
```javascript
// Use console for debugging
console.log('Value:', value);
console.error('Error:', error);
console.time('label');
// ... code ...
console.timeEnd('label');
```

### Testing Output Capture
```javascript
// Check what's being captured
console.log('Captured output:', capturedOutput);
```

### Performance Profiling
```javascript
// Use browser DevTools
// Press F12 → Performance tab
// Record action and analyze timeline
```

## 🎓 Learning Resources

### For JavaScript
- [MDN Web Docs](https://developer.mozilla.org/)
- [JavaScript.info](https://javascript.info/)

### For Python
- [Python Docs](https://python.org/docs)
- [Real Python](https://realpython.com/)

### For Pyodide
- [Pyodide Docs](https://pyodide.org/en/stable/)
- [Pyodide GitHub](https://github.com/pyodide/pyodide)

### For Web Design
- [MDN CSS Guide](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Web.dev](https://web.dev/)

## 🚨 Important Notes

### Don't
- ❌ Introduce breaking changes without discussion
- ❌ Add large external dependencies
- ❌ Remove existing features
- ❌ Push directly to main (always use PR)

### Do
- ✅ Keep features focused and small
- ✅ Write clear commit messages
- ✅ Test thoroughly
- ✅ Update documentation
- ✅ Be respectful in discussions

## 📞 Questions?

- Open a discussion on GitHub
- Check existing issues for similar questions
- Review the GUIDE.md for usage questions

## 🎉 Thank You!

Your contributions make PyCode better for everyone. Thank you for helping! 🙌

---

Happy contributing! 💻✨
