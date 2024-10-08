## listing-files
# Procedure
Followed the process as mentioned in pwn.college
# Bash
`hacker@commands~listing-files:~$ ls /challenge
26929-renamed-run-11892  DESCRIPTION.md
hacker@commands~listing-files:~$ cat /challenge/26929-renamed-run-11892
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:~$ cat /flag
cat: /flag: Permission denied
hacker@commands~listing-files:~$ cat /challenge/description.md
cat: /challenge/description.md: No such file or directory
hacker@commands~listing-files:~$ cat /challenge/DESCRIPTION.md
So far, we've told you which files to interact with.
But directories can have lots of files (and other directories) inside them, and we won't always be here to tell you their names.
You'll need to learn to **l**i**s**t their contents using the `ls` command!

`ls` will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided.
Observe:

```console
hacker@dojo:~$ ls /challenge
run
hacker@dojo:~$ ls
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$ ls /home/hacker
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$
```

In this challenge, we've named `/challenge/run` with some random name!
List the files in `/challenge` to find it.
hacker@commands~listing-files:~$ cd /challenge
hacker@commands~listing-files:/challenge$ ./26929-renamed-run-11892
Yahaha, you found me! Here is your flag:
pwn.college{8z5WdCrKBFKzHwaIfFdHDv3WxrV.dhjM4QDLxgTN1czW}`
# Reference
pwn.college
