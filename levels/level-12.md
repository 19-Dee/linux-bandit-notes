# Bandit Level 11 → 12

## Commands Used

```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m' <<< "encoded text"
```

## What I Learned

- ROT13 is a substitution cipher that rotates letters 13 positions through the alphabet.
- `tr` translates characters from one set into another.
- `A-Za-z` represents uppercase and lowercase letters.
- `<<<` is a Bash here-string that passes text to a command through standard input.
- ROT13 is not a secure encryption method.

## Difficulties

- Was unfamiliar with ROT13 and didn't know how to decode the contents of `data.txt`.
- Consulted Wikipedia to understand the ROT13 transformation and identify a suitable command.
- Used `tr` to decode the text and retrieve the password.
