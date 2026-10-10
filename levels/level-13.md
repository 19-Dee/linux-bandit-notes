# Bandit Level 12 → 13

## Commands Used

```bash
mktemp -d
cp ~/data.txt .
xxd -r data.txt > data1.bin
file data1.bin

gzip -dc data1.bin > data2.bin
bzip2 -dc data2.bin > decompressed.bin
tar -xf data4.bin
file data5.bin
tar -xf data5.bin
file data6.bin
bzip2 -dc data6.bin > data8.bin
file data8.bin
tar -xf data8.bin
gzip -dc data8.bin > data9.bin
cat data9.bin
```

## What I Learned

- `mktemp -d` creates a temporary directory for working with files.
- `cp` copies files into another location.
- `xxd -r` reverses a hexadecimal dump into its original binary data.
- `file` identifies the format of a file by examining its contents.
- `gzip -dc` and `bzip2 -dc` decompress data and send the result to stdout.
- `tar -xf` extracts files from a tar archive.
- Compression reduces data size, whereas archiving packages files together.
- Repeatedly checking file types helps determine which decompression or extraction command to use.

## Difficulties

- The original file had been repeatedly compressed using different formats.
- Had to identify each resulting file type before deciding which command to use.
- Initially struggled with `tar` syntax and received several errors before successfully using `tar -xf`.
- Used `tar --help` to investigate the available options.
- Initially tried `bzip` before correcting the command to `bzip2`.
- Occasionally used `cat` on binary files, producing unreadable output.
- Repeated the identification and decompression process until reaching the file containing the password.
