# User Accounts

##

| Command                 | Description and/or Reason                                      |
| ----------------------- | -------------------------------------------------------------- |
| cat /etc/passwd         | local accounts                                                 |
| cat /etc/shadow         | password hashes on Linux                                       |
| /etc/security/passwd    | password hashes on AIX                                         |
| cat /etc/group          | groups (or /etc/gshadow)                                       |
| getent passwd           | should dump all local, LDAP, NIS, whatever the system is using |
| getent group            | same for groups                                                |
| pdbedit -L -w           | Samba’s own database                                           |
| pdbedit -L -v           | ​                                                              |
| cat /etc/aliases        | mail aliases                                                   |
| find /etc -name aliases | ​                                                              |
| getent aliases          | ​                                                              |
| ypcat passwd            | displays NIS password file                                     |

**Obtain user's information**

* ls -alh /home/\*/
* ls -alh /home/\*/.ssh/
* cat /home/\*/.ssh/authorized\_keys
* cat /home/\*/.ssh/known\_hosts
* cat /home/\*/._hist_ # you can learn a lot from this
* find /home/\*/.vnc /home/\*/.subversion -type f
* grep ^ssh /home/\*/._hist_
* grep ^telnet /home/\*/._hist_
* grep ^mysql /home/\*/._hist_
* cat /home/\*/.viminfo
* sudo -l # if sudoers is not. readable, this sometimes works per user
* crontab -l
* cat /home/\*/.mysql\_history
* sudo -p (allows the user to define what the password prompt will be, useful for fun customization with aliases or shell scripts)

**Credentials**

| File/Folder                  | Description and/or Reason    |
| ---------------------------- | ---------------------------- |
| /home/\*/.ssh/id\*           | SSH keys, often passwordless |
| /tmp/krb5cc\_\*              | Kerberos tickets             |
| /tmp/krb5.keytab             | Kerberos tickets             |
| /home/\*/.gnupg/secring.gpgs | PGP keys                     |
