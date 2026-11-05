# Day 2 – Linux Fundamentals & File System

## 1. Linux Fundamentals

Linux is an open-source operating system kernel.

### Linux Architecture
- Hardware
- Kernel
- Shell
- Applications

### Shell
A shell provides an interface for executing Linux commands.

Bash is the primary shell used in this training.

```bash
echo $SHELL
```

## 2. Linux File System

Linux uses a hierarchical filesystem starting from `/`.

| Directory | Purpose |
|---|---|
| `/` | Root filesystem |
| `/home` | User directories |
| `/root` | Root user's home |
| `/etc` | Configuration |
| `/var` | Logs and variable data |
| `/tmp` | Temporary files |
| `/usr` | Programs and libraries |
| `/opt` | Optional software |
| `/dev` | Device files |
| `/proc` | Process/kernel information |
| `/mnt` | Mount points |
| `/boot` | Boot files |

## 3. Paths

- Absolute path: starts with `/`.
- Relative path: starts from current directory.
- `~`: user's home directory.
- `.`: current directory.
- `..`: parent directory.

## 4. Navigation Commands

```bash
pwd
ls
ls -l
ls -a
ls -la
cd /
cd ~
cd ..
cd -
```

## 5. File and Directory Management

```bash
mkdir devops
mkdir -p devops/linux/day02
touch notes.txt
cp notes.txt backup.txt
cp -r directory backup-directory
mv notes.txt linux-notes.txt
rm linux-notes.txt
rm -r directory
```

## 6. File Viewing

```bash
cat notes.txt
less notes.txt
head notes.txt
head -n 5 notes.txt
tail notes.txt
tail -n 20 notes.txt
tail -f application.log
```

## 7. File Content Manipulation

Overwrite:

```bash
echo "Linux learning" > notes.txt
```

Append:

```bash
echo "Day 2" >> notes.txt
```

## 8. Linux Permissions

Permissions:
- Read = 4
- Write = 2
- Execute = 1

Categories:
- Owner
- Group
- Others

Examples:

```bash
chmod 755 script.sh
chmod 644 notes.txt
chmod +x script.sh
chmod u+x script.sh
chmod g+w notes.txt
chmod o-r notes.txt
```

Change ownership:

```bash
sudo chown ubuntu notes.txt
sudo chown ubuntu:ubuntu notes.txt
```

## 9. File Searching

```bash
find ~ -name "notes.txt"
find ~ -type f
find ~ -type d
find /var/log -name "*.log"
```

Search text:

```bash
grep "error" notes.txt
grep -i "error" notes.txt
grep -n "error" notes.txt
grep -r "error" /var/log
```

## 10. System Information

```bash
date
whoami
hostname
uname -a
df -h
free -h
uptime
top
ps aux
history
```

## 11. Practical Assignment

Create:

```text
~/devops-training/day02/
├── scripts/
├── logs/
├── configs/
└── backup/
```

Create files:

```bash
touch scripts/deploy.sh
touch logs/application.log
touch configs/app.conf
```

Practice:
- Write and append content.
- Copy and rename files.
- Apply permissions.
- Search for files.
- Search log errors.
- Monitor logs using tail -f.

## 12. Interview Questions

1. What is Linux?
2. What is a kernel?
3. What is a shell?
4. Explain Linux filesystem hierarchy.
5. Absolute path vs relative path?
6. What is the difference between > and >>?
7. Explain chmod 755.
8. What does chmod +x do?
9. What is the difference between cp and mv?
10. How do you monitor logs?
11. How do you search for errors in logs?
12. What is the purpose of /etc and /var/log?

## 13. Day 2 Completion Checklist

- [ ] Understand Linux architecture.
- [ ] Understand filesystem hierarchy.
- [ ] Navigate using pwd, ls, and cd.
- [ ] Create, copy, move, and delete files.
- [ ] Read files using cat, less, head, and tail.
- [ ] Understand permissions.
- [ ] Practice chmod.
- [ ] Search using find and grep.
- [ ] Practice log troubleshooting.
- [ ] Complete Day 2 quiz.

---