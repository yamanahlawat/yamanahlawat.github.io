---
layout: post
title: "Automatically Update all installed shadcn/ui Components"
date: 2025-01-19 12:00:00 +0000
categories: [nextjs, shadcn-ui]
tags: [nextjs, shadcn, automation]
---

A simple script to update all your shadcn/ui components in one go. No more updating components one by one!

### The Script
<script src="https://gist.github.com/yamanahlawat/bdf75bcde4f9bb1f88efbed6f47e3f8b.js"></script>

### Quick Start
1. Save as `update-shadcn-components.sh`
2. Make executable: `chmod +x update-shadcn-components.sh`
3. Run: `./update-shadcn-components.sh`

### What it does
- Updates all shadcn components in `src/components/ui/`
- Shows progress for each update
- Tells you what succeeded and what failed

### Before Running
- Commit your changes
- Be in your project root directory

That's it! Simple and effective way to keep your shadcn components up to date.
