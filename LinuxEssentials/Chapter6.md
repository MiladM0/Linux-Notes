# 🐧 Linux Shell Basics

## 📖 Basic Commands, Globbing, Quoting & Variables

---

# ⚡ Understanding Linux Commands

A Linux command is typically made up of three parts:

```text
command [options] [arguments]
```

| Part     | Purpose          | Example    |
| -------- | ---------------- | ---------- |
| Command  | What to do       | `ls`       |
| Option   | How to do it     | `-a`       |
| Argument | What to do it on | `Desktop/` |

### Example

```bash
ls -a Desktop/
```

Meaning:

* `ls` → list files
* `-a` → include hidden files
* `Desktop/` → target directory

---

# 🌐 Remote Command Tools

Linux provides tools for accessing remote systems.

## Telnet

```bash
telnet
```

### Characteristics

❌ Not encrypted

❌ Not secure for modern use

Historically used for remote administration.

---

## SSH (Secure Shell)

```bash
ssh
```

### Characteristics

✅ Encrypted

✅ Secure

✅ Industry standard for remote administration

Example:

```bash
ssh username@server-ip
```

---

# 🔤 Case Sensitivity

> [!IMPORTANT]
> Linux is a **case-sensitive** operating system.

Examples:

```text
file.txt
File.txt
FILE.txt
```

These are considered **three different files**.

---

# 📦 Variables

A variable is a named container used to store data.

### Example

```bash
name="Milad"
```

Using the variable:

```bash
echo $name
```

Output:

```text
Milad
```

> [!TIP]
> In Bash, variables are usually referenced using `$variable_name`.

---

# ❌ What Is a Syntax Error?

A syntax error occurs when a command or script does not follow the correct language rules.

### Example

Correct:

```bash
echo "Hello"
```

Incorrect:

```bash
echo "Hello
```

The missing quotation mark causes a syntax error.

---

# 🤖 What Is a Shell Script?

A shell script is a file containing Linux commands that are executed automatically.

### Purpose

* Automate repetitive tasks
* Save time
* Reduce manual work

### Example

```bash
#!/bin/bash

echo "Hello World"
date
```

Typical extension:

```text
.sh
```

---

# 📝 Quoting

Quoting removes or changes the special meaning of certain characters.

### Common Special Characters

```text
$ * ; > ? & | "
```

These are often called:

```text
Metacharacters
```

---

## Double Quotes

```bash
echo "$HOME"
```

Variables are expanded.

Output:

```text
/home/user
```

---

## Single Quotes

```bash
echo '$HOME'
```

Variables are **not** expanded.

Output:

```text
$HOME
```

---

# 🔍 Globbing

Globbing is a pattern-matching technique used by the shell to find files.

---

## Asterisk (*)

Matches zero or more characters.

Example:

```bash
ls *.txt
```

Matches:

```text
notes.txt
report.txt
todo.txt
```

---

## Question Mark (?)

Matches exactly one character.

Example:

```bash
ls file?.txt
```

Matches:

```text
file1.txt
fileA.txt
```

But not:

```text
file10.txt
```

---

## Globbing vs Regular Expressions

> [!NOTE]
> Globbing and Regular Expressions (RegEx) are related concepts but are **not the same thing**.

Examples:

| Feature | Globbing                 | RegEx                     |
| ------- | ------------------------ | ------------------------- |
| `*`     | Any number of characters | Previous pattern repeated |
| `?`     | One character            | Optional previous pattern |
| Usage   | File matching            | Text matching             |

---

# 📁 Working with Directories

## Create a Directory

```bash
mkdir myfolder
```

Creates:

```text
myfolder/
```

---

## Show Current Directory

```bash
pwd
```

Output example:

```text
/home/user/Documents
```

`pwd` stands for:

```text
Print Working Directory
```

---

# 📂 Listing Files

## Show Files

```bash
ls
```

---

## Show Hidden Files

```bash
ls -a
```

Displays all files, including hidden files.

Examples:

```text
.bashrc
.gitconfig
.profile
```

---

## Detailed Listing

```bash
ls -l
```

Displays:

* Permissions
* Owner
* Group
* Size
* Modification date

Example:

```text
-rw-r--r-- 1 user user 120 Jul 20 file.txt
```

---

# 🗑️ Removing Files and Directories

## Remove a File

```bash
rm file.txt
```

---

## Remove an Empty Directory

```bash
rmdir myfolder
```

---

## Remove a Non-Empty Directory

```bash
rm -r myfolder
```

> [!WARNING]
> Be careful with `rm -r` because it deletes files recursively.

---

# 💡 Useful Linux Tip

> [!TIP]
> Everything in Linux is treated as a file (or file-like object).

Examples include:

* Regular files
* Directories
* Devices
* Pipes
* Sockets

Also:

> File extensions are usually not required for Linux to identify executable programs.

---

# 🔄 Multiple Commands on One Line

Commands can be separated using a semicolon (`;`).

Example:

```bash
pwd; ls; date
```

This executes:

1. `pwd`
2. `ls`
3. `date`

one after another.

---

# 🌎 Environment Variables

## Display Environment Variables

```bash
printenv
```

Displays environment variables such as:

```text
PATH
HOME
USER
SHELL
```

---

# 📚 Getting Help in Linux

Linux provides several built-in documentation tools.

---

## whatis

```bash
whatis ls
```

Displays a short description.

Example:

```text
ls - list directory contents
```

---

## whereis

```bash
whereis ls
```

Locates:

* Binary files
* Source files
* Manual pages

---

## apropos

```bash
apropos network
```

Searches command descriptions for matching keywords.

Equivalent to:

```bash
man -k network
```

---

## man

```bash
man ls
```

Displays the full manual page.

### Navigation

| Key   | Action        |
| ----- | ------------- |
| Space | Next page     |
| b     | Previous page |
| /     | Search        |
| q     | Quit          |

> [!NOTE]
> Most Linux systems use the **less** pager to display manual pages.

---

## info

```bash
info ls
```

Similar to `man`, but often:

* More detailed
* Organized as a hyperlinked document
* Easier for large manuals

---

# 📌 Key Takeaways

* Linux commands follow the pattern: `command + options + arguments`.
* SSH is the secure replacement for Telnet.
* Linux is case-sensitive.
* Variables store reusable data.
* Shell scripts automate repetitive tasks.
* Quoting controls how special characters are interpreted.
* Globbing is used for filename pattern matching.
* `mkdir`, `pwd`, `ls`, and `rm` are essential filesystem commands.
* `man`, `info`, `whatis`, and `apropos` help you learn Linux commands.
