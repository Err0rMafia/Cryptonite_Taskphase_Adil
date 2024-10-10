# helpful-programs
## Procedure
Followed the process as mentioned in pwn.college. Mistake: Didn't read the whole help page
## Bash
`hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h]
                                            [--fortune]
                                            [-v]
                                            [-g GIVE_THE_FLAG]
                                            [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct
                        value
  -p, --print-value     print the value that will cause the
                        -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -g
usage: a challenge to make you ask for help
       [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: expected one argument
hacker@man~helpful-programs:~$ /challenge/challenge -g GI
VE_THE_FLAG
usage: a challenge to make you ask for help
       [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge --give-the-flag GIVE_THE_FLAG
usage: a challenge to make you ask for help
       [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge --give-the-flag
usage: a challenge to make you ask for help
       [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: expected one argument
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help
       [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the
                        correct value
  -p, --print-value     print the value that will cause
                        the -g option to give you the
                        flag
hacker@man~helpful-programs:~$ man challenge
No manual entry for challenge
hacker@man~helpful-programs:~$ /challenge/challenge --help -g
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge   -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG,'
hacker@man~helpful-programs:~$ /challenge/challenge   -g 777
Incorrect number! Look at the program help.
hacker@man~helpful-programs:~$ /challenge/challenge   -p
The secret value is: 80
hacker@man~helpful-programs:~$ /challenge/challenge   -g 80
Correct usage! Your flag: pwn.college{QNAltMbUjc0qOpCK8Twwd00z-jV.ddjM4QDLxgTN1czW}`
## Reference
pwn.college
