# Swap Memory

**Pilfering Credentials From Swap Memory**

Staying along the lines of directly dumpling credentials from memory, we can also dump sensitive information from the swap file. As everything is a "file" in Linux, so is swap space, and we can use that to our advantage using built-in tools.

One caveat to this technique is that this has to be done as the root account and may also be prone to false-positives as it's difficult to ascertain exactly where in swap memory sensitive information will be temporarily stored. The partition or "file" defined as the swap file can be found with the following commands:

swapon -s

We can obtain the exact same information by issuing:

cat /proc/swaps

The process from here is straight. We can use `strings` command against the `/dev/sdaX` partition while we use `grep` for strings we're looking for:

strings /dev/sda2 | grep "password="

strings /dev/sda5 | grep "\&password="

This shellscript has also been written to automate searching for common sensitive strings within the swap file:

\{% embed url="[https://github.com/sevagas/swap\_digger](https://github.com/sevagas/swap\_digger)" %\}
