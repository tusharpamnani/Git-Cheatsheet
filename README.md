# **Git Cheat Sheet for Beginners**

## **What is Git?**
Git is a version control system that helps track changes in your code, collaborate with others, and manage different versions of your project.

---

## **Setup & Configuration**
Before using Git, set up your name and email (used to track contributions).

```bash
git config --global user.name "Your Name"   # Set your name
git config --global user.email "your.email@example.com"  # Set your email
git config --list                          # Check all configurations
```

### Example:
```bash
git config --global user.name "tusharpamnani"
git config --global user.email "tusharpamnani1@example.com"
```

---

## **Creating & Connecting Repositories**
1. **Initialize a new repository**:  
   A repository is like a folder to track your project.

   ```bash
   git init
   ```
   Example:
   ```bash
   git init my-project
   cd my-project
   ```

2. **Clone an existing repository**:  
   Copy a remote repository to your computer.

   ```bash
   git clone <repository-url>
   ```
   Example:
   ```bash
   git clone https://github.com/user/repo.git
   ```

3. **Connect to a remote repository**:  
   Link your local repository to a remote one.

   ```bash
   git remote add origin https://github.com/user/project-name.git
   ```

   Example:
   ```bash
   git remote add origin https://github.com/tusharpamnani/Git-Cheatsheet.git
   ```

---

## **Basic Commands**
These commands are used daily.

### Check the Status:
```bash
git status
```
This shows changes in your project (new, modified, or deleted files).

### Add Changes:
```bash
git add <file>  # Add a specific file
git add .       # Add all files
```

### Commit Changes:
```bash
git commit -m "Your message here"
```
This saves your changes locally with a message.

Example:
```bash
git commit -m "Added login functionality"
```

### Push Changes to Remote:
```bash
git push origin <branch-name>
```

Example:
```bash
git push origin main
```

---

## **Working with Branches**
Branches let you work on different features or fixes separately.

### List Branches:
```bash
git branch        # Local branches
git branch -a     # All branches (local + remote)
```

### Create & Switch Branches:
```bash
git branch <branch-name>   # Create new branch
git checkout <branch-name> # Switch to a branch
git checkout -b <branch-name>  # Create and switch
```

Example:
```bash
git checkout -b feature-login
```

---

## **Undoing Mistakes**
Mistakes happen. Here’s how to fix them.

### Unstage a File:
```bash
git reset <file>
```

### Undo Last Commit (Keep Changes):
```bash
git reset --soft HEAD~1
```

### Undo Last Commit (Discard Changes):
```bash
git reset --hard HEAD~1
```

---

## **Saving Work Temporarily (Stashing)**
Stashing is like saving a draft.

```bash
git stash             # Save your changes
git stash list        # View saved stashes
git stash apply       # Apply a stash
git stash pop         # Apply and delete stash
```

---

## **Viewing History**
```bash
git log               # View commit history
git log --oneline     # Compact view
git diff              # See file changes
git diff --staged     # Compare staged changes
```

---

## **Best Practices for First-Time Users**
1. Always write meaningful commit messages:
   - Good: `git commit -m "Added user authentication"`
   - Bad: `git commit -m "fixed stuff"`

2. Pull changes before pushing:
   ```bash
   git pull origin <branch>
   ```

3. Commit often, but don’t commit unnecessary files:
   - Use `.gitignore` to exclude files like logs or config files.

4. Learn by experimenting:
   - Use a test repository to practice commands.

---

### **Common Errors & Fixes**
1. **Forgot to add changes before committing**:
   ```bash
   git add .
   git commit -m "Your message"
   ```

2. **Pushed to the wrong branch**:
   ```bash
   git checkout <correct-branch>
   git push origin <branch-name>
   ```

---

## **Getting Help**
When in doubt:
```bash
git help <command>    # Example: git help commit
```

This cheat sheet should help you get started with Git. Practice frequently to gain confidence!
