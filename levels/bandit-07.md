# Bandit Level 6 → 7

## Commands Used

```bash
ls * -la
find *
find * | grep "bandit7"
cat /path/to/password/file
```

## What I Learned

- `find` can search for files across directories.
- `grep` can filter the output of `find` to locate matching file paths.
- Linux files have ownership information identifying their user and group.
- Searching a large part of the filesystem can produce extensive output and permission errors.

## Difficulties

- Initially tried combining `ls -la` with `grep` to search for files matching the required size, owner, and group.
- Encountered permission errors when exploring directories.
- Experimented with `find` and accidentally generated a very large list of files.
- Used `find` with `grep` to locate a path containing `bandit7`.
- Read the password file using `cat` and verified the password by successfully connecting as `bandit7`.
