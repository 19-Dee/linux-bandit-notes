# Bandit Level 8 → 9

## Commands Used

```bash
sort -d data.txt | uniq -c
```

## What I Learned

- `sort` sorts lines of text.
- `sort -d` uses dictionary-order comparisons.
- `uniq -c` counts occurrences of adjacent identical lines.
- Sorting before using `uniq` groups duplicate lines together.
- `uniq -u` can display only lines that occur exactly once, avoiding manual inspection of the counts.

## Difficulties

- Experimented with different commands before finding a working solution.
- Used `sort` and `uniq -c` to identify how many times each line occurred.
- Manually located the line with a count of `1`.
- Realised that manually searching the output would become inefficient with much larger files.
