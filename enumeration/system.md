# System

| Command               | Description and/or Reason                                     |
| --------------------- | ------------------------------------------------------------- |
| uname -a              | Prints the kernel version, arch, sometimes distro             |
| ps aux                | List all running processes                                    |
| top -n 1 -d           | Print process, 1 is a number of lines                         |
| id                    | Your current username, groups                                 |
| arch, uname -m        | Kernel processor architecture                                 |
| w                     | who is connected, uptime and load avg                         |
| who -a                | uptime, runlevel, tty, proceses etc.                          |
| gcc -v                | Returns the version of GCC.                                   |
| mysql --version       | Returns the version of MySQL.                                 |
| perl -v               | Returns the version of Perl.                                  |
| ruby -v               | Returns the version of Ruby.                                  |
| python --version      | Returns the version of Python.                                |
| df -k                 | mounted fs, size, % use, dev and mount point                  |
| mount                 | mounted fs                                                    |
| last -a               | Last users logged on                                          |
| lastcomm              |                                                               |
| lastlog               |                                                               |
| lastlogin (BSD)       |                                                               |
| getenforce            | Get the status of SELinux (Enforcing, Permissive or Disabled) |
| dmesg                 | Informations from the last system boot                        |
| lspci                 | prints all PCI buses and devices                              |
| lsusb                 | prints all USB buses and devices                              |
| lscpu                 | prints CPU information                                        |
| lshw                  | list hardware information                                     |
| ex                    |                                                               |
| cat /proc/cpuinfo     |                                                               |
| cat /proc/meminfo     |                                                               |
| du -h --max-depth=1 / | note: can cause heavy disk i/o                                |
| which nmap            | locate a command (ie nmap or nc)                              |
| locate bin/nmap       |                                                               |
| locate bin/nc         |                                                               |
| jps -l                |                                                               |
| java -version         | Returns the version of Java.                                  |
