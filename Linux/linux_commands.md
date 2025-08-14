# Linux Command and System Reference

## Commands

### Manuals
- `man [term]` – Show the manual for a command.  
- `[term] --help` – List all available flags and usage.

### SSH & User Management
- `ssh tryhackme@10.10.199.173` – Connect to a remote server via SSH.  
- `su -l user` – Switch to another user account.

### File Editing
- `nano [file]` – Edit text files.

### File Transfer
- `wget [URL]` – Download files over HTTP.  
- `scp [source_file] [user@destination:/path]` – Copy files securely over SSH.  
  Example:  
  ```bash
  scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt
Process Management
ps – List running processes.

ps aux – List all processes including system and other users’ processes.

kill [PID] – Terminate a process. Options:

SIGTERM – Gracefully terminate, allows cleanup.

SIGKILL – Force kill, no cleanup.

SIGSTOP – Suspend a process.

systemctl [start|stop|enable|disable] [service] – Manage services.

fg – Bring background process to foreground.

Basic Commands
echo – Print text.

whoami – Show current user.

ls – List files.

ls -lh – List files with permissions and sizes.

cat – Display file content.

pwd – Show current directory.

find – Locate files.

* – Wildcard for files.

wc – Word count.

grep – Search text patterns.

touch [file] – Create a new file.

mkdir [dir] – Create a directory.

cp [source] [dest] – Copy files or directories.

mv [source] [dest] – Move or rename files/directories.

rm [file] – Remove files.

file [file] – Determine file type.

Shell Operators
& – Run command in background, use fg to bring to foreground.

&& – Combine multiple commands sequentially.

> – Redirect output, overwriting file.

bash
Copy
Edit
echo hey > welcome
>> – Redirect output, appending to file.

Common Directories
/etc – OS configuration files.

/var – Application files, logs.

/tmp – Temporary data, cleared on reboot.

Webserver
Run Python webserver:

bash
Copy
Edit
python3 -m http.server
Download file from webserver (new terminal):

bash
Copy
Edit
wget http://10.10.169.65:8000/myfile
Cron Jobs
Crontab Generator – Tool to generate cron syntax.

Crontab format:
| Field | Description |
|-------|-------------|
| MIN | Minute to execute |
| HOUR | Hour to execute |
| DOM | Day of month |
| MON | Month |
| DOW | Day of week |
| CMD | Command to execute |

Example:

bash
Copy
Edit
0 */12 * * * cp -R /home/cmnatic/Documents /var/backups/
Software Management
apt – Install or manage software.
Benefits: Automatically checks for updates via repositories.

Adding GPG Key & Repository (Sublime Text Example)
Add GPG key:

bash
Copy
Edit
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
Add repository file in /etc/apt/sources.list.d/sublime-text.list.

Update apt:

bash
Copy
Edit
sudo apt update
Install software:

bash
Copy
Edit
sudo apt install sublime-text
Remove packages:

bash
Copy
Edit
sudo apt remove sublime-text
Network
ss – Display socket statistics.
