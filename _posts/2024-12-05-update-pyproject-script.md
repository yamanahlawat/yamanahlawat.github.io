---
layout: post
title: "Auto update uv pyproject.toml dependencies"
date: 2024-12-05 10:00:00 +0000
categories: [python, uv-package-manager, scripts]
tags: [python, uv, pyproject, automation, tomli]
---

Unlike pip-tools, `uv` package manager currently doesn't support automatically updating `pyproject.toml` based on the lock file. This script helps automate that process by reading the versions from `uv.lock` and updating your `pyproject.toml` accordingly.

### Features of the Script
- Automatically updates both main dependencies and dependency groups
- Removes duplicate version constraints
- Preserves dependency extras (e.g., `fastapi[standard]`)
- Creates a backup of `pyproject.toml` before making changes

### Prerequisites
- Python 3.11+
- `tomli-w` package (`pip install tomli-w`)
- An updated `uv.lock` file (`uv lock --update` or `uv lock -U`)

### Usage Instructions
1. Update your lock file: `uv lock -U`
2. Run the script: `python upgrade_pyproject.py`

### Script
You can find the full script below:
<script src="https://gist.github.com/yamanahlawat/270a120dd1981010a9336b871f80a39b.js"></script>
