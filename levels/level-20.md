# Bandit Level 20 → 21

## Commands Used

```bash
./suconnect
./suconnect whoami
./suconnect localhost whoami
./suconnect 22
./suconnect 2220
./suconnect 443
./suconnect 8080

# Terminal 1: Start a TCP listener
nc -l -p 12345

# Terminal 2: Connect to the listener
./suconnect 12345

# Terminal 1: Enter the Bandit 20 password and press Enter
```

## What I Learned

- `nc` (Netcat) can operate as both a TCP client and a TCP listener.
- `nc -l -p 12345` listens for incoming TCP connections on port 12345.
- A client must connect to the same port that the server is listening on.
- Port 12345 was an arbitrary choice; any available, permitted port could have been used.
- Ports 22 and 2220 were already being used by SSH services, which is why they returned SSH identification strings rather than the expected password.
- Two processes can communicate over TCP using `localhost`, even when running in separate terminal sessions on the same machine.
- A setuid executable can communicate over a network connection while running with its owner's effective permissions.

## Difficulties

- Initially misunderstood the port argument and tried passing `whoami` and `localhost`.
- Tried connecting to existing ports, including 22, 2220, 443 and 8080, without realising I needed to create my own listener.
- Learned how to start a Netcat listener and used two SSH sessions to run the listener and `suconnect` simultaneously.
- Sent the current password through the TCP connection and successfully retrieved the next password.
- Clarified why we used port 12345 instead of an existing SSH port.
