# Bandit Level 0 → 1

## Commands Used

```bash
cat readme
exit
ssh -p 2220 -l bandit1 bandit.labs.overthewire.org
```

## What I Learned

- `cat` displays the contents of a file in the terminal.
- `exit` terminates the current shell session, returning me to my local terminal when used in an SSH session.
- SSH allows me to connect to a remote machine using different user accounts.
- Passwords for subsequent Bandit levels can be retrieved from files on the remote machine.

## Difficulties

- Initially considered SSHing directly from Bandit 0 into Bandit 1.
- Instead, used `exit` to return to my MacBook's terminal and established a new SSH connection using the Bandit 1 credentials.
- Saved the password in a local text file organised within a folder for the level.
