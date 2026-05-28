# Development Guide

This guide covers development setup, architecture, and best practices for My First Bot.

## 🏗️ Architecture Overview

The bot follows a simple, modular structure:

```
Bot Startup
    ↓
Console Logging
    ↓
Task Execution
    ↓
File Logging
    ↓
Completion Status
```

## 🔨 Development Setup

### Prerequisites

- Python 3.7+
- Git
- Text editor or IDE (VS Code, PyCharm, etc.)

### Initial Setup

```bash
# Clone the repository
git clone https://github.com/gasukwo52-commits/my-first-bot.git
cd my-first-bot

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## 📁 Project Structure

```
my-first-bot/
├── bot.py                    # Main bot script
├── requirements.txt          # Python dependencies
├── README.md                # User documentation
├── CONTRIBUTING.md          # Contribution guidelines
├── DEVELOPMENT.md           # This file
├── LICENSE                  # MIT License
└── .github/
    └── workflows/           # CI/CD configuration
```

## 🔧 Common Development Tasks

### Running the Bot

```bash
python bot.py
```

### Viewing Logs

```bash
# Display all logs
cat log.txt

# Display last 10 lines
tail -10 log.txt

# Clear logs
> log.txt  # Unix/Mac
or
del log.txt  # Windows
```

### Adding a New Feature

1. Create a feature branch:
   ```bash
   git checkout -b feature/my-feature
   ```

2. Modify `bot.py`:
   ```python
   def my_new_feature():
       """Description of what this function does."""
       print("Running my new feature...")
       with open("log.txt", "a") as f:
           f.write("My new feature ran successfully!\n")
   ```

3. Call the function in main execution
4. Test thoroughly
5. Commit and push

### Running Tests

Currently, the project doesn't have automated tests. Consider adding:

```bash
# Example: Create tests directory
mkdir tests
touch tests/__init__.py
touch tests/test_bot.py
```

Basic test template:
```python
import os
import unittest
from unittest.mock import patch, mock_open

class TestBot(unittest.TestCase):
    def test_log_creation(self):
        """Test that logs are created successfully."""
        # Add your test here
        pass

if __name__ == '__main__':
    unittest.main()
```

## 🐛 Debugging

### Debug Mode

Add debug output to understand bot execution:

```python
import sys

DEBUG = True

def debug_print(message):
    if DEBUG:
        print(f"[DEBUG] {message}", file=sys.stderr)

debug_print("Bot initialized")
```

### Common Issues

| Issue | Solution |
|-------|----------|
| ModuleNotFoundError | Install dependencies: `pip install -r requirements.txt` |
| Permission denied | Check file permissions: `chmod +x bot.py` |
| Cannot write log | Verify write permissions to directory |

## 📊 Performance Considerations

For a bot this size, performance isn't critical, but consider:

- **File I/O:** Minimize log file writes
- **Memory:** Monitor for memory leaks
- **Execution time:** Keep tasks responsive

Example optimization:
```python
# Batch log writes instead of single writes
log_entries = []
log_entries.append("Task 1 completed")
log_entries.append("Task 2 completed")

with open("log.txt", "a") as f:
    f.write("\n".join(log_entries) + "\n")
```

## 🔐 Security Best Practices

For this learning project:

1. **Avoid hardcoded secrets** - Use environment variables
2. **Validate input** - Even if from trusted sources
3. **Sanitize logs** - Don't log sensitive information
4. **Keep dependencies updated** - Regular `pip list --outdated`

Example secure logging:
```python
# Bad
password = "secret123"
with open("log.txt", "a") as f:
    f.write(f"Password: {password}\n")

# Good
import os
log_message = os.environ.get('BOT_STATUS', 'running')
with open("log.txt", "a") as f:
    f.write(f"Status: {log_message}\n")
```

## 📦 Dependency Management

### Updating requirements.txt

After installing new packages:
```bash
pip freeze > requirements.txt
```

### Checking for outdated packages

```bash
pip list --outdated
```

### Upgrading packages

```bash
pip install --upgrade package-name
```

## 🚀 Deployment

### Local Deployment

1. Ensure dependencies are installed
2. Test locally: `python bot.py`
3. Verify logs are created

### CI/CD Pipeline

The repository uses GitHub Actions (see `.github/workflows/`).

Current workflow: Azure WebApps Node.js deployment

To modify the workflow:
```bash
# Edit the workflow file
nano .github/workflows/azure-webapps-node.yml
```

## 📚 Learning Resources

- [Python Documentation](https://docs.python.org/3/)
- [PEP 8 Style Guide](https://www.python.org/dev/peps/pep-0008/)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)

## 🤝 Getting Help

- Check existing issues and discussions
- Review the [CONTRIBUTING.md](./CONTRIBUTING.md)
- Ask questions in issue comments
- Reach out to maintainers

## 📝 Code Review Checklist

Before requesting review:

- [ ] Code runs without errors
- [ ] Follows PEP 8 style guide
- [ ] Comments added for complex logic
- [ ] Log messages are clear
- [ ] No hardcoded values (use config/env vars)
- [ ] Dependencies are listed in requirements.txt
- [ ] Commit messages are descriptive

## 🔄 Continuous Improvement

Suggestions for enhancing the bot:

1. **Add configuration file** - `config.yaml`
2. **Implement task scheduling** - `schedule` library
3. **Add error handling** - Try/except blocks
4. **Create unit tests** - `unittest` framework
5. **Add logging levels** - `logging` module
6. **Implement CLI arguments** - `argparse` module

---

Happy coding! Questions? Open an issue on GitHub. 🚀
