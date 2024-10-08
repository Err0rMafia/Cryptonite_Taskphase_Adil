## Home_Sweet_Home
# Procedure
I couldn't understand what is written on pwn.college. I tried some hit and trial then learnt about these from Google, Chatgpt etc.
# Bash
`hacker@paths~home-sweet-home:~$ cd ~/./run
ssh-entrypoint: cd: /home/hacker/./run: No such file or directory
hacker@paths~home-sweet-home:~$ cd ~/../run
ssh-entrypoint: cd: /home/hacker/../run: No such file or directory
hacker@paths~home-sweet-home:~$ cd ~/challenge/run
ssh-entrypoint: cd: /home/hacker/challenge/run: No such file or directory
hacker@paths~home-sweet-home:~$ ~
ssh-entrypoint: /home/hacker: Is a directory
hacker@paths~home-sweet-home:~$ ~/c
ssh-entrypoint: /home/hacker/c: No such file or directory
hacker@paths~home-sweet-home:~$ /challenge/run ~/c
Writing the file to /home/hacker/c!
... and reading it back to you:
pwn.college{4oUw25e3xbVqOgJ9BoSXVe5gPs5.dNzM4QDLxgTN1czW}
hacker@paths~home-sweet-home:~$ /challenge/run ~/isthisright
The argument you provided must not have been longer than 3 characters (it's
currently 13 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ~/q
Writing the file to /home/hacker/q!
... and reading it back to you:
pwn.college{4oUw25e3xbVqOgJ9BoSXVe5gPs5.dNzM4QDLxgTN1czW}`
# Reference
Google.com
pwn.college
youtube.com
chat.openai.com
