# redirecting-errors
## Procedure
Followed the process as mentioned in pwn.college.
## Bash
`hacker@piping~redirecting-errors:~$ /ch*/r* > myflag 2> instructions
hacker@piping~redirecting-errors:~$ myflag
ssh-entrypoint: myflag: command not found
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{M0cDaVtiLlW4RJU1mkN5NwTnkzR.ddjN1QDLxgTN1czW}
`
## Reference
pwn.college
