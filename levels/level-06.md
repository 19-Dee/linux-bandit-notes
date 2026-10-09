# Bandit Level 5 → 6

## Commands Used

```bash
ls * -la | grep -E "1033|maybe"
```

## What I Learned

- `ls -la` displays detailed file information, including permissions and file sizes.
- `*` expands to matching files and directories.
- `|` pipes the output of one command into another.
- `grep` filters lines matching a specified pattern.
- `grep -E` enables extended regular expressions, allowing `|` to act as an OR operator.
- Combining commands allows me to filter results and locate files matching specific criteria.

## Difficulties

- Initially used `ls * -la` with `grep` to identify the file matching the required size of 1033 bytes.
- The output showed the filename but not its parent directory.
- Researched how to include directory names in the filtered output.
- Used `grep -E "1033|maybe"` to display both the matching file and the directory headings, allowing me to locate the correct file.
