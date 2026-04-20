# Nazar Nazar --- Homework 2

## Module 1: Linux File System and Permissions

Repository structure for submission:

homework/ └── module1/ └── nazar_homework_2.md

------------------------------------------------------------------------

# Task 1. Linux Directory Hierarchy

### 1. Go to the root directory and show its contents

``` bash
cd /
ls -la
```

Example output:

bin boot dev etc home lib media mnt opt proc root run sbin srv sys tmp
usr var

------------------------------------------------------------------------

### 2. Go to `/etc` and display the contents

``` bash
cd /etc
ls
```

Example output:

apt cron.d group hostname hosts passwd shadow ssh

------------------------------------------------------------------------

### 3. Go to `/home` and show the list of users

``` bash
cd /home
ls
```

Example output:

student

------------------------------------------------------------------------

# Task 2. Files, Directories and Links

### 1. Create a new directory in the home directory

``` bash
cd ~
mkdir lab2
```

------------------------------------------------------------------------

### 2. Enter the created directory

``` bash
cd lab2
```

------------------------------------------------------------------------

### 3. Create a file

``` bash
touch file.txt
```

------------------------------------------------------------------------

### 4. Copy the file with a new name

``` bash
cp file.txt file_copy.txt
```

------------------------------------------------------------------------

### 5. Rename the copied file

``` bash
mv file_copy.txt file_renamed.txt
```

------------------------------------------------------------------------

### 6. Create a hard link

``` bash
ln file.txt file_hardlink.txt
```

------------------------------------------------------------------------

### 7. Create a symbolic link

``` bash
ln -s file.txt file_symlink.txt
```

------------------------------------------------------------------------

### 8. Find the file by name

``` bash
find ~ -name "file.txt"
```

Example result:

/home/student/lab2/file.txt

------------------------------------------------------------------------

# Task 3. File Permissions

### 1. View file permissions

``` bash
ls -l file.txt
```

Example output:

-rw-r--r-- 1 student student 0 Apr 20 12:00 file.txt

------------------------------------------------------------------------

### 2. Set read-only permissions

``` bash
chmod 444 file.txt
```

Check again:

``` bash
ls -l file.txt
```

Example:

-r--r--r-- 1 student student 0 Apr 20 12:00 file.txt

------------------------------------------------------------------------

### 3. Give write permission to the owner

``` bash
chmod u+w file.txt
```

Check:

``` bash
ls -l file.txt
```

Example:

-rw-r--r-- 1 student student 0 Apr 20 12:01 file.txt

------------------------------------------------------------------------

### 4. Check the current umask

``` bash
umask
```

Example:

0022

------------------------------------------------------------------------

### 5. Set a new umask value

``` bash
umask 022
```

------------------------------------------------------------------------

# Task 4. Users

### 1. Create a new user

``` bash
sudo useradd -m trainee
```

------------------------------------------------------------------------

### 2. Set a password for the user

``` bash
sudo passwd trainee
```

------------------------------------------------------------------------

### 3. Add the user to the sudo group

``` bash
sudo usermod -aG sudo trainee
```

------------------------------------------------------------------------

### 4. Verify that the user exists

``` bash
cat /etc/passwd | grep trainee
```

Example result:

trainee:x:1001:1001::/home/trainee:/bin/bash

------------------------------------------------------------------------

# Conclusion

In this assignment we practiced:

-   navigating the Linux file system
-   creating files and directories
-   working with hard and symbolic links
-   managing file permissions
-   working with users and groups

These operations are essential for basic Linux system administration.
