---
layout: post
title: "Auto update uv pyproject.toml dependencies"
date: 2024-12-05 10:00:00 +0000
categories: [python, uv-package-manager, scripts]
tags: [python, uv, pyproject, automation, tomli]
---

Unlike pip-tools, `uv` package manager currently doesn't support automatically updating `pyproject.toml` based on the lock file. This script helps automate that process by automatically running `uv lock -U` and then updating your `pyproject.toml` with the latest versions.

### Features of the Script
- **Fully automated**: Runs `uv lock -U` automatically before updating `pyproject.toml`
- Updates both main dependencies and dependency groups
- Preserves dependency extras (e.g., `fastapi[standard]`)
- Removes duplicate version constraints
- Clear progress indicators with success/failure feedback
- Shows exactly which dependencies were updated
- Proper error handling for missing `uv` command

### Prerequisites
- Python 3.11+ (for built-in `tomllib`)
- `tomli-w` package (`pip install tomli-w`)
- `uv` installed and available in PATH

### Usage Instructions
Simply run the script:
```bash
python upgrade_pyproject.py
```

The script will automatically:
1. Run `uv lock -U` to update all dependencies to their latest versions
2. Parse the updated lock file
3. Update your `pyproject.toml` to match the lock file versions
4. Display all changes made

### What's New
The updated script now handles the entire workflow in one command. No need to manually run `uv lock -U` first - the script does it all for you! It also provides better visual feedback with progress indicators and shows the output from the lock update process.

### Script
You can find the full script below:
<script src="https://gist.github.com/yamanahlawat/270a120dd1981010a9336b871f80a39b.js"></script>
