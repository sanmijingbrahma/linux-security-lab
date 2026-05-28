# # Linux Survival — Module 2

## 1. Pathname

A **pathname** tells Linux where a file or directory is located.

### Types of Pathnames

### Absolute Path

Starts from the root directory `/`

Example:

```bash
/home/user/Documents/file.txt
```

### Relative Path

Starts from the current directory.

Example:

```bash
Documents/file.txt
```

### Important Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| `/`    | Root directory    |
| `.`    | Current directory |
| `..`   | Parent directory  |
| `~`    | Home directory    |

### Useful Commands

```bash
pwd        # Show current directory
cd         # Change directory
ls         # List files
```

Examples:

```bash
cd /home/user/Desktop
cd ..
cd ~
```

---

# 2. Copy Files

Use the `cp` command.

## Syntax

```bash
cp source destination
```

## Examples

### Copy a file

```bash
cp file1.txt backup.txt
```

### Copy to another directory

```bash
cp file1.txt /home/user/Documents/
```

### Copy directories

```bash
cp -r Folder1 Folder2
```

`-r` means recursive.

### Preserve original timestamps and permissions

```bash
cp -p file1.txt backup.txt
```

---

# 3. Remove Files

Use the `rm` command.

## Syntax

```bash
rm filename
```

## Examples

### Remove a file

```bash
rm file1.txt
```

### Remove multiple files

```bash
rm file1.txt file2.txt
```

### Remove with confirmation

```bash
rm -i file1.txt
```

### Force remove

```bash
rm -f file1.txt
```

⚠ Be careful with:

```bash
rm -rf *
```

It can delete everything recursively.

---

# 4. Remove Directories

## Remove empty directory

```bash
rmdir dirname
```


# 5. File Security

Linux security is mainly controlled through:

* Ownership
* Permissions

Every file has:

| Type       | Meaning       |
| ---------- | ------------- |
| User (u)   | Owner         |
| Group (g)  | Group users   |
| Others (o) | Everyone else |

---

# 6. Change File Permissions

Use the `chmod` command.

## Permission Types

| Permission | Symbol | Value |
| ---------- | ------ | ----- |
| Read       | r      | 4     |
| Write      | w      | 2     |
| Execute    | x      | 1     |

---

## View Permissions

```bash
ls -l
```

Example:

```bash
-rwxr-xr--
```

Breakdown:

| Part | Meaning            |
| ---- | ------------------ |
| rwx  | Owner permissions  |
| r-x  | Group permissions  |
| r--  | Others permissions |

---

## Change Permissions (Symbolic Method)

### Add execute permission

```bash
chmod +x script.sh
```

### Remove write permission

```bash
chmod -w file.txt
```

### Give owner full permission

```bash
chmod u=rwx file.txt
```

---

## Change Permissions (Numeric Method)

### Example

```bash
chmod 755 script.sh
```

Explanation:

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 5      | r-x        |
| 5      | r-x        |

Another example:

```bash
chmod 644 notes.txt
```

Meaning:

* Owner → read/write
* Group → read
* Others → read

---

# 7. Wildcards (`*` and `?`)

Wildcards help match filenames.

---

## `*` (Asterisk)

Matches **zero or more characters**.

### Examples

```bash
ls *.txt
```

Shows all `.txt` files.

```bash
rm *.log
```

Deletes all `.log` files.

```bash
cp image* backup/
```

Copies files starting with `image`.

---

## `?` (Question Mark)

Matches exactly **one character**.

### Examples

```bash
ls file?.txt
```

Matches:

```text
file1.txt
fileA.txt
```

But NOT:

```text
file10.txt
```

---

# 8. Group Membership

Linux allows users to belong to groups for shared access.

---

## Check Current User Groups

```bash
groups
```

```bash
id
```

