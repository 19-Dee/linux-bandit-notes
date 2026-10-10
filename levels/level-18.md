# Bandit Level 18 → 19

## Commands Used

```bash
ssh -i bandit17.key bandit.labs.overthewire.org -p 2220 -l bandit18 cat ./readme
```

## What I Learned

- SSH can execute commands on a remote server without opening an interactive terminal session.
- A remote command can be specified after the SSH connection arguments.
- SSH returns the remote command's output to the local terminal.
- Running a remote command can avoid interactive shell startup behaviour that would otherwise terminate the session.

## Difficulties

- Initially didn't know that SSH could execute individual commands remotely.
- The Bandit 18 shell was configured to log out interactive SSH sessions automatically.
- Learned about remote command execution and used it to read the `readme` file without opening an interactive session.
- Successfully retrieved the password for Bandit 19.
