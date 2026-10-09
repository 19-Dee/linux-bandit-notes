# Bandit Level 0

## Commands Used

```bash
ssh
ssh -l bandit0 bandit.labs.overthewire.org -p 2220
```

## What I Learned

- SSH (Secure Shell) allows me to securely connect to a remote machine.
- SSH uses port 22 by default, but a different port can be specified using the `-p` flag.
- The `-l` flag allows me to specify the username I want to log in as.
- Alternatively, I can specify the username using the `username@hostname` format.
- Once connected, SSH prompts for the password associated with the specified user.

## Difficulties

- Initially attempted to connect without specifying a port, which meant SSH tried the default port 22.
- Investigated the available SSH options and discovered the `-p` flag, which allows me to specify a different port.
- Initially expected SSH to prompt me for both a username and password.
- Realised I needed to specify the username using the `-l` flag before entering the password.
- Successfully connected to the Bandit machine after correcting the command.
