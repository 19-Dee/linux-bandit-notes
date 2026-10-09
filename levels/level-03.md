# Bandit Level 2 → 3

## Commands Used

```bash
cat -- "--spaces in this filename--"
exit
ssh -p 2220 -l bandit2 bandit.labs.overthewire.org
```

## What I Learned

- Filenames containing spaces can be handled using quotation marks.
- `--` indicates the end of command-line options, allowing filenames beginning with `-` to be treated as arguments rather than options.
- Being logged into the wrong Linux account can result in permission errors when accessing files.

## Difficulties

- Initially encountered a permission error because I was still logged into Bandit 1.
- Realised I needed to connect to Bandit 2 before attempting the challenge.
- Initially struggled to read the file because its name contained spaces and began with dashes.
- Used the terminal's guidance to discover the `--` option and successfully retrieved the password.
