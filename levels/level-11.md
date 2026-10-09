# Bandit Level 10 → 11

## Commands Used

```bash
cat data.txt
base64 -d <encoded-string>
base64 --help
base64 -d data.txt
```

## What I Learned

- Base64 is an encoding scheme that represents binary data using printable characters.
- Base64 encoding is not encryption.
- `base64 -d` decodes Base64-encoded data.
- The `base64` command accepts a filename as an argument and reads its contents.
- `--help` displays a command's usage instructions and available options.

## Difficulties

- Initially tried passing the encoded string directly to `base64 -d`, which resulted in a file-not-found error.
- Used `base64 --help` to investigate the correct syntax.
- Realised I needed to pass the filename rather than the encoded contents.
- Successfully decoded `data.txt` and retrieved the password.
