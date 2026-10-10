# Bandit Level 19 → 20

## Commands Used

```bash
ls
cat bandit20-do
file bandit20-do
./bandit20-do
./bandit20-do cat /etc/bandit_pass/bandit20
```

## What I Learned

- `file` can identify executable binaries and whether they have the setuid bit enabled.
- Setuid allows an executable to run with the effective user ID of its owner rather than the user executing it.
- `./` can be used to execute a program located in the current directory.
- `cat` displays file contents, whereas executing a binary runs its instructions.
- A setuid executable can access files using its owner's effective permissions.
- Setuid doesn't necessarily grant root privileges; it depends on who owns the executable.

## Difficulties

- Initially used `cat` on the executable, which produced unreadable binary output.
- Discovered that `bandit20-do` was a setuid executable but initially misunderstood setuid as a command that needed installing.
- Experimented with `setuid`, explored `/sbin`, and attempted to use `setuids.bt`, but encountered errors and permission restrictions.
- Learned that I needed to execute `bandit20-do` rather than read it.
- Used the executable to run `cat` with Bandit 20's effective permissions and successfully retrieved the password.
