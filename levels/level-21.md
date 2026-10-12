# Bandit Level 21 → 22

## Commands Used

```bash
cd /etc/cron.d/
ls
cat cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

## What I Learned

- `cron` is a Linux service that schedules commands and scripts to run automatically.
- `/etc/cron.d/` contains system cron job configurations.
- `* * * * *` schedules a job to execute every minute.
- Cron jobs can run under a specified user account, in this case `bandit22`.
- `&> /dev/null` discards both standard output and standard error.
- `chmod 644` gives the file owner read/write permissions and everyone else read-only permissions.
- The `>` operator redirects command output into a file, overwriting its existing contents.

## Difficulties

- Initially tried running `cron` and modifying crontabs, but encountered permission errors.
- Investigated cron documentation to understand how scheduled jobs work.
- Located `cronjob_bandit22` and identified the shell script being executed.
- Discovered that the script copies the Bandit 22 password into a file under `/tmp` and makes it readable.
- Read the temporary file and successfully retrieved the password for Bandit 22.
