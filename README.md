# My First Bot

[![Workflow Status](https://github.com/gasukwo52-commits/my-first-bot/actions/workflows/azure-webapps-node.yml/badge.svg)](https://github.com/gasukwo52-commits/my-first-bot/actions/workflows/azure-webapps-node.yml)

A simple automation bot project exploring creativity through task automation. This is a learning project designed to demonstrate basic bot development and automation concepts.

## 📋 Table of Contents

- [Features](#features)
- [What it does](#what-it-does)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Logging](#logging)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- 🤖 Automated task execution
- 📝 Task logging to file (`log.txt`)
- 🚀 Easy to extend with new tasks
- 📊 Simple status reporting
- 🔄 Automatic error handling

## 🎯 What it does

The bot performs the following automated tasks:

```python
print("Bot started!")

print("Doing automatic task...")

# Example task
with open("log.txt", "a") as f:
    f.write("Bot ran successfully!\n")

print("Done!")
```

**Current Functionality:**
- Logs startup status to console
- Executes predefined automation tasks
- Records task completion in `log.txt`
- Prints completion status

## 📦 Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

## 🔧 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gasukwo52-commits/my-first-bot.git
   cd my-first-bot
   ```

2. **(Optional) Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies (if any):**
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

### Basic Usage

Run the bot:
```bash
python bot.py
```

### Expected Output

```
Bot started!
Doing automatic task...
Done!
```

### Checking Logs

View the task execution logs:
```bash
cat log.txt
```

Or on Windows:
```cmd
type log.txt
```

## 📁 Project Structure

```
my-first-bot/
├── README.md                 # This file - project documentation
├── bot.py                    # Main bot script
├── log.txt                   # Task execution logs (generated at runtime)
├── requirements.txt          # Python dependencies
├── LICENSE                   # Project license
├── .gitignore               # Git ignore patterns
├── .github/
│   └── workflows/           # GitHub Actions workflows
│       └── azure-webapps-node.yml
└── .devcontainer/           # Development container configuration
```

## ⚙️ Configuration

Currently, the bot runs with hardcoded tasks. To add custom tasks:

1. Open `bot.py`
2. Add your task logic after the "Doing automatic task..." section
3. Update `log.txt` with any custom logging as needed

**Example: Adding a new task**
```python
# Add new task
print("Running new task...")
with open("log.txt", "a") as f:
    f.write("New task completed!\n")
```

## 📊 Logging

The bot writes all task completion events to `log.txt`. Each execution appends a new line:

```
Bot ran successfully!
Bot ran successfully!
Bot ran successfully!
```

**Log File Location:** `./log.txt`

### Clearing Logs

To clear existing logs (on Unix/Mac):
```bash
rm log.txt
```

On Windows:
```cmd
del log.txt
```

## 🐛 Troubleshooting

### Bot doesn't start
- Ensure Python 3.7+ is installed: `python --version`
- Check that `bot.py` exists in the current directory
- Verify file permissions: `chmod +x bot.py` (Unix/Mac)

### Permission denied on `log.txt`
- Check file permissions: `ls -l log.txt` (Unix/Mac)
- Ensure write access to the directory
- Delete and re-run the bot to recreate the file

### No logs being written
- Verify the directory is writable: `touch test.txt`
- Check disk space availability
- Ensure `log.txt` isn't open in another program

## 🤝 Contributing

We welcome contributions! To help improve this bot:

1. **Fork the repository**
2. **Create a feature branch:** `git checkout -b feature/your-feature`
3. **Make your changes** and test thoroughly
4. **Commit with clear messages:** `git commit -m "Add descriptive message"`
5. **Push to your fork:** `git push origin feature/your-feature`
6. **Open a Pull Request** with a clear description

See [CONTRIBUTING.md](./CONTRIBUTING.md) for more details.

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

**Questions or Issues?** Please open an [issue](https://github.com/gasukwo52-commits/my-first-bot/issues) on GitHub.
