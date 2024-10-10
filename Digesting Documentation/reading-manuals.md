# reading-manuals
## Procedure
Followed the process as mentioned in pwn.college
## Bash
`hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                Challenge Commands                CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --sqlyop NUM
              print the flag if NUM is 242

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-
       luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                      May 2024                     CHALLENGE(1)
hacker@man~reading-manuals:~$ challenge --sqlyop 242
ssh-entrypoint: challenge: command not found
hacker@man~reading-manuals:~$ challenge --sqlyop NUM 242
ssh-entrypoint: challenge: command not found
hacker@man~reading-manuals:~$ /challenge/challenge --sqlyop 242
Correct usage! Your flag: pwn.college{s2AXIqlH42yXoU5pSjUa6S_P_Oi.dRTM4QDLxgTN1czW}`
## Reference
pwn.college
