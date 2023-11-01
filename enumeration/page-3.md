# Page 3

id # current user information

uname -a # kernel version

grep $USER /etc/passwd # Current User Information from /etc/passwd

lastlog # most recent logins

w # who is currently logged onto the system

last # last logged on users

\# all users including UID and GID information

for user in $(cat /etc/passwd | cut -f1 -d":"); do id $user;done

\# List all UID 0 (root) accounts

cat /etc/passwd | cut -f1,3,4 -d":" | grep "0:0" | cut 0f1 0d":" | awk '{print $1}'

cat /etc/passwd # Read passwd file

cat /etc/shadow # check readibility of the shadow file

sudo -l # what can we sudo without a password

cat /etc/sudoers # can we read /etc/sudoers file?

cat /root/.bash\_history # can we read roots .bash\_history files?

cat /etc/issue # OS

cat /etc/\*-release # OS

\# can we sudo known binaries that allow breaking out into a shell?

sudo -l | grep vim

sudo -l | grep nmap

sudo -l | grep vi

ls -als /root/ # can we list root's home directory?

echo $PATH # current $PATH env variable

cat /etc/crontab && ls -als /etc/cron\* # list all cron jobs

find /etc/cron\* -type f -perm -o+w -exec ls -l {} \\; # find world-writeable cron jobs

ps auxwww # list running processes

ps -u root # list all processes running as root

ps -u $USER # list all processes running as current user

find / -perm -4000 -type f 2>/dev/null # Find SUID files

find / -uid 0 -perm -4000 -type f 2>/dev/null # Find SUID files owned by root

find / -perm -2000 0type -f 2>/dev/null # Find GUID files

find -perm -2 -type f 2>/dev/null # Find wolrd-writable files

ls -al /etc/\*.conf # list all conf files in /etc/

grep pass\* /etc/\*.conf # Find conf files that contain the string "pass\*"

lsof -n # list open files

dpkg -l # list installed packages (debian)

\# Common software versions

sudo -V

httpd -v

apache2 -v

mysql -V

sendmail -d0.1

\# print process binaries/paths and permissions

ps aux | awk '{print $11}' | xargs -r ls -la 2>/dev/null |awk '!x\[$0]++'
