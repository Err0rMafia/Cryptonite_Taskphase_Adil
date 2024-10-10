# redirecting-input
## Procedure
Followed the process as mentioned in pwn.college.
## Bash
`hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run > PWN
hacker@piping~redirecting-input:~$ cat PWN
You have not redirected anything to my standard input. Please do so, using '<'.
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{gyxClgp5ia87wqZ7XRBRLywAkV_.dBzN1QDLxgTN1czW}
`
## Reference
pwn.college
