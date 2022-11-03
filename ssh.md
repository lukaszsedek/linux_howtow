# SSH

''
*[cloud_user@server1 ~]$ ssh-keygen*
Generating public/private rsa key pair.
Enter file in which to save the key (/home/cloud_user/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/cloud_user/.ssh/id_rsa.
Your public key has been saved in /home/cloud_user/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:Rao4iwc6+Yk/ZjyWEVicL7LmVO6OepWu3DQcxMGxRQw cloud_user@server1
The key's randomart image is:
+---[RSA 2048]----+
| . oE=o   .      |
|  +..+.  o       |
| o .+   . .      |
|o oo.. . .       |
| o+o+.. S        |
|.=.=o+           |
|B.o=*            |
| *@*..           |
|+BB=.            |
+----[SHA256]-----+

*[cloud_user@server1 ~]$ ssh-copy-id 10.0.1.208*
/usr/bin/ssh-copy-id: INFO: Source of key(s) to be installed: "/home/cloud_user/.ssh/id_rsa.pub"
The authenticity of host '10.0.1.208 (10.0.1.208)' can't be established.
ECDSA key fingerprint is SHA256:J+DCxdUIeiJLsF2PTOD3OB1tEU7HHqvzWMPUM/Tc5cI.
ECDSA key fingerprint is MD5:a5:b5:b7:0f:91:74:ee:fa:c6:4d:ec:58:88:26:aa:a0.
Are you sure you want to continue connecting (yes/no)? yes
/usr/bin/ssh-copy-id: INFO: attempting to log in with the new key(s), to filter out any that are already installed
/usr/bin/ssh-copy-id: INFO: 1 key(s) remain to be installed -- if you are prompted now it is to install the new keys
Password:

Number of key(s) added: 1

Now try logging into the machine, with:   "ssh '10.0.1.208'"
and check to make sure that only the key(s) you wanted were added.

*[cloud_user@server1 ~]$ ssh 10.0.1.208*
[cloud_user@server2 ~]$''