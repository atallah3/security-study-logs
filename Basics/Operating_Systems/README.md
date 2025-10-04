# Linux
### **Why Linux?**

- Open Source Technology You can view/edit/remove any part of the system, nothing is hidden!
- Hackers FriendlyMany useful tools could be found by default in major Linux distributions. Also, there are distributions like [Kali Linux](https://www.kali.org/) and [Parrot Security OS](https://parrotsec.org/) that were made for security researchers.
- Easy packages installation package = program = software
- Lots of flavorsRead [List of Linux distributions](https://en.wikipedia.org/wiki/List_of_Linux_distributions).
- Watch [You Only NEED 3 Linux Distributions](https://www.youtube.com/watch?v=t9e3NvTnCOA)

In general, when you attempt to do anything and it asks you to confirm with `Y` for `Yes` or `N` for `No`, the default choice s the capital one. ex: If it tells you `Do you want to continue [Y/n]`. The default choice if you just press Enter will be Yes.

**[ Updating System ]**

Before downloading any package, we need to update our package index:

```bash
sudo apt update
```

- `sudo`: Stands for "superuser do." It allows a permitted user to execute a command as the **superuser** or another user.
- `apt`: The command-line interface for the **package management system**.
- `update`: A specific sub-command of `apt` that updates the package index on your system. This means it fetches the latest information about available packages from the repositories defined in your system.

After updating the package index, you can upgrade -If needed or to be up to date- the installed packages to their latest versions:

```bash
sudo apt upgrade
```

- `upgrade`: A sub-command of `apt` that installs the newest versions of all packages currently installed on the system, based on the information fetched by `apt update`.

---

**[ Getting Help ]**

In case you found a command or forget how the command works you use the command `man`, and it will give you the manual page for this command.

```bash
man apt
```

Also you could try to add the `-h` or the `--help` switch, and you will see a tiny help message.

```bash
apt -h
# Or you could run
apt --help
```

---

**[ Package Handling ]**

**{ Install }**

To install a package you could use `sudo apt install PACKAGE_NAME`

```bash
sudo apt install obsidian
```

**{ Search }**

To search for a package you could use `sudo apt search PACKAGE_NAME_YOU_THINK` and you will get a list of packages to choose between.

```bash
sudo apt search vlc
```

**{ Remove }**

To remove a package from your system `sudo apt remove PACKAGE_NAME`

```bash
sudo apt remove obsidian
```

You could use `autoremove` to remove the package and its dependencies

```bash
sudo apt autoremove obsidian
```

**{ Universal Package Managers }**

If you search for a package but you didn't find, there are some universal package managers that you may use.

Read [Universal Package Managers for Linux: Snap, Flatpak, and AppImage](https://www.tecmint.com/cross-distribution-package-managers-for-linux/).

---

**[ File Handling ]**

When you open a new terminal, you will be in your home directory, located at `/home/YOUR_USERNAME/`. Display files and directories in the current directory:

```bash
ls
```

- `ls -a`: Display hidden files and directories.
- `ls -l`: Show files and directories in a detailed format, including file permissions, sizes, and more.
    - `ls -l -h`: Display sizes in human-readable formats instead of bytes. You can combine these options as `ls -lh`. To also include hidden files and directories, use `ls -ahl`.

Print the current directory path:

```bash
pwd
```

If you find a directory and want to enter it:

```bash
cd dir_name
```

**{ Search }**

To search for a file or directory run `locate` command:

```bash
locate file_name
```

Alternatively you could use `find PATH_TO_SEARCH -name FILENAME` command to search recursively until found your target. To search for `flag.txt` file and starting search from the root `/`:

```bash
find / -name flag.txt
```

**{ Download }**

You can download files via:

- `wget`
- `curl`: could be used with any protocol like `ftp`, not only `http`.

```bash
# Example with wget.
wget https://example.com/file.zip

# Example with curl.
curl -O https://example.com/file.zip

# Download a file and save it with a different name
curl -o new_name.zip https://example.com/file.zip
```

**{ Create }**

You could create files with

- `touch` command like `touch newfile.txt`.touch command is made to update the timestamp of existing files without modifying their content and in case you give it a name of a file that doesn't exist, it will create it as a new file.
- `echo` command like you are trying to write nothing into a file, so this will create a file with this name `echo '' > newfile.txt`.

You need to learn a terminal text editor like Nano, Neovim. I personally suggest Neovim.

Read [9 Best Text Editors for the Linux Command Line](https://itsfoss.com/command-line-text-editors-linux/).

**{ view }**

If you have a large file that might cause your text editor to freeze when you try to open it, or if you just want a quick glimpse at the beginning or end of the file without loading the entire content, you can use the following commands:

```bash
head -n 5 myfile # Displays the first 5 lines
tail -n 5 myfile # Displays the last 5 lines.
```

If you do not specify `-n {number}`, the command will default to displaying 10 lines.

As a real use case, you might need to monitor the logs in the `/var/log/apache2/access.log` file in real-time. You can do this with the following command:

```bash
tail -f /var/log/apache2/access.log
```

This file is typically the first place to check to see who accessed what on your Linux server, especially when investigating potential security breaches or compromises.

**{ File Permissions }**

File permissions in Linux determine who can read, write, or execute a file or directory. Each file or directory has an associated set of permissions for three different categories of users: the owner, the group, and others.

**Permission Types:**

1. **Read (`r`):**
    - For files, this allows a user to view the contents.
    - For directories, this allows a user to list the contents.
2. **Write (`w`):**
    - For files, this allows a user to modify or delete the contents.
    - For directories, this allows a user to create, delete, or rename files within the directory.
3. **Execute (`x`):**
    - For files, this allows a user to run the file as a program.
    - For directories, this allows a user to enter the directory and access its contents.

**Permission Structure:**

Permissions are represented by a string of ten characters. For example:

```bash
-rwxr-xr--
```

- The first character represents the type of file ( for regular file, `d` for directory, `l` for symbolic link, etc.).
- The next nine characters are divided into three sets of three, representing the permissions for the owner, the group, and others, respectively.
    - **rwx** for the owner: Read, write, and execute permissions.
    - **r-x** for the group: Read and execute permissions.
    - **r--** for others: Read-only permission.

**Modifying Permissions:**

Permissions can be modified using the `chmod` command. There are two main ways to set permissions: using symbolic (letter-based) or numeric (octal) notation.

- **Symbolic Notation Example:**

```bash
chmod u+x file.txt
```

- This command adds execute permission for the file owner (`u` stands for "user").
- **Numeric Notation Example:**This sets the permissions to `rwxr-xr-x` (read, write, and execute for the owner; read and execute for the group and others).
    
    ```bash
     chmod 755 file.txt
    ```
    

**Viewing Permissions:**

You can view the permissions of a file or directory using the `ls -l` command:

```bash
ls -l file.txt
```

This command displays a detailed list of files and directories along with their permissions, ownership, and other attributes.

---

**[ Command Control and Redirection Operators ]**

1. **`>` and `>>` Symbols:**
    - The `echo` command typically displays text directly in the terminal, like `echo Hello, World!`. Instead of displaying this output, you can **redirect** it to a file.
        - **Option 1:** Use `>` to overwrite the contents of a file with the new output, replacing anything that was there before.
        - **Option 2:** Use `>>` to append the new output to the end of an existing file, as in `echo Hello >> newfile.txt`.
    - This redirection isn't limited to the `echo` command; it can be applied to any command's output. For example, `ls > content.txt` saves the output of the `ls` command into a new file called `content.txt`.
2. **`|` Symbol (Pipe):**
    - The pipe character `|` allows you to redirect the output of one command to another command as input. For instance, you can take the output of `ifconfig` and filter it through `grep` to search for the term "inet":
    
    ```bash
    ifconfig | grep -i "inet"
    ```
    
    You can also chain multiple commands together. For example, after filtering with `grep`, you might want to further process the output using the `cut` command:
    
    ```bash
    ifconfig | grep -i "inet " | cut -d ":" -f 2
    ```
    
    In this example, the `cut` command splits each line using the colon `:` as a delimiter and then extracts the **second** field from each line.
    
3. **`&&` Symbol (Logical AND):** The `&&` operator is used to run multiple commands sequentially, but only if the preceding command is successful. For instance, if you want to compile a program and then run it, you could use:
    
    ```bash
    gcc myprogram.c -o myprogram && ./myprogram
    ```
    
    Here, the program will only be executed if the compilation is successful.
    
4. **`;` Symbol (Command Separator):** The semicolon `;` is used to run multiple commands sequentially, regardless of whether the previous command was successful or not. For example:
    
    ```bash
    mkdir new_folder; cd new_folder; touch file.txt
    ```
    
    This sequence will create a new directory, change into that directory, and then create a new file within it, regardless of the success or failure of each step.
    
5. **`&` Symbol (Background Execution):** The ampersand `&` allows you to run a command in the background so that you can continue using the terminal for other tasks. For example:
    
    ```bash
    long_running_command &
    ```
    
    This will run `long_running_command` in the background, freeing up the terminal for other commands.
    
6. **`||` Symbol (Logical OR):** The `||` operator is used to execute the second command only if the first command fails. For example:
    
    ```bash
    mkdir new_folder || echo "Failed to create directory"
    ```
    
    Here, the message will be printed only if the `mkdir` command fails.
    

Read [What Are stdin, stdout, and stderr on Linux?](https://www.howtogeek.com/435903/what-are-stdin-stdout-and-stderr-on-linux/#:~:text=In%20Linux%2C%20stdin%20is%20the,stderr%20(standard%20error)%20stream.)

---

**[ Regular Expressions ]**

How to get all subdomains for `yahoo` form the main `yahoo.com` page? First we need to download the index.html:

```bash
wget yahoo.com
```

Search for `yahoo.com`:

```bash
cat index.html | grep -i "yahoo.com"
```

Only get the result, not all line that our result in:

```bash
cat index.html | grep -i -o "yahoo.com"
```

This only return all time that yahoo.com appears in that file.

We will make a small regex that searches for all of characters or numbers that maybe have anything after them, and at the end there is `.yahoo.com`.

```bash
cat index.html | grep -i -o "[a-z0-9]*.yahoo.com"
```

But now we have some duplicates, to remove them we could use:

```bash
cat index.html | grep -i -o "[a-z0-9]*.yahoo.com" | uniq
```

We could also remove duplicates and sort them in one shot as:

```bash
cat index.html | grep -i -o "[a-z0-9]*.yahoo.com" | sort -u
```

We could use `grep` without `cat` as:

```bash
grep -i -o "[a-z0-9]*.yahoo.com" index.html | sort -u
```

To store the output in a file

```bash
grep -i -o "[a-z0-9]*.yahoo.com" index.html | sort -u > output.txt
```

To store the output in a file and in the same printing out the result

```bash
grep -i -o "[a-z0-9]*.yahoo.com" index.html | sort -u | tee output.txt
```

Test your regular expressions at https://regex101.com/

---

**[ System Monitoring and Resource Management ]**

1. **`ps` Command (Process Status):** The `ps` command displays information about running processes. By default, it shows processes with the same user ID and terminal as the current user. The output includes the process ID (PID), terminal (TTY), cumulative CPU time (TIME), and the executable name (CMD). For example:
    
    ```bash
    ps aux  # Simple usage is `ps`.
    ```
    
    This command lists all processes with details like user, CPU, and memory usage.
    
2. **`df` Command (Disk Free):** The `df` command reports available disk space on file systems. It’s useful for monitoring disk usage. For example:
    
    ```bash
    df -h
    ```
    
    This command displays disk space usage in a human-readable format, showing sizes in GB or MB.
    
3. **`top` and `htop` Commands:** The `top` command provides a real-time view of system processes, including CPU and memory usage. It’s an interactive tool for monitoring system performance. For example:
    
    ```bash
    top
    ```
    
    Running this command opens an interface displaying resource-intensive processes and overall system performance. For a more user-friendly alternative, you can use `htop`, which offers a more visual and interactive display, including easy navigation and additional features like process sorting and filtering.

   ---
   ---
