1. Explain what a Linux user, group, and file owner are.
2. What do the permission symbols `r`, `w`, and `x` mean for files and
    directories?
3. Interpret the permission mode `rwxr-xr-x` and convert it to numeric
    form.
4. What does `chmod 640 file.txt` mean?
5. Write commands to:
    -   Create a group named `developers`.
    -   Add user `alice` to `developers` without removing her other
        supplementary groups.
    -   Display the groups of the current user.
6. Explain the difference between `chown` and `chgrp`.
7. What is `sudo`, and why should it be used carefully?
8. A user can read a file but cannot modify it. List two commands or
    checks you would use to investigate and explain what you would
    inspect.

------------------------------------------------------------------------

## Answer Key

1. A user is an account identity; a group collects users for shared
    access; owner is the account owning a filesystem object.
2. `r` read; `w` write; `x` execute (for directories, search/traverse).
3. Owner read/write/execute; group read/execute; others read/execute.
    Numeric: `755`.
4. Owner read/write; group read; others no permissions.
5. `sudo groupadd developers`; `sudo usermod -aG developers alice`;
    `groups` (or `id`).
6. `chown` changes owner (and optionally group); `chgrp` changes group
    ownership.
7. `sudo` runs an approved command with elevated privileges; use least
    privilege and verify commands before running.
8. Check `ls -l file.txt` and `id`/`groups`; inspect owner/group/mode
    and directory permissions (including parent directories). Use
    `namei -l /path/to/file` where available.