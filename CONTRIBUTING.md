# Contributing to My First Bot

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the project.

## 📖 Code of Conduct

- Be respectful and constructive
- Focus on the code, not the person
- Help others learn and grow
- Report issues professionally

## 🐛 Reporting Issues

If you find a bug:

1. **Check existing issues** to avoid duplicates
2. **Provide a clear description** of the problem
3. **Include steps to reproduce:**
   - What you were doing
   - What happened
   - What you expected to happen
4. **Attach relevant information:**
   - Python version: `python --version`
   - Operating system
   - Any error messages or logs

## ✨ Suggesting Features

We'd love to hear your ideas! When suggesting a feature:

1. **Use a clear, descriptive title**
2. **Provide detailed description** of the feature
3. **Explain the use case** and why it would be useful
4. **Include examples** if possible

## 🛠️ Development Setup

### 1. Fork and Clone

```bash
git clone https://github.com/YOUR-USERNAME/my-first-bot.git
cd my-first-bot
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 📝 Making Changes

### 1. Create a Feature Branch

```bash
git checkout -b feature/your-feature-name
```

Branch naming convention:
- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring

### 2. Make Your Changes

- Keep commits focused and atomic
- Write clear commit messages
- Follow the existing code style
- Add comments for complex logic

### 3. Test Your Changes

```bash
python bot.py
cat log.txt  # Verify logs are written
```

### 4. Commit Your Work

```bash
git add .
git commit -m "Brief description of changes"
```

Commit message guidelines:
- Use present tense: "Add feature" not "Added feature"
- Be specific: "Fix logging bug" not "Fix bug"
- Reference issues: "Fixes #123"

## 📤 Submitting a Pull Request

1. **Push your branch:**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Open a Pull Request on GitHub:**
   - Fill out the PR template completely
   - Provide a clear description of changes
   - Reference any related issues
   - Include screenshots if relevant

3. **Respond to feedback:**
   - Be open to suggestions
   - Update your PR based on reviews
   - Re-request review when ready

## ✅ Pull Request Checklist

Before submitting your PR, ensure:

- [ ] Code follows the existing style
- [ ] Changes are tested locally
- [ ] Commit messages are clear and descriptive
- [ ] No unnecessary files are included
- [ ] Documentation is updated if needed
- [ ] No breaking changes (explain if unavoidable)

## 📚 Code Style

- **Python:** Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/)
- **Naming:** Use descriptive names for variables and functions
- **Comments:** Add comments for non-obvious logic
- **Line length:** Keep lines under 88 characters when possible

### Example:

```python
# Good
def log_task_completion(task_name):
    """Log that a task has completed successfully."""
    with open("log.txt", "a") as f:
        f.write(f"{task_name} ran successfully!\n")

# Avoid
def log_completion(t):
    f = open("log.txt", "a")
    f.write(t + " done\n")
    f.close()
```

## 🔄 Review Process

1. **Automated checks** run on your PR
2. **Maintainers review** your changes
3. **Feedback is provided** (may need updates)
4. **Once approved**, your PR is merged

## 📖 Documentation

When adding features, please update:

- **README.md** - For user-facing features
- **Code comments** - For complex logic
- **This file** - If adding new contribution guidelines

## 🚀 Getting Help

- **Questions?** Open an issue with the `question` label
- **Stuck?** Comment on the issue and ask for help
- **Want to discuss?** Join our discussions section

## 📋 Area-Specific Guidelines

### Adding New Features

- Create an issue first to discuss the feature
- Keep changes focused and modular
- Add appropriate logging
- Update documentation

### Bug Fixes

- Create an issue describing the bug
- Include test case if possible
- Verify fix doesn't break existing functionality

### Documentation

- Use clear, simple language
- Include examples
- Keep it up-to-date with code changes

## 🎉 Thank You!

Your contributions make this project better. We appreciate your time and effort!

---

Have questions? Feel free to reach out or open an issue. Happy coding! 🚀
