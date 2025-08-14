# Metasploit Configuration Parameters

- **RHOSTS**: "Remote host" specifies the target system's IP address. It can be a single IP, a network range using CIDR notation (e.g., `/24`, `/16`), or a range (e.g., `10.10.10.x-10.10.10.y`). Alternatively, use a file listing targets (one per line) with `file:/path/to/target_file.txt`.

 ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/603df7900d7b6f1dff18b0bd/room-content/138a36f26c25994fcfe47e1fab085ac8.png)

- **RPORT**: "Remote port" defines the port on the target system where the vulnerable application is running.

- **PAYLOAD**: Specifies the payload to be used with the exploit.

- **LHOST**: "Local host" refers to the IP address of the attacking machine (e.g., AttackBox or Kali Linux).

- **LPORT**: "Local port" is the port on the attacking machine used for the reverse shell connection. Choose any port not in use by other applications.

- **SESSION**: Each connection to the target system in Metasploit is assigned a session ID. This ID is used with post-exploitation modules to interact with the target via an existing connection.


