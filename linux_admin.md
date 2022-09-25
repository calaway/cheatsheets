# Linux Admin Cheatsheet

### Power Off
```bash
# Shutdown
sudo shutdown -h now

# Reboot
sudo reboot
```

### Users
```bash
# See all users
cat /etc/passwd

# See all non-system users
cat /etc/passwd | grep /bin/bash

# Switch users
sudo su - <username>
```

### Disk
```bash
# See disk space used (disk free) on all mounted partitions in human readable format:
df -h

# Show block devices found on the machine (mounted or not) and any corresponding partitions it recognizes
lsblk

# List the human-readable sizes of a directory and any subdirectories, up to N levels deep
sudo du -ah -d 1 /home

# Or for a specific file system:
df -h /opt/finicity/
```

### Processes
```bash
# Kill process by ID:
kill -9 1234
```
