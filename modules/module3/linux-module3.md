# # Linux/Unix Command Notes

## 1. Home Directories (`~`)

* `~` represents the current user's home directory.
* Examples:

  ```bash
  cd ~
  pwd
  ```
* Typical home directory:

  ```text
  /home/username
  ```

---

## 2. `man` (Manual Pages)

* Displays the user manual for commands.
* Syntax:

  ```bash
  man command_name
  ```
* Example:

  ```bash
  man ls
  man cat
  ```
* Navigation:

  * `Space` → Next page
  * `b` → Previous page
  * `q` → Quit

---

## 3. `finger`

* Displays information about users.
* Syntax:

  ```bash
  finger username
  ```
* Example:

  ```bash
  finger john
  ```
* Shows login name, home directory, shell, and login status (if installed).

---

## 4. Finding Files (`find`)

* Searches for files and directories.
* Syntax:

  ```bash
  find [path] [options]
  ```
* Examples:

  ```bash
  find . -name "file.txt"
  find /home -name "*.pdf"
  find . -type d
  ```

---

## 5. `cat`

* Displays, creates, or combines files.
* Syntax:

  ```bash
  cat filename
  ```
* Examples:

  ```bash
  cat notes.txt
  cat file1.txt file2.txt
  ```
* Create a file:

  ```bash
  cat > notes.txt
  ```

---

## 6. Redirection

### Output Redirection (`>`)

* Sends output to a file.

  ```bash
  ls > files.txt
  ```

### Append Output (`>>`)

* Adds output to the end of a file.

  ```bash
  echo "Hello" >> notes.txt
  ```

### Input Redirection (`<`)

* Uses a file as input.

  ```bash
  sort < names.txt
  ```

---
### 7. Printing Files (Using `lpr`)

#### Print a File

```bash
lpr filename
```

Example:

```bash
lpr report.txt
```

#### Print on a Specific Printer

```bash
lpr -P printer_name filename
```

Example:

```bash
lpr -P HP_LaserJet report.txt
```

#### Check Print Job Status

```bash
lpq
```

For a specific printer:

```bash
lpq -P HP_LaserJet
```

#### Cancel Print Jobs

Cancel a specific job:

```bash
lprm job-id
```

Example:

```bash
lprm 15
```

Cancel all your print jobs:

```bash
lprm -
```

Cancel all jobs on a specific printer:

```bash
lprm -P HP_LaserJet -
```

#### List Available Printers

```bash
lpstat -p
```


Then print normally:

```bash
lpr report.txt
```

