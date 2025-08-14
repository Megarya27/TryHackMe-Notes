# Windows Commands and PowerShell Reference

## System Configuration
- **msconfig** – Open System Configuration via Run.  
- **Active Directory (AD)** – Manage computers on a network and apply policies according to organizational units.

---

## Command Prompt (cmd.exe)

### Basic Help
- `cmd /?` – Show command-line help.

### System Info
- `set` – Display current environment variables and paths.  
- `ver` – Show OS version.  
- `systeminfo` – Detailed system information.  
- `| more` – Paginate long output.

### Networking
- `ipconfig /all` – Display full network configuration.  
- `ping [domain]` – Test connectivity.  
- `tracert [domain]` – Trace route to a host.  
- `nslookup [domain]` – Query DNS records.  
- `netstat` – Show active connections and listening ports.

### File Operations
- `dir /a` – List all directories including hidden ones.  
- `copy` – Copy files.  
- `move` – Move or rename files.  
- `del` – Delete files.  
- `type [file]` – Display file content. Use `| more` for long files.

### Process Management
- `tasklist` – List running processes.  
- `tasklist /FI "imagename eq sshd.exe"` – Search for a specific process.  
- `taskkill /PID target_pid` – Kill a process.

### Shutdown / Restart
- `shutdown /r` – Restart the computer.  
- `shutdown /s` – Shutdown the computer.

---

## PowerShell

### Cmdlets
- PowerShell commands are called **cmdlets**, following **Verb-Noun** convention.

### Command Discovery
- `Get-Command` – List all cmdlets.  
- `Get-Command -CommandType "Function"` – Filter commands by type.  
- `Get-Command -Name "Remove*"` – List commands starting with “Remove”.  
- `Get-Help` – Show command documentation.  
- `Get-Help [Cmdlet] -examples` – Show usage examples.

### File and Directory
- `Get-ChildItem` – List files and directories.  
- `Set-Location -Path ".\Documents"` – Change directory.  
- `New-Item -Path ".\captain-cabin\captain-wardrobe" -ItemType "Directory"` – Create a new directory.  
- `Remove-Item` – Delete files or directories.  
- `Copy-Item` – Copy files or directories.  
- `Get-Content` – Display file contents.  
- `Select-String -Path ".\captain-hat.txt" -Pattern "hat"` – Search for text in a file.  
- `Get-ChildItem | Sort-Object Length -Descending | Select-Object -First 1` – Get largest file.  
- `Get-ChildItem | Where-Object -Property Length -gt 100` – Filter items larger than 100 bytes.

### Remote Execution
- `Invoke-Command` – Execute commands on remote systems.

### System and Network Info
- `Get-ComputerInfo` – Full system information.  
- `Get-LocalUser` – List local users.  
- `Get-NetIPConfiguration` – Network configuration summary.  
- `Get-NetIPAddress` – Show IP addresses.  
- `Get-Process` – List running processes.  
- `Get-Service` – List services.  
- `Get-NetTCPConnection` – Show active TCP connections.  
- `Get-FileHash` – Compute file hash.
