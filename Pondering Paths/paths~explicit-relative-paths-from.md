## paths~explicit-relative-paths-from.md
# Procedure
Followed the process as mentioned in pwn.college
# Bash
`hacker@paths~explicit-relative-paths-from-:~$ ./challenge/run
ssh-entrypoint: ./challenge/run: No such file or directory
hacker@paths~explicit-relative-paths-from-:~$ pwd
/home/hacker
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{oRLJ_puwYQI5GwP3OB3xGmqKyGB.dBTN1QDLxgTN1czW}`
# Reference
pwn.college
