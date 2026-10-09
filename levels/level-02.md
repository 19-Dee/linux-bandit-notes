# Bandit Level 1 → 2

## Commands Used

```bash
ls
cat -
pwd
cat /home/bandit1/-
```

## What I Learned

- `ls` lists files in a directory.
- `pwd` prints the absolute path of the current working directory.
- `cat -` reads from standard input rather than opening a file named `-`.
- Files with special names can be accessed using explicit paths.
- `Ctrl+C` interrupts a running process.
- Absolute paths specify a file's location from the filesystem root.

## Difficulties

- Initially attempted to read the file using `cat -`, but the command waited for input.
- Used `Ctrl+C` to interrupt the process.
- Experimented with navigating directories, `chmod`, and `sudo`, but couldn't resolve the issue.
- Researched the problem on Stack Overflow and discovered that specifying the file's path would work.
- Used `pwd` to identify the working directory and constructed the absolute path to retrieve the password.
