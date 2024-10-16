# duplicating-piped-data-with-tee
## Procedure
Followed the instructions on pwn.college
## Bash
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee john |
 /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat john
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "YDIjFx2d"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret YDIjFx2d | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{YDIjFx2dwsHjPgsjUfTz09nk5u6.dFjM5QDLxgTN1czW}
```
## Resources
pwn.college
