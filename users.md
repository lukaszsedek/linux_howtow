# User managment
## Basic commands

|  What | command  |
|---|---|
|  `useradd <username>` | Create new user  |
|  `groupadd <groupname>` | Create new group  |
|  `usermod -g <group name> <username>` | Set  group as the account's primary group  |
|  `usermod -aG <group name> <username>`  | Set  group as the account's supplementary group |
|  `groupdel <groupname>` | Delete group  |
|  `passwd <user>`  | Set password for a user  |
|  `passwd -S <user>` | Check if account is locked  |
|  `passwd -u <user>` |  Unlock the account |
|  `usermod -U <user>`  |  Unlock the user's password |
|  `userdel -r <user>`  |  Delete a user. NOTICE! Without flag `-r` system does not delete a home folder |
|  `sudo su - <user>`  | evelate privilage as the user |

## Troubleshooting
1. Check if an account is locked

    grep <user> /etc/shadow 

If you see two exclamation marks `!!` the account is locked. But...

Check if the password for the account is locked as well

passwd -S <username>

To unlock the password:

    passwd -u user1

To unlock user account:
    usermod -U <username>

If a user has no password set, you cannot unlock a password. You need to set a new password and then unlock.

2. Check If a user is a sudoer
