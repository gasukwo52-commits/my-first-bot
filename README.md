# My First Bot

[![Workflow Status](https://github.com/gasukwo52-commits/my-first-bot/actions/workflows/azure-webapps-node.yml/badge.svg)](https://github.com/gasukwo52-commits/my-first-bot/actions/workflows/azure-webapps-node.yml)

This is my first automation bot. A simple project exploring creativity through automation.

## What it does

The bot performs the following tasks:

```python
print("Bot started!")

print("Doing automatic task...")

# Example task
with open("log.txt", "a") as f:
    f.write("Bot ran successfully!\n")

print("Done!")
```

## Features

- Starts up and logs its status
- Performs automatic tasks
- Logs task completion to `log.txt`

## Getting Started

Run the bot with:

```bash
python bot.py
```

Check `log.txt` for task execution logs.
