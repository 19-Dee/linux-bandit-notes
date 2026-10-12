# Bandit Level 22 → 23

## Commands Used

```bash
cd /etc/cron.d/
ls
cat cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh

# Execute the script to understand its behaviour
/usr/bin/cronjob_bandit23.sh

# Examine how the filename is generated
echo I am user bandit22 | md5sum
echo I am user bandit23 | md5sum | cut -d ' ' -f 1

# Read the password file created by the scheduled job
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```

## What I Learned

- Cron jobs can execute scripts under a different user account from my current session.
- `$(command)` performs command substitution, replacing the expression with the command's output.
- `whoami` returns the effective username of the process running the command.
- `md5sum` calculates an MD5 hash of the input.
- `cut -d ' ' -f 1` extracts the first field using a space as the delimiter.
- Hashing can be used to generate predictable filenames, not just to verify data integrity.
- Running the same script under different user accounts can produce different results.

## Difficulties

- Initially attempted to access variables from the script directly, without understanding that they weren't defined in my current shell.
- Executed the script as `bandit22`, which generated a filename containing the current user's password rather than the next password.
- Investigated the individual commands used to generate the filename, including `echo`, `md5sum` and `cut`.
- Realised that cron executes the script as `bandit23`, meaning `whoami` produces a different username.
- Recreated the filename using `bandit23` and successfully retrieved the next password.
- Attempted to write to the Bandit 23 password file but received a permission error, confirming that I couldn't overwrite it as `bandit22`.
