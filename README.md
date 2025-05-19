# 🚫 .gitignore for 42 C Projects (Philo, Pipex, Minishell, FDF, etc.)

![Git](https://img.shields.io/badge/Git-clean-blue?style=flat-square)
![42 Projects](https://img.shields.io/badge/42-Core_Projects-blue?style=flat-square)
![Editor Agnostic](https://img.shields.io/badge/Editors-Vim%20%7C%20CLion%20%7C%20VSCode-yellow?style=flat-square)
![No Junk](https://img.shields.io/badge/Junk-Free-critical?style=flat-square)

A robust and battle-tested `.gitignore` tailored specifically for **42 School C projects**.  
It helps you keep your repository clean and professional when working on:

- ✅ Philo  
- ✅ Pipex  
- ✅ Minishell  
- ✅ FDF  
- And other common C-based core projects

It also supports multiple development environments:
- 🧠 42 Norm compliance
- 🛠️ CLion, IntelliJ, VS Code
- 🌀 Vim and terminal-only workflows
- 💾 System junk and backup file cleanup

---

## 📥 How to Use

You can either:

1. **Copy the contents** of this `.gitignore` and paste it into your project's root.

2. Or download it and rename:

```bash
curl -O https://raw.githubusercontent.com/kitearuba/c-clean-gitignore/main/.gitignore
````

---

## 💡 Why This Exists

When working in C projects (especially 42), Git repos can get cluttered with:

* Editor and IDE files
* Backup files
* Compiled binaries
* Temporary files
* Local-only data

This `.gitignore` helps you:

* Keep your commits clean
* Focus on your code
* Collaborate without conflicts
* Pass evaluations with no junk or noise

---

## 🔥 What's Covered

### 🧠 Core Project Binaries (ignored)

```bash
philo
pipex
minishell
fdf
```

These are compiled with your `Makefile`, not committed.

---

### 🗂️ General Dev Files

```bash
*.o       # Object files
*.a       # Static libs
*.so      # Shared libs
*.d       # Dependency files (from -MMD)
*.out     # Executables
*.elf     # Embedded binaries
*.dSYM/   # macOS debug files
```

---

### ✏️ Editor + IDE Trash

```bash
# Vim
*.swp
*.swo
*.swn

# JetBrains (CLion / IntelliJ)
.idea/

# Visual Studio
*.user
*.suo
*.VC.db
*.opensdf
*.sdf

# VS Code
.vscode/
```

---

### 🧼 OS and Backup Files

```bash
.DS_Store   # macOS metadata
*~          # Temp/backup files
*.bak       # Manual backups
*.log       # Debug logs
```

---

### 🧪 Kernel Module Clutter (optional)

```bash
*.mod*
*.cmd
.tmp_versions/
Module.symvers
```

---

### 📦 `minilibx-linux` Smart Ignore

```bash
minilibx-linux/*
!minilibx-linux/*.c
!minilibx-linux/*.h
!minilibx-linux/Makefile
```

> This lets you include source files from `minilibx`, but not system-generated junk.

---

## 🧹 Already Tracking Files You Want to Ignore?

If Git is already tracking files like `.idea/`, `.vscode/`, `*.o`, or other clutter, you’ll need to untrack them manually.

### 👉 Step-by-step Cleanup

1. **Untrack files (but keep them locally):**

```bash
git rm --cached -r .idea .vscode *.o *.log
```

2. **Commit the cleanup:**

```bash
git commit -m "Cleaned up tracked junk files 📦"
```

3. **Push your changes:**

```bash
git push
```

---

### 🧪 Double Check

To verify what's being ignored:

```bash
git status --ignored
```

---

### 💬 Pro Tip

If you want to be extra safe, stash your work first:

```bash
git stash
git rm --cached -r .idea
git commit -m "Untracking .idea"
git push
git stash pop
```

---

## 🧙 Bonus Tip

To force apply your `.gitignore` to already tracked junk:

```bash
git rm -r --cached .idea minilibx-linux
git add .
git commit -m "Applied .gitignore to clean repo ✨"
```

---

## 👨‍💻 Maintainer

**Christian Rodríguez (chrrodri)**
GitHub: [@kitearuba](https://github.com/kitearuba)
Personal Site: [crod.io](https://crod.io)

---

## 🛡️ Keep It Clean. Push With Pride.

```
~ No .swp left behind. No .idea folder in sight. ~
```

---

## 📜 License

Licensed under the [MIT License](LICENSE).
Free to use, improve, and share.
