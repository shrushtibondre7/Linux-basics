# Chapter 6 - Vim and Nano Editors

# Introduction

A text editor is a software application used to create and edit text files. In Linux, text editors are essential for modifying configuration files, writing shell scripts, editing code, and managing system settings.

The two most commonly used command-line text editors are:

- Vim
- Nano

Every Linux Administrator and DevOps Engineer should know how to use both.

---

# What is Vim?

Vim (Vi Improved) is a powerful and advanced command-line text editor. It is fast, lightweight, and available on almost every Linux distribution.

### Features of Vim

- Lightweight
- Fast
- Keyboard-based navigation
- Syntax highlighting
- Search and replace
- Undo and Redo
- Plugin support
- Suitable for programming and system administration

---

# Opening a File in Vim

Open an existing file:

```bash
vim file.txt
```

Create a new file:

```bash
vim notes.txt
```

---

# Vim Modes

Vim works in different modes.

## 1. Normal Mode

Default mode used for navigation and commands.

Examples:

- Move cursor
- Copy text
- Delete text
- Save file
- Exit editor

---

## 2. Insert Mode

Used for typing or editing text.

Press:

```text
i
```

Now you can type normally.

To return to Normal Mode:

Press

```text
Esc
```

---

## 3. Command Mode

Used to save, quit, search, and perform advanced operations.

Enter Command Mode by pressing:

```text
:
```

---

# Important Vim Commands

## Save File

```text
:w
```

---

## Save and Exit

```text
:wq
```

or

```text
:x
```

---

## Exit Without Saving

```text
:q!
```

---

## Quit

```text
:q
```

---

# Navigation Commands

Move Left

```text
h
```

Move Down

```text
j
```

Move Up

```text
k
```

Move Right

```text
l
```

Beginning of Line

```text
0
```

End of Line

```text
$
```

Go to First Line

```text
gg
```

Go to Last Line

```text
G
```

---

# Editing Commands

Delete Character

```text
x
```

Delete Entire Line

```text
dd
```

Delete Five Lines

```text
5dd
```

Copy Line

```text
yy
```

Copy Five Lines

```text
5yy
```

Paste

```text
p
```

Undo

```text
u
```

Redo

```text
Ctrl + r
```

---

# Search in Vim

Search Word

```text
/searchword
```

Next Match

```text
n
```

Previous Match

```text
N
```

---

# Replace Text

Replace first occurrence

```text
:s/old/new/
```

Replace all occurrences

```text
:%s/old/new/g
```

---

# What is Nano?

Nano is a simple and beginner-friendly command-line text editor.

Unlike Vim, Nano displays keyboard shortcuts at the bottom of the screen, making it easier to learn.

---

# Opening Nano

Create or open a file

```bash
nano notes.txt
```

---

# Common Nano Shortcuts

Save File

```text
Ctrl + O
```

Exit Nano

```text
Ctrl + X
```

Cut Line

```text
Ctrl + K
```

Paste

```text
Ctrl + U
```

Search

```text
Ctrl + W
```

Go to Line Number

```text
Ctrl + _
```

---

# Vim vs Nano

| Feature | Vim | Nano |
|---------|------|------|
| Difficulty | Moderate | Easy |
| Learning Curve | High | Low |
| Performance | Fast | Fast |
| Keyboard Shortcuts | Many | Simple |
| Best For | Developers & Admins | Beginners |
| Default in Servers | Yes | Sometimes |

---

# Which Editor Should You Learn?

Nano is recommended for beginners because it is simple.

Vim is recommended for Linux Administrators, Cloud Engineers, and DevOps Engineers because it is available on almost every Linux server and offers advanced editing features.

---

# Best Practices

- Learn basic Vim commands.
- Save your work frequently.
- Practice navigation without using the mouse.
- Use Nano when quick edits are required.
- Use Vim for configuration files and scripting.

---

# Summary

In this chapter, we learned:

- What is Vim
- What is Nano
- Vim Modes
- Navigation Commands
- Editing Commands
- Search and Replace
- Saving and Exiting
- Vim vs Nano

---

# Interview Questions

## 1. What is Vim?

Vim is an advanced command-line text editor used to create and edit files in Linux.

---

## 2. What is Nano?

Nano is a simple command-line text editor designed for beginners.

---

## 3. How do you enter Insert Mode in Vim?

Press:

```text
i
```

---

## 4. How do you save and exit in Vim?

```text
:wq
```

or

```text
:x
```

---

## 5. How do you quit without saving?

```text
:q!
```

---

## 6. Which editor is easier for beginners?

Nano.

---

## 7. Which editor is preferred by Linux Administrators?

Vim.

---

# Hands-on Practice

```bash
vim practice.txt

nano practice.txt

cat practice.txt
```

Practice:

- Create a file using Vim.
- Write your name.
- Save the file.
- Exit Vim.
- Open the same file using Nano.
- Add one more line.
- Save and exit.
- Display the file using `cat`.

---

# Conclusion

Vim and Nano are essential Linux text editors. Nano is ideal for beginners, while Vim is a powerful editor preferred by system administrators and DevOps engineers for managing configuration files, scripts, and source code.
