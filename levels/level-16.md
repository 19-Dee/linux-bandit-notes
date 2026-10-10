# Bandit Level 16 → 17

## Commands Used

```bash
nmap localhost -p 31000-32000 -PS
nmap -sV -p 31046,31518,31691,31790,31960 localhost

echo "CURRENT_PASSWORD" | ncat localhost 31518 --ssl
echo "CURRENT_PASSWORD" | ncat localhost 31790 --ssl
```

## What I Learned

- `nmap` scans ports to identify which ones are open.
- `-p` specifies the ports or port range to scan.
- `nmap -sV` attempts to identify the services and protocols running on open ports.
- An open TCP port doesn't necessarily mean the service supports TLS.
- `ncat --ssl` establishes a TLS-encrypted connection.
- Some services simply echo back the data they receive, while others process the input and return a different response.
- SSH private keys can be used to authenticate to remote servers.

## Difficulties

- Initially identified five open ports but wasn't sure how to determine which services supported TLS.
- Experimented with `nmap -sV`, but the scan took longer than expected.
- Had some confusion around pipes, input redirection, and the `-p` option in Ncat.
- Corrected the command syntax to pipe the password into Ncat.
- Tested port 31518, which echoed the current password.
- Tested port 31790, which returned the private SSH key needed for Bandit 17.
