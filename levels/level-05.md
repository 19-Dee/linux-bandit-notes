# Bandit Level 4 → 5

## Commands Used

```bash
file -- ./-file00
file -- ./*
cat ./-file07
```

## What I Learned

- `file` examines a file's contents to identify its type.
- `data` is a generic classification for files whose format cannot be identified more specifically.
- `ASCII text` indicates that a file contains text encoded using ASCII.
- `*` is a wildcard that the shell expands to match filenames.
- `file -- ./*` allows me to inspect multiple files in a directory using a single command.

## Difficulties

- Initially considered using `cat` to inspect each file individually.
- Tried combining `ls` and `cat`, as well as experimenting with `grep`, but couldn't find a working solution.
- Discovered the `file` command and tested it against an individual file.
- Used `file -- ./*` to identify the ASCII text file and retrieved the password using `cat`.
