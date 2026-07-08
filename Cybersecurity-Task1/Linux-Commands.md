# Linux Commands

Commands demonstrated during Task 1, run from the Kali Linux terminal.

---

## Print Working Directory

```bash
pwd
```
Displays the current working directory's absolute path.

---

## List Files

```bash
ls
```
Lists files and directories in the current location.

---

## Change Directory

```bash
cd Task1
```
Moves into the `Task1` directory.

---

## Create a Directory

```bash
mkdir Task1
```
Creates a new folder named `Task1`.

---

## Create an Empty File

```bash
touch demo.txt
```
Creates a new, empty file called `demo.txt`.

---

## Write Text to a File

```bash
echo "Hello ApexPlanet" > demo.txt
```
Writes the string `Hello ApexPlanet` into `demo.txt`, overwriting existing content.

---

## Display File Contents

```bash
cat demo.txt
```
Prints the contents of `demo.txt` to the terminal.

---

## Copy a File

```bash
cp demo.txt demo2.txt
```
Creates a copy of `demo.txt` named `demo2.txt`.

---

## Rename / Move a File

```bash
mv demo2.txt notes.txt
```
Renames `demo2.txt` to `notes.txt`.

---

## Change File Permissions

```bash
chmod 755 demo.txt
```
Sets read/write/execute for the owner, and read/execute for group and others.

---

## Current User

```bash
whoami
```
Displays the currently logged-in username.

---

## Hostname

```bash
hostname
```
Displays the machine's hostname.

---

## Network Interfaces

```bash
ip addr
```
Displays all network interfaces and their assigned IP addresses.

---

## Netcat Verification

```bash
nc -h
```
Displays the Netcat help menu, confirming the tool is installed and available for use.
