# Metasploit and Meterpreter Reference

## Core Commands
- `background`: Sends the current session to the background
- `exit`: Terminates the Meterpreter session
- `guid`: Retrieves the session's Globally Unique Identifier (GUID)
- `help`: Shows the help menu
- `info`: Provides details about a Post module
- `irb`: Launches an interactive Ruby shell in the current session
- `load`: Loads one or more Meterpreter extensions
- `migrate`: Moves Meterpreter to a different process
- `run`: Runs a Meterpreter script or Post module
- `sessions`: Switches to another session quickly

## File System Commands
- `cd`: Changes the current directory
- `ls`: Lists files in the current directory (also works with `dir`)
- `pwd`: Displays the current working directory
- `edit`: Edits a file
- `cat`: Shows the contents of a file
- `rm`: Deletes a specified file
- `search`: Searches for files
- `upload`: Uploads a file or directory
- `download`: Downloads a file or directory

## Networking Commands
- `arp`: Shows the host's ARP cache
- `ifconfig`: Lists available network interfaces on the target
- `netstat`: Displays active network connections
- `portfwd`: Forwards a local port to a remote service
- `route`: Views or modifies the routing table

## System Commands
- `clearev`: Clears event logs
- `execute`: Runs a specified command
- `getpid`: Displays the current process ID
- `getuid`: Shows the user account under which Meterpreter is running
- `kill`: Terminates a process by ID
- `pkill`: Terminates processes by name
- `ps`: Lists running processes
- `reboot`: Reboots the target system
- `shell`: Opens a system command shell
- `shutdown`: Powers off the target system
- `sysinfo`: Retrieves system information, such as the operating system

## Other Commands
These appear under various categories in the help menu:
- `idletime`: Shows how long the remote user has been idle
- `keyscan_dump`: Exports the keystroke buffer
- `keyscan_start`: Begins capturing keystrokes
- `keyscan_stop`: Stops capturing keystrokes
- `screenshare`: Streams the remote desktop in real time
- `screenshot`: Captures a screenshot of the active desktop
- `record_mic`: Records audio from the default microphone for a specified duration
- `webcam_chat`: Initiates a video chat
- `webcam_list`: Lists available webcams
- `webcam_snap`: Takes a snapshot from a specified webcam
- `webcam_stream`: Streams video from a specified webcam
- `getsystem`: Attempts to escalate privileges to SYSTEM level
- `hashdump`: Extracts the contents of the SAM database

## Metasploit Framework Commands
- `use [module]`: Loads a module (e.g., `use exploit/windows/smb/ms17_010_eternalblue`)
- `msfconsole`: Launches the Metasploit console
- **Within a module**:
  - `show options`: Displays configurable options
  - `show payload`: Lists available payloads
  - `info`: Shows module details
  - `back`: Exits the current module
  - `exploit -z` or `run`: Executes the module (`-z` runs it in the background)
  - `check`: Tests if the target is vulnerable without exploiting
  - `sessions`: Lists active sessions
  - `session -i [session number]`: Interacts with a specific session
- `search ms17-010`: Searches modules using a CVE number
- `search type:auxiliary telnet`: Searches by module type
- `set PARAMETER_NAME VALUE`: Sets a parameter value
- `unset all`: Clears all parameter values
- `setg` / `unsetg`: Sets or clears parameters globally across modules
- **Meterpreter-specific**:
  - `background`: Sends the Meterpreter session to the background
