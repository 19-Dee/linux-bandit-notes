# Bandit Level 3 → 4

## Commands Used

```bash
cd /home/bandit3
ls
ls -a
cat inhere/...Hiding-From-You
```

## What I Learned

- Linux files beginning with `.` are treated as hidden files.
- `ls` does not display hidden files by default.
- `ls -a` displays all entries, including hidden files.
- Hidden files can be accessed normally once their names are known.

## Difficulties

- Initially couldn't locate the file using `ls`.
- Used `ls -a` to reveal the hidden file and retrieved the password using `cat`.
