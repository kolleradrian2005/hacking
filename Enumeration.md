# Enumeration

## Nmap

```console
$ nmap -T4 -A <IP>
```

## Gobuster
Useful if port 80/443 is open
```console
$ gobuster dir -u <URL> -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -t 100
```

## DNS
Useful if port 53 is open
```console
$ nslookup
> SERVER <IP>
> <IP>
```

## Dig
Useful if the method above found something useful
```console
$ dig axfr <HOST> @<IP>
```

## /etc/hosts
When domain found with the either of 2 methods above, make host resolve deez
```console
$ sudo mousepad /etc/hosts
```
The file should look like this
```
127.0.0.1   localhost
127.0.0.1   thebeast
<IP>        <domain1> <domain2> ... # Add this line
...
```
