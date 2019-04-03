## What is on the end of this SSH connection?
Sometimes you have access to command line interface of your server. To find out what kind of system is there, you can try this:
```bash
# to get information about linux distribution
cat /etc/*-release

# to get information about linux kernel
uname -a

# to get actual system user:
whoami
```
