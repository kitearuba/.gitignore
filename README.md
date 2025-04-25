# 🚫 .gitignore for C Devs (Vim + CLion + VS + 42 Style)

![Git](https://img.shields.io/badge/Git-clean-blue?style=flat-square)
![C Projects](https://img.shields.io/badge/Language-C-green?style=flat-square)
![Editor Agnostic](https://img.shields.io/badge/Editors-Vim%20%7C%20CLion%20%7C%20VSCode-yellow?style=flat-square)
![No Junk](https://img.shields.io/badge/Junk-Free-critical?style=flat-square)

A robust `.gitignore` tailored for C development, including support for:
- 🧠 42 School projects  
- 🛠️ JetBrains IDEs (`.idea/`)  
- 🌀 Vim swap files  
- 🧱 Visual Studio clutter  
- 💾 OS & system trash  
- 🎨 And even `minilibx` smart exceptions!

---

## 📥 How to Use

You can either:

1. **Copy the contents** of the `gitignore` file from this repo
   and paste them into your project's `.gitignore`.

2. Or download the file (named `gitignore`), then **rename it** in your project root:

   mv gitignore .gitignore

---

## 💡 Why This Exists

When collaborating on C projects or pushing to GitHub, your repo can easily get polluted by:
- Editor settings
- Swap files
- Compiled binaries
- IDE-generated junk
- Local-only dependencies

This `.gitignore` keeps your repository **lean**, **clean**, and **collaborator-friendly**. It follows good practice for team dev and includes smart logic to **ignore `minilibx-linux/` but allow key source files**.

---

## 🔥 What's Covered

### 🗂️ General Dev Files
```bash
*.o       # Object files
*.a       # Static libs
*.so      # Shared libs
*.exe     # Executables
*.out     # Executables
*.elf     # Embedded binaries
*.dSYM/   # macOS debug files
```

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

# VS Code (optional, safe to include)
.vscode/
```

### 🧼 OS and Backup Files
```bash
.DS_Store   # macOS
*~          # Backups
*.bak       # Manual backups
*.log       # Debug logs
```

### 🧪 Kernel Module Clutter
```bash
*.mod*
*.cmd
.tmp_versions/
Module.symvers
```

### 📦 `minilibx-linux` Smart Ignore
```bash
minilibx-linux/*
!minilibx-linux/*.c
!minilibx-linux/*.h
!minilibx-linux/Makefile
```
> This keeps the source clean and shareable while ignoring local builds, `.o` files, or system-specific junk.

---

## 🛠️ Usage

Copy this `.gitignore` into the root of your C project:

```bash
curl -O https://raw.githubusercontent.com/kitearuba/c-clean-gitignore/main/.gitignore
```

Or clone the whole repo and pick what you need.

---

## 🙌 Inspired By

- [GitHub's official gitignore templates](https://github.com/github/gitignore)
- 42 Network norms & tools
- Developer pain during late-night debugging sessions

---

## 👨‍💻 Maintainer

- **Christian (chrrodri)**  
  GitHub: [@kitearuba](https://github.com/kitearuba)  
  Personal Site: [is.crod.io](https://is.crod.io)

---

## 🧙 Bonus Tip

To apply your new `.gitignore` to already-tracked junk:
```bash
git rm -r --cached .idea minilibx-linux
git add .
git commit -m "Cleaned repo with updated .gitignore ✨"
```

---

## 🛡️ Keep It Clean. Push With Pride.  
```
~ No `.swp` left behind. No `.idea` folder in sight. ~
```
