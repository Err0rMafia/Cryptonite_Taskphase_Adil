## hidden-files
# Procedure
Followed the process as mentioned in pwn.college
# Bash
`hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.                     bin        etc    lib64   nix   run   tmp
..                    boot       home   libx32  opt   sbin  usr
.dockerenv            challenge  lib    media   proc  srv   var
.flag-51172185526603  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ .flag-51172185526603
ssh-entrypoint: .flag-51172185526603: command not found
hacker@commands~hidden-files:/$ /.flag-51172185526603
ssh-entrypoint: /.flag-51172185526603: Permission denied
hacker@commands~hidden-files:/$ cat .flag-51172185526603
pwn.college{cBwSPVGP8qLcJIYlUctD5ZZKPM0.dBTN4QDLxgTN1czW}`
# Reference
pwn.college
