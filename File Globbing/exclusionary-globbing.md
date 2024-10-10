# exclusionary-globbing
## Procedure
Followed the process as mentioned in pwn.college. Mistake: pwm instead of pwn
hacker@globbing~exclusionary-globbing:/challenge/files$ /ch*/r* [!pwm]*
Your expansion did not expand to the requested files (amazing beautiful
challenging delightful educational fantastic great happy incredible jovial kind
laughing magical optimistic queenly radiant splendid thrilling uplifting
victorious xenial youthful zesty).
Instead, it expanded to:
amazing beautiful challenging delightful educational fantastic great happy incredible jovial kind laughing nice optimistic queenly radiant splendid thrilling uplifting victorious xenial youthful zesty
hacker@globbing~exclusionary-globbing:/challenge/files$ /ch*/r* [!pwn]*
You got it! Here is your flag!
pwn.college{IO8C7jPDKsAwoWcAYOwl_xby_Qi.dZjM4QDLxgTN1czW}`
## Reference
pwn.college
