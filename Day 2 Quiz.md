## Day 2 --- Linux Basics & Filesystem

1. What is Linux, and what is the role of the shell?
2. Explain the difference between an absolute path and a relative path.
3. What are the purposes of `/etc`, `/var`, `/home`, `/tmp`, and
    `/opt`?
4. Write commands to:
    -   Print your current directory.
    -   List files, including hidden files, with details.
    -   Create a directory named `devops-lab`.
    -   Create an empty file named `notes.txt`.
5. Explain the difference between `cp` and `mv`.
6. What do `>` and `>>` do when used with shell output redirection?
7. Write a command that displays the last 20 lines of `app.log`.
8. Write a command that follows new log entries in `app.log`
    continuously.
9. Use `grep` to find lines containing `ERROR` in `app.log`.
10. Use `find` to locate all files named `config.yml` under the current
    directory.
11. What information do `df -h`, `free -h`, and `uptime` provide?
12. What is the difference between `head` and `tail`?

------------------------------------------------------------------------

## Answer Key

1. Linux is an operating-system kernel commonly used with GNU and other
    tools; a shell interprets commands and runs programs.
2. Absolute paths start from `/`; relative paths are interpreted from
    the current directory.
3. `/etc` configuration; `/var` changing data/logs; `/home` user homes;
    `/tmp` temporary files; `/opt` optional/add-on software.
4. `pwd`; `ls -la`; `mkdir devops-lab`; `touch notes.txt`.
5. `cp` copies; `mv` moves or renames.
6. `>` overwrites/creates; `>>` appends/creates.
7. `tail -n 20 app.log`.
8. `tail -f app.log` (or `tail -F app.log` for rotation-aware
    following).
9. `grep "ERROR" app.log`.
10. `find . -type f -name "config.yml"`.
11. `df -h` disk usage; `free -h` memory/swap; `uptime` running
    duration/load averages.
12. `head` shows beginning; `tail` shows end.