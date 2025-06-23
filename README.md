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
