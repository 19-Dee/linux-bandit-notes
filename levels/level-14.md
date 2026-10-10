# Bandit Level 14 → 15

## Commands Used

```bash
echo "CURRENT_PASSWORD" > /tmp/bandit14-pass.txt
nc localhost 30000 < /tmp/bandit14-pass.txt
```

## What I Learned

- `nc` (Netcat) can establish TCP connections to network services.
- `localhost` refers to the machine on which the command is running.
- A port number identifies the destination service.
- `<` redirects a file into a process's standard input.
- Netcat can send data to a service and display its response.

## Difficulties

- Initially didn't understand how to submit the password to a service listening on a specific port.
- Needed help identifying the appropriate commands.
- Used `echo` to save the current password into a temporary file.
- Used `nc` with input redirection to submit the password to port 30000.
- Successfully received the password for the next level.
