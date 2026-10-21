# Assignment 3 – Terminal Navigation Practice Sheet

As a Windows user working with PowerShell and Git Bash, understanding both standard Unix commands and PowerShell equivalents is essential for navigating directories and managing project files.

## Command Reference

| # | Task Description | Bash / Git Bash | Windows PowerShell |
|---|------------------|-----------------|--------------------|
| 1 | Print current directory | `pwd` | `pwd` / `Get-Location` |
| 2 | List directory contents | `ls` | `ls` / `dir` / `Get-ChildItem` |
| 3 | List with hidden files & details | `ls -la` | `ls -Force` |
| 4 | Create a new folder | `mkdir project` | `mkdir project` |
| 5 | Navigate into folder | `cd project` | `cd project` |
| 6 | Create a new empty file | `touch index.html` | `ni index.html` / `New-Item index.html` |
| 7 | Create nested directories | `mkdir -p css/images` | `mkdir css/images` |
| 8 | Move one level up | `cd ..` | `cd ..` |
| 9 | Move to user home folder | `cd ~` | `cd ~` |
| 10 | Copy a file | `cp index.html copy.html` | `cp index.html copy.html` |
| 11 | Move / Rename a file | `mv copy.html temp.html` | `mv copy.html temp.html` |
| 12 | Remove a single file | `rm temp.html` | `rm temp.html` |
| 13 | Remove folder recursively | `rm -rf old-dir` | `rm -r old-dir` / `Remove-Item -Recurse old-dir` |
| 14 | Display file content | `cat index.html` | `cat index.html` / `Get-Content index.html` |
| 15 | Clear terminal screen | `clear` | `cls` / `Clear-Host` |
| 16 | Open current folder in VS Code | `code .` | `code .` |

---

## Hands-on Navigation Exercise

**Task:**
From the user home directory:
1. Create a workspace folder named `bca-web` with nested directories `styles` and `assets`.
2. Create `index.html` inside `bca-web` and `style.css` inside `styles`.
3. Navigate into `styles`, check location, and return to `bca-web` in one command.
4. List all files recursively to verify structure.
5. Create a backup of `index.html` as `index-backup.html`, then delete the backup.
6. Launch VS Code in the folder.

### Executed Commands (PowerShell)

```powershell
# Step 1: Create directory hierarchy
cd ~
mkdir -p bca-web/styles, bca-web/assets

# Step 2: Create project files
ni bca-web/index.html
ni bca-web/styles/style.css

# Step 3: Navigate and return
cd bca-web/styles
pwd
cd ..

# Step 4: Recursive directory inspection
ls -Recurse

# Step 5: Copy and delete backup
cp index.html index-backup.html
rm index-backup.html

# Step 6: Open in code editor
code .
```
