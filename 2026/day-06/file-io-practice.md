# Day 06 - Linux Fundamentals: Read and Write Text Files

## 📌 Objective

Today’s goal is to practice basic file I/O operations using Linux fundamental commands.

- Creating a file: notes.txt
- Writing content using redirection: >
- Appending new lines: >>
- Reading full file content: cat
- Reading partial content: head & tail
- Writing and displaying content simultaneously: tee

---

## 🛠️ Commands

### 1️⃣ Create a file
```bash
touch notes.txt
```
Creates an empty file named `notes.txt`.

---

### 2️⃣ Write contents using `>`
```bash
echo "Starting Day 6 of my DevOps Challenge." > notes.txt
```
Write text into the file.

> ⚠️ `>` overwrites existing content.

---

### 3️⃣ Append contents using `>>`
```bash
echo "Redirection using > and >> operator. Learning file read and write operations." >> notes.txt
```
Append new line(s) to the file without removing exisitng content.

### 4️⃣ Read Full File Using `cat`
```bash
cat notes.txt
```
Display complete file content.

---

### 5️⃣ Read First Few Lines Using `head`
```bash
head -n 2 notes.txt
```
Displays first 2 lines of the file.

---

### 6️⃣ Read Last Few Lines Using `tail`
```bash
tail -n 2 notes.txt
```
Displays first 2 lines of the file.

---

### 7️⃣ Write and Display Using `tee`
```bash
echo "Using tee command to write and display output." | tee -a notes.txt 
```
It writes to the file and displays output on the terminal at the same time.

---

## 📂 Final File Content (notes.txt)
```
Starting Day 6 of my DevOps Challenge.
Redirection using > and >> operator. Learning file read and write operations.
Using tee command to write and display output.

<img src="img/File IO.png" width="800">

```

---

## 🎯 Outcome

- `>` overwrite file contents.
- `>>` append contents.
- `cat`, `head` & `tail` are essential command to read fully and partially part of file. Also useful for log file analysis.
- `tee` is essential command to write and read a file at a time. Also useful for logging and scripting.

---

## 🚀 Why This Matters in DevOps

In real-world of DevOps:

* Logs are text-based.
* Configuration files are text-based.
* Scripts generate output file which is text-based.
* Monitoring tools store logs in files.

So being comfortable with file I/O ops helps in:
* Troubleshooting & debugging prod issues.
* Automating tasks.

---

> This is extremely useful for real-time log monitoring in servers.