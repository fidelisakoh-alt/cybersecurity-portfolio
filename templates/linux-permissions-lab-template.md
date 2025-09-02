# Linux Permissions — Lab Notes

## Commands Practised
```bash
ls -l
chmod u+rwx,g+rx,o-r
chown user:group file.txt
chgrp group file.txt
usermod -aG group user
```
## Scenarios
- Create a file and set least-privilege permissions.
- Demonstrate setuid/setgid/sticky bit safely on a test directory.

## Takeaways
- How permission bits map to security controls.
- Common misconfigurations to watch for.
