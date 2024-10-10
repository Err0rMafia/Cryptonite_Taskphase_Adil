# mixing-globs
## Procedure
Followed the process as mentioned in pwn.college. Mistake: tried doing it different then expected. reaslised my mistake when one of the hit and trial gave a key.
## Bash
`hacker@globbing~mixing-globs:~$ cd /ch*/fi*
hacker@globbing~mixing-globs:/challenge/files$ ch*gin
ssh-entrypoint: ch*gin: command not found
hacker@globbing~mixing-globs:/challenge/files$ ././*ing
hacker@globbing~mixing-globs:/challenge/files$ ././*nal
hacker@globbing~mixing-globs:/challenge/files$ ././*ing
hacker@globbing~mixing-globs:/challenge/files$ ~cd ~
ssh-entrypoint: ~cd: command not found
hacker@globbing~mixing-globs:/challenge/files$ cd ~
hacker@globbing~mixing-globs:~$ cd /ch*/fi*
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run
Error: you did not use a square bracket glob...
hacker@globbing~mixing-globs:/challenge/files$ ././*ning
hacker@globbing~mixing-globs:/challenge/files$ ././*ging
hacker@globbing~mixing-globs:/challenge/files$ ././*nal
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [pec]*
You got it! Here is your flag!
pwn.college{M_S0yUv-nDKk1uhvTMwTsEUlC_C.dVjM4QDLxgTN1czW}`
## Reference
pwn.college
