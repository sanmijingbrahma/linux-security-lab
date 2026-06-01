# Linux Module 4

## `cp -r`

Copies directories and their contents recursively.

**Syntax:**

```bash
cp -r source_directory destination_directory
```

**Example:**

```bash
cp -r Documents Backup
```

Copies the `Documents` directory and all its files/subdirectories into `Backup`.

---

## `df`

Displays disk space usage of file systems.

**Syntax:**

```bash
df
```

**Useful option:**

```bash
df -h
```

`-h` shows sizes in human-readable format (KB, MB, GB).

**Example Output:**

```bash
Filesystem      Size  Used Avail Use%
/dev/sda1       100G   45G   55G  45%
```

---

## `rm -r`

Removes directories and their contents recursively.

**Syntax:**

```bash
rm -r directory_name
```

**Example:**

```bash
rm -r temp
```

Deletes the `temp` directory and everything inside it.

**Force deletion:**

```bash
rm -rf temp
```

`-f` suppresses confirmation prompts.

⚠️ Use carefully; deleted files are not easily recoverable.

---

## `ps aux`

Displays detailed information about all running processes.

**Syntax:**

```bash
ps aux
```

**Columns:**

* **USER** – Process owner
* **PID** – Process ID
* **%CPU** – CPU usage
* **%MEM** – Memory usage
* **COMMAND** – Command that started the process

**Example:**

```bash
ps aux | grep firefox
```

Shows Firefox-related processes.

---

## `|` (Pipe)

Passes the output of one command as input to another command.

**Syntax:**

```bash
command1 | command2
```

**Example:**

```bash
ls | wc -l
```

Counts the number of files and directories in the current folder.

**Another Example:**

```bash
ps aux | grep chrome
```

Finds Chrome processes.

---

## `grep`

Searches for text patterns in files or command output.

**Syntax:**

```bash
grep pattern file
```

**Examples:**

```bash
grep "error" log.txt
```

Finds lines containing "error".

```bash
grep -i "linux" notes.txt
```

Searches case-insensitively.

```bash
ps aux | grep ssh
```


---

## `kill`

Terminates a running process using its Process ID (PID).

**Syntax:**

```bash
kill PID
```

**Example:**

```bash
kill 1234
```

Sends a termination signal to process `1234`.

To find the PID:

```bash
ps aux | grep firefox
```

---

## `kill -9`

Forcefully terminates a process using the **SIGKILL** signal.

**Syntax:**

```bash
kill -9 PID
```

**Example:**

```bash
kill -9 1234
```

**When to use:**

* When a process is frozen or unresponsive.
* When a normal `kill` command does not work.

⚠️ `kill -9` immediately stops the process without allowing it to save data or clean up resources.

