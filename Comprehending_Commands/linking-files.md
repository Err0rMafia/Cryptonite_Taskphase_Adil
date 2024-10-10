# linking-files
## Procedure
Followed the process as mentioned in pwn.college. understood the concept using hit and trail.
## Bash
`hacker@commands~linking-files:~$ cat /challenge/catflag
#!/opt/pwn.college/bash

fold -s <<< "About to read out the /home/hacker/not-the-flag file!"
cat /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /home/hacker/flag /challenge/catflag
ln: failed to create symbolic link '/challenge/catflag': File exists
hacker@commands~linking-files:~$ ln -s /home/hacker/flag /challenge/flagg
ln: failed to create symbolic link '/challenge/flagg': Permission denied
hacker@commands~linking-files:~$ ln -s /home/hacker/not-the-flag /challenge/catflag
ln: failed to create symbolic link '/challenge/catflag': File exists
hacker@commands~linking-files:~$ ln -s /flag /challange/fleg
ln: failed to create symbolic link '/challange/fleg': No such file or directory
hacker@commands~linking-files:~$ pwd
/home/hacker
hacker@commands~linking-files:~$ touch fleg
hacker@commands~linking-files:~$ ln -s /flag /challange/fleg
ln: failed to create symbolic link '/challange/fleg': No such file or directory
hacker@commands~linking-files:~$ ln -s /flag /fleg
ln: failed to create symbolic link '/fleg': Permission denied
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{0hCMq8M49OqV6EelyDoK76Mak64.dlTM1UDLxgTN1czW}`
## Reference
pwn.college
