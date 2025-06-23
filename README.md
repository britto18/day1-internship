# Day1 Internship
## Network Scanning Steps

```bash
# Step 1: Find your own IP address
ifconfig

# Step 2: Identify the IP range and perform a ping sweep
nmap <your-ip>/24

# Step 3: Scan the identified range using a TCP SYN scan
nmap -sS <target-ip-range>
```

## Commonly Open Ports Found

| Port      | Service         | Description                                 | Common Vulnerabilities / Risks                                       |
|-----------|------------------|---------------------------------------------|----------------------------------------------------------------------|
| 135/tcp   | msrpc            | Microsoft RPC service                       | Used in DCOM exploits, MS03-026 (Blaster worm), privilege escalation |
| 445/tcp   | microsoft-ds     | SMB over TCP                                | EternalBlue (MS17-010), WannaCry, SMB relay attacks                  |
| 902/tcp   | iss-realsecure   | VMware Server Console Port                  | May expose VMware services to remote exploitation if not patched     |
| 912/tcp   | apex-mesh        | Often used by backup/monitoring tools       | Rarely used; can be misconfigured and expose internal services       |
| 4343/tcp  | unicall          | Used by proprietary comms (rare)            | Not standardized – can host custom or legacy vulnerable services     |
| 4449/tcp  | privatewire      | Unknown/private service                     | Often used in custom applications, may lack authentication/logging   |
| 7070/tcp  | realserver        | RealAudio/RealServer Streaming              | Directory traversal, remote code execution (RCE) vulnerabilities     |

