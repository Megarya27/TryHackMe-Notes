# Nmap Reference

## Target Specification
- IP Range: Scan all IPs in a range
`192.168.0.1-10`  # From 192.168.0.1 to 192.168.0.10
- Subnet: Scan a subnet using CIDR notation
`192.168.0.1/24`  # Equivalent to 192.168.0.0-255
- Hostname: Scan using a hostname
`example.thm`

Example: Discover online hosts on a network
`nmap -sn 192.168.66.0/24`

## Scan Types
`-sT`  TCP connect scan – complete three-way handshake
`-sS`  TCP SYN scan – first step only (stealthy)
`-sU`  UDP scan
`-F`   Fast mode – scans 100 most common ports
`-p[range]`  Specify port range (`-p-` scans all ports)

## Detection Options
`-O`   OS detection
`-sV`  Service and version detection
`-A`   OS detection, version detection, plus extras
`-Pn`  Scan hosts that appear down

## Timing and Performance
`-T<0-5>`  Timing template – paranoid (0), sneaky (1), polite (2), normal (3), aggressive (4), insane (5)
`--min-parallelism <numprobes>` / `--max-parallelism <numprobes>`  Min/max number of parallel probes
`--min-rate <number>` / `--max-rate <number>`  Min/max packets per second
`--host-timeout <time>`  Maximum wait time for a host

## Output Options
`-oN <filename>`  Normal output
`-oX <filename>`  XML output
`-oG <filename>`  Grepable output (for grep or awk)
`-oA <basename>`  Output in all major formats

## Real-Time Output
`-v`  Verbosity level (`-vv`, `-v4` for more detail)
`-d`  Debugging level (`-d` to `-d9`)
