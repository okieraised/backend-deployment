# 🐧 Useful Ubuntu/Linux Commands

## 🔹 File and Directory Operations

| Command | Description |
|--------|-------------|
| `ls -l` | List files in long format |
| `ls -a` | List all files (including hidden) |
| `cd <dir>` | Change directory |
| `pwd` | Show current directory |
| `mkdir <dir>` | Create a new directory |
| `rm <file>` | Delete a file |
| `rm -r <dir>` | Delete a directory recursively |
| `cp <src> <dest>` | Copy file or directory |
| `mv <src> <dest>` | Move or rename a file |
| `touch <file>` | Create an empty file |

---

## 🔹 Searching and Finding

| Command | Description |
|--------|-------------|
| `find . -name "*.log"` | Find files by name |
| `grep "text" file.txt` | Search for text in a file |
| `grep -r "text" ./dir` | Recursively search in directory |
| `locate <filename>` | Quickly find file by name (requires `mlocate`) |

---

## 🔹 File Viewing and Editing

| Command | Description |
|--------|-------------|
| `cat <file>` | Print file content |
| `less <file>` | View file with scroll |
| `head -n 10 <file>` | First 10 lines of a file |
| `tail -n 10 <file>` | Last 10 lines |
| `nano <file>` | Open file with Nano editor |
| `vim <file>` | Open file with Vim editor |

---

## 🔹 Package Management (APT)

| Command | Description |
|--------|-------------|
| `sudo apt update` | Update package list |
| `sudo apt upgrade` | Upgrade all packages |
| `sudo apt install <package>` | Install a package |
| `sudo apt remove <package>` | Remove a package |
| `sudo apt autoremove` | Remove unused packages |
| `dpkg -l` | List installed packages |

---

## 🔹 System Information

| Command | Description |
|--------|-------------|
| `uname -a` | Kernel and architecture info |
| `lsb_release -a` | OS version info |
| `hostnamectl` | Show system hostname and OS info |
| `df -h` | Disk usage |
| `du -sh <dir>` | Size of directory |
| `free -h` | Memory usage |
| `uptime` | System uptime and load average |

---

## 🔹 Process and Resource Monitoring

| Command | Description |
|--------|-------------|
| `top` | Real-time process viewer |
| `htop` | Enhanced process viewer (requires install) |
| `ps aux` | List all running processes |
| `kill <pid>` | Terminate a process |
| `kill -9 <pid>` | Force kill |
| `nice` / `renice` | Set process priority |

---

## 🔹 Networking

| Command | Description |
|--------|-------------|
| `ip a` | Show IP addresses |
| `ip r` | Show routing table |
| `ping <host>` | Ping a host |
| `traceroute <host>` | Trace network path (use `sudo apt install traceroute`) |
| `netstat -tuln` | Show open ports (use `ss -tuln` on newer distros) |
| `curl <url>` | Fetch data from URL |
| `wget <url>` | Download a file |

---

## 🔹 User Management

| Command | Description |
|--------|-------------|
| `whoami` | Show current user |
| `id` | Show UID, GID and groups |
| `adduser <name>` | Add a new user |
| `sudo passwd <name>` | Set user password |
| `usermod -aG <group> <user>` | Add user to a group |
| `deluser <name>` | Remove a user |

---

## 🔹 Permissions

| Command | Description |
|--------|-------------|
| `chmod +x <file>` | Make a file executable |
| `chmod 755 <file>` | Set permissions |
| `chown user:group <file>` | Change ownership |
| `sudo` | Run a command as superuser |
| `sudo su` | Switch to root shell |

---

## 🔹 Archives and Compression

| Command | Description |
|--------|-------------|
| `tar -czf file.tar.gz dir/` | Compress a directory |
| `tar -xzf file.tar.gz` | Extract a `.tar.gz` file |
| `zip -r file.zip dir/` | Create a zip archive |
| `unzip file.zip` | Extract a zip file |

---

## 🔹 System Services (systemd)

| Command | Description |
|--------|-------------|
| `systemctl status <service>` | Show service status |
| `systemctl start <service>` | Start a service |
| `systemctl stop <service>` | Stop a service |
| `systemctl restart <service>` | Restart a service |
| `systemctl enable <service>` | Start on boot |
| `systemctl disable <service>` | Disable on boot |

---

## 🔹 Disk & Devices

| Command | Description |
|--------|-------------|
| `lsblk` | List block devices |
| `mount` / `umount` | Mount or unmount file systems |
| `df -Th` | Show mounted filesystems with types |
| `fdisk -l` | Show disk partitions |

---

## 🔹 Miscellaneous

| Command | Description |
|--------|-------------|
| `history` | Show command history |
| `alias ll='ls -l'` | Create command alias |
| `date` | Show current date/time |
| `cal` | Show calendar |
| `uptime` | How long system has been running |

---

## 🔹 Keyboard Shortcuts in Terminal

| Shortcut | Description |
|----------|-------------|
| `Ctrl + C` | Kill current process |
| `Ctrl + Z` | Suspend process |
| `Ctrl + D` | Logout or EOF |
| `Ctrl + L` | Clear screen |
| `!!` | Repeat last command |
| `!n` | Run command number n from history |

---

