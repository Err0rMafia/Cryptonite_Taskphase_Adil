
## making-directories
# Procedure
Followed the process as mentioned in pwn.college
# Bash
`hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ touch college
hacker@commands~making-directories:/tmp$ cd /challenge
hacker@commands~making-directories:/challenge$ ./run
Uh oh! /tmp/pwn/college does not exist. Please use the 'touch' command to
create it!
hacker@commands~making-directories:/challenge$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ cd /challenge
hacker@commands~making-directories:/challenge$ ./run
Success! Here is your flag:
pwn.college{gXfp2XItGHQYKxVatMHVdR6K9MB.dFzM4QDLxgTN1czW}`
# Reference
pwn.college
