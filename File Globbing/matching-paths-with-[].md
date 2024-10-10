# matching-paths-with-[]
## Procedure
Followed the process as mentioned in pwn.college. Mistake: didn't used _ first time
## Bash
`hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file[bash]
Your expansion did not expand to the requested files (/challenge/files/file_b,
/challenge/files/file_a, /challenge/files/file_s, and /challenge/files/file_h).
Instead, it expanded to:
/challenge/files/file[bash]
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{oKMxXTCnYHBT_HN1k0H_XH7vzg9.dRjM4QDLxgTN1czW}`
## Reference
pwn.college
