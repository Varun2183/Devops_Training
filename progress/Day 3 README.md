# Day 3 – Linux Users, Groups, Permissions & Ownership

## 1. Linux Users

Linux supports multiple users.

Types:
- Root user
- Regular user
- System user

Commands:

```bash
whoami
id
id root
```

## 2. User Management

Create user:

```bash
sudo useradd -m -s /bin/bash devuser
```

Set password:

```bash
sudo passwd devuser
```

Verify:

```bash
id devuser
getent passwd devuser
```

Delete user:

```bash
sudo userdel devuser
sudo userdel -r devuser
```

Modify user:

```bash
sudo usermod -aG developers devuser
sudo usermod -s /bin/bash devuser
```

## 3. Linux Groups

Create group:

```bash
sudo groupadd developers
```

Add users:

```bash
sudo usermod -aG developers devuser
```

Verify:

```bash
groups devuser
getent group developers
```

Delete group:

```bash
sudo groupdel developers
```

## 4. Ownership

Change owner:

```bash
sudo chown devuser app.conf
```

Change owner and group:

```bash
sudo chown devuser:developers app.conf
```

Recursive ownership:

```bash
sudo chown -R devuser:developers project/
```

Change group:

```bash
sudo chgrp developers app.conf
```

## 5. Linux Permissions

Permissions:
- Read = 4
- Write = 2
- Execute = 1

Examples:

```bash
chmod 755 deploy.sh
chmod 644 app.conf
chmod 700 private.sh
chmod 600 secrets.txt
chmod +x deploy.sh
chmod u+x deploy.sh
chmod g+w app.conf
chmod o-r app.conf
```

### Permission reference

| Mode | Meaning |
|---|---|
| 777 | Everyone rwx |
| 755 | Owner rwx, group/others rx |
| 700 | Owner rwx only |
| 644 | Owner rw, group/others r |
| 600 | Owner rw only |

Avoid unnecessary 777 permissions.

## 6. sudo

Execute privileged command:

```bash
sudo apt update
```

Open root shell:

```bash
sudo -i
```

Exit:

```bash
exit
```

Add user to sudo group:

```bash
sudo usermod -aG sudo devuser
```

## 7. Permission Troubleshooting

Check permissions:

```bash
ls -l deploy.sh
stat deploy.sh
```

Check user:

```bash
whoami
id
groups
```

Fix execute permission:

```bash
chmod +x deploy.sh
```

Fix ownership:

```bash
sudo chown devuser:developers app.conf
```

## 8. Practical Assignment

- Create two Linux users.
- Create a developers group.
- Add both users to developers.
- Create `/opt/company/project`.
- Assign group ownership.
- Set shared directory permissions.
- Create a deployment script.
- Test execution permissions.
- Troubleshoot Permission denied.
- Verify users, groups, and ownership.

## 9. Interview Topics

1. What is UID and GID?
2. What is root?
3. Explain Linux user management.
4. Explain group management.
5. Explain chmod 755 and 644.
6. Explain chown and chgrp.
7. What is sudo?
8. Why avoid chmod 777?
9. Explain setgid on a directory.
10. How do you troubleshoot Permission denied?

## 10. Day 3 Completion Checklist

- [ ] Understand users and groups.
- [ ] Create Linux users.
- [ ] Create Linux groups.
- [ ] Assign users to groups.
- [ ] Understand ownership.
- [ ] Practice chmod.
- [ ] Practice chown.
- [ ] Understand sudo.
- [ ] Troubleshoot permission errors.
- [ ] Complete Linux administration lab.
- [ ] Complete assessment.

---