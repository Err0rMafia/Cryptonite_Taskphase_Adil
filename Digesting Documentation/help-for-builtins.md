# help-for-builtins
## Procedure
Followed the process as mentioned in pwn.college
## Bash
`hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "03MwaHHw".
hacker@man~help-for-builtins:~$ challenge --secret 03MwaHHw
Correct! Here is your flag!
pwn.college{03MwaHHwc7vxu3YbwoYvLHBVJuZ.dRTM5QDLxgTN1czW}
`
## Reference
pwn.college
