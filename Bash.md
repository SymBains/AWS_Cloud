## How can we set a variable in BASH?

- Use `variable_name="value"` to set a variable
  - `name="John"`
  - To reference the variable later, use `$` e.g. `echo $name`
    - `echo $name` - prints the variable's value

## What are environment variables?
- Special variables that affect the shell and processes' behavior
- Environment variables in Linux are dynamic values that affect the processes or programs on a computer. They can store information such as the location of temporary files, the default editor to be used, system paths, or details about the session profile.
- They are inherited by child processes and can be accessed system-wide.
- Examples: `PATH`, `HOME`, `USER`.
    - echo `$HOME` - Shows your home directory
    - echo `$PATH` - Shows system search paths

## How can we set up an environment variable?

- Use `export` to make a variable available to child processes
  - A child process in computing is a process created by another process (the parent process).  

## How can you make an environment variable persistent?
To persist across sessions, add the export line to:
- For current user only: ~/.bashrc or ~/.bash_profile
- For all users: /etc/environment or /etc/profile

``` bash
echo 'export MY_VAR="value"' >> ~/.bashrc
source ~/.bashrc  # Reload to apply
```

## What is a Process?
Whenever a command is issued in Unix/Linux, it creates/starts a new process. For example, pwd when issued which is used to list the current directory location the user is in, a process starts. Through a 5 digit ID number Unix/Linux keeps an account of the processes, this number is called process ID or PID.

## How can we see running processes?
`ps` (Process Status)
```bash
ps aux  # Show all running processes
``` 

- `top` - Interactive process viewer
- `htop` - More advanced (if installed)

## What are child processes?

- A child process is created by a parent process.
- Example: Running ls from a shell makes ls a child of the shell.

Use `pstree` to visualize process hierarchy

## How can you run a process in the background, rather than the foreground?

- Add & to the command
  - sleep 100 & - Runs in background
  - jobs - Check background jobs
  - fg %1 - Bring job back to foreground

## How can you end a process?

- By PID(The Process ID (PID) is a unique identifier assigned to each process running in a Linux operating system):
```bash
kill 1234  # Graceful termination (SIGTERM)
kill -9 1234  # Force kill (SIGKILL)
```

- By name
```bash
pkill process_name
killall process_name
```

## Explain the Linux permission system

- Every file/directory has 3 permission types:
  - Owner (u) – User who owns the file.
  - Group (g) – Group that owns the file.
  - Others (o) – Everyone else.

- 3 basic permissions:
  - Read (r) – View file contents.
  - Write (w) – Modify file.
  - Execute (x) – Run as a program/script.

- Example: -rw-r--r-- means:
  - User: read/write
  - Group: read-only
  - Others: read-only

## Explain the shorthand permission system (numbers)
- Permissions are represented in octal (0-7):
  - 4 = Read (r)
  - 2 = Write (w)
  - 1 = Execute (x)

- Add them to set combined permissions:
  - 7 = 4+2+1 (rwx)
  - 6 = 4+2 (rw-)
  - 5 = 4+1 (r-x)

Example:

`chmod 755 file` → `rwxr-xr-x` (Owner: rwx, Group/Others: r-x)
`chmod 644 file` → `rw-r--r--` (Owner: rw-, Group/Others: r--)

chmod = change mode

## How can you change the permissions on a file?

- Using chmod (Change Mode):
```bash
chmod u+x file.sh  # Add execute for owner
chmod go-w file.txt  # Remove write for group & others
chmod 755 script.sh  # Set rwxr-xr-x (numeric)
```

- Changing ownership with chown:
```bash
chown user:group file.txt
```


