## touching-files
# Procedure
Followed the process as mentioned in pwn.college
# Bash
`heartlesscrypto@HM_Laptop2:~$ ssh -i ./key hacker@dojo.pwn.college

Connected!
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwm  tmp.XvrUsDZh8M
hacker@commands~touching-files:/tmp$ cd ~/challenge/run
ssh-entrypoint: cd: /home/hacker/challenge/run: No such file or directory
hacker@commands~touching-files:/tmp$ cat /challenge/run
#!/opt/pwn.college/bash

if [ ! -f /tmp/pwn ]
then
        fold -s <<< "Uh oh! /tmp/pwn does not exist. Please use the 'touch' command to create it!"
        exit 1
fi

if [ ! -f /tmp/college ]
then
        fold -s <<< "Uh oh! /tmp/college does not exist. Please use the 'touch' command to create it!"
        exit 2
fi

echo "Success! Here is your flag:"
cat /flag
hacker@commands~touching-files:/tmp$ cd /challenge
hacker@commands~touching-files:/challenge$ ./run
Uh oh! /tmp/pwn does not exist. Please use the 'touch' command to create it!
hacker@commands~touching-files:/challenge$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ cd /challenge
hacker@commands~touching-files:/challenge$ run
ssh-entrypoint: run: command not found
hacker@commands~touching-files:/challenge$ ./run
Success! Here is your flag:
pwn.college{cRZvESmgGIyUuXdhNdYXctQCt7c.dBzM4QDLxgTN1czW}`
# Reference
pwn.college
