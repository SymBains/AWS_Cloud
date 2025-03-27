## Commands Cheat Sheet

### System Information
- `uname` - Print system information  
   - `uname -a` - Displays all system information
- `whoami` - Displays the current logged-in user
- `cat` - View contents of a file
  - `cat /etc/shells` - Lists all available shells
- `ps -p $$` - Shows the shell you are currently using

### Navigation & History
- Press `↑` (up arrow) - Navigate through previous commands
- `history` - Shows the last 500 commands used
- `history -c` - Clears the command history
- `pwd` - Prints the present working directory

### File & Directory Management
- `ls` - Lists files and folders
- `cp <source> <destination>` - Copy files or directories
- `rm <file>` - Remove a file
   - `rm -r <directory>` - Remove a directory recursively
- `mkdir <directory>` - Create a new directory
- `touch <file>` - Create a blank file
- `mv <file> <directory>` - Move a file to a directory
- `file <file>` - Displays the file type

### Viewing & Editing Files
- `cat <file>` - View the contents of a file
- `nano <file>` - Opens the file in the nano text editor  
   - `Ctrl + X` - Close nano
- `head -<number> <file>` - Show the first N lines of a file
- `tail -<number> <file>` - Show the last N lines of a file
- `nl <file>` - Numbers the lines of a file
- `cat <file> | grep <search-term>` - Highlight and show matching lines containing the search term

### Network & Downloads
- `curl <url>` - Transfer data (general-purpose)
- `wget <url>` - Download files and folders (preferred)

### Permissions & Superuser
- `sudo <command>` - Run a command as a superuser
- `sudo apt update -y` - Update package lists (add `-y` to auto-confirm)
- `sudo apt install <package>` - Install a package
- `sudo apt upgrade -y` - Upgrade all packages
- `sudo su` - Temporarily switch to the superuser
- `exit` - Exit from superuser mode

### Manual & Help
- `man <command>` - Displays the manual page for the command

### Example: NGINX Commands
- `sudo apt install nginx -y` - Install the NGINX web server
- `sudo systemctl status nginx` - Check the status of the NGINX service

### Useful Tips
- `Tab` - Auto-complete file and directory names
