# Bandit Level 17 → 18

## Commands Used

```bash
diff --help
ls -la
diff passwords.new passwords.old
cat passwords.new | grep "MATCHING_VALUE"
cat passwords.new | grep "OLD_VALUE"
```

## What I Learned

- `diff` compares files line by line and identifies differences.
- `42c42` indicates that line 42 differs between the two files.
- `<` represents a line from the first file supplied to `diff`.
- `>` represents a line from the second file.
- `grep` can verify whether a particular string exists in a file.

## Difficulties

- Used `diff --help` to investigate how to compare the two files.
- Identified the changed line using `diff`.
- Used `grep` to confirm which value appeared in `passwords.new` and which did not.
