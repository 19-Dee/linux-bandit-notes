# Bandit Level 15 → 16

## Commands Used

```bash
echo "CURRENT_PASSWORD" | ncat --ssl -p 30001
echo "CURRENT_PASSWORD" | ncat localhost --ssl -p 30001
echo "CURRENT_PASSWORD" | ncat localhost 30001 --ssl
```

## What I Learned

- `ncat` can establish TCP connections with TLS encryption.
- `--ssl` enables TLS for the connection.
- TLS encrypts data transmitted between the client and server.
- The `-p` option in `ncat` specifies the local source port rather than the destination port.
- A pipe (`|`) passes the output of `echo` into `ncat` through standard input.

## Difficulties

- Initially experimented with Netcat before trying Ncat.
- Used `-p 30001` incorrectly when attempting to specify the destination port.
- Encountered connection errors while experimenting with the command syntax.
- Corrected the command by specifying `localhost 30001 --ssl`.
- Successfully established a TLS connection and retrieved the next password.
