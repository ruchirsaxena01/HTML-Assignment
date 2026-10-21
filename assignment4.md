# Assignment 4 – Repository with Meaningful Git Commits

Version control is an indispensable engineering practice. This assignment documents setting up Git identity, initializing our project repository, and establishing a professional commit workflow.

## Git Identity Configuration

```bash
# Set author credentials globally
git config --global user.name "Ruchir Saxena"
git config --global user.email "saxenaruchir282@gmail.com"

# Verify current settings
git config user.name
git config user.email
```

## Repository Setup & Milestone Commits

```bash
# Initialize project repository
git init
git branch -M main

# Commit 1: Initial repository documentation
echo "# HTML & CSS Coursework - BCA (AI)" > readme.md
git add readme.md
git commit -m "docs: add initial course overview and readme"

# Commit 2: Setup and command documentation
git add assignment1.md assignment2.md assignment3.md
git commit -m "docs: complete setup proof, url workflow and terminal sheets (01-03)"

# Commit 3: HTML basics and personal introduction
git add assignment6.html assignment7.html assignment8.html assignment10.html
git commit -m "feat: add first web page, text resume and personal introduction (06-08, 10)"
```

## Commit Message Best Practices

1. **Use Conventional Prefixes:**
   - `feat:` for new HTML files, layouts, or component additions.
   - `style:` for CSS styling, color palette tweaks, and font updates.
   - `docs:` for markdown guides, explanations, and readme updates.
   - `fix:` for debugging HTML issues, fixing syntax, or overflow bugs.
   - `refactor:` for improving semantic markup without changing visual behavior.
2. **Imperative, Present-Tense Subject Line:** Write *"add flexbox navbar"* rather than *"added flexbox navbar"*.
3. **Atomic Commits:** Keep commits scoped to a single logical task or group of assignments.

## Planned Course Commit Milestones

| Commit | Message Format | Assignments Included |
|---|---|---|
| 1 | `docs: add README and repository structure` | Readme, gitignore |
| 2 | `docs: setup proof, network flow, and CLI navigation` | 01 – 05 |
| 3 | `feat: basic HTML structure, resume, and debugging` | 06 – 10 |
| 4 | `feat: portfolio links, accessible images, and college info` | 11 – 15 |
| 5 | `feat: interactive forms, data tables, and multi-page site` | 16 – 20 |
| 6 | `style: CSS fundamentals, selectors, and design tokens` | 21 – 25 |
| 7 | `style: box model, card components, overflow, and z-index` | 26 – 30 |
| 8 | `feat: modern Flexbox navigation, login, and landing sections` | 31 – 35 |
| 9 | `feat: CSS Grid galleries, auto-fit cards, and dashboard layout` | 36 – 40 |
| 10 | `feat: responsive breakpoints, audit fixes, and cafe landing capstone` | 41 – 45 |
