# Bandit Level 9 → 10

## Commands Used

```bash
sort data.txt | grep -a ==
strings -d data.txt | grep ===
```

## What I Learned

- `strings` extracts human-readable sequences of characters from files containing binary data.
- `strings -d` scans data sections of files where applicable.
- `grep` filters output to find lines matching a specified pattern.
- Combining `strings` and `grep` allows me to extract and filter readable text from binary data.
- `sort` sorts lines rather than extracting human-readable strings.

## Difficulties

- Initially tried combining `sort` and `grep` to locate the password, but the output contained unreadable characters.
- Was unsure which string contained the password because the output was difficult to interpret.
- Discovered the `strings` command and combined it with `grep` to filter for multiple `=` characters.
- Successfully isolated the human-readable strings and identified the password.
