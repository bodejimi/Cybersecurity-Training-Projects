# File permissions in Linux
#Project description
In this project I will examine existing permissions on a file system. I’ll  determine if the permissions match the authorization that should be given. If they do not match, I’ll modify the permissions to authorize the appropriate users and remove any unauthorized access.

# File and directory details
drwxr-xr-x 3 researcher2 research_team 4096 Jul 14 19:56 .
drwxr-xr-x 1 root        root          4096 Jul 14 19:56 ..
-rw------- 1 researcher2 research_team   10 Jul 14 20:00 .bash_history
-rw-r--r-- 1 researcher2 research_team  220 Mar 27  2022 .bash_logout
-rw-r--r-- 1 researcher2 research_team 3574 Jul 14 19:56 .bashrc
-rw-r--r-- 1 researcher2 research_team 3574 Jul 14 19:56 .profile
drwxr-xr-x 3 researcher2 research_team 4096 Jul 14 19:56 projects

# Description of the permissions string
drwxr-xr-x 3 researcher2 research_team 4096 Jul 14 19:56 projects
Descriptions of the permissions string
d — This is a directory.
rwx — Owner can read, write, and execute.
r-x — Group can read and execute.
r-x — Others can read and execute.
Each character in the 10-character string represents either the type or permission setting for the file.

# Changing file permissions on a hidden file
I ran command chmod u-r projects to remove the write permission from  user
# Resulting Permissions
drwxr-xr-x 3 researcher2 research_team 4096 Jul 14 19:56 .
drwxr-xr-x 1 root        root          4096 Jul 14 19:56 ..
-rw------- 1 researcher2 research_team   36 Jul 14 20:26 bash_history
-rw-r--r-- 1 researcher2 research_team  220 Mar 27  2022 .bash_logout
-rw-r--r-- 1 researcher2 research_team 3574 Jul 14 19:56 .bashrc
-rw-r--r-- 1 researcher2 research_team 3574 Jul 14 19:56 .profile
dr-xr-xr-x 3 researcher2 research_team 4096 Jul 14 19:56 projects

# Changing directory permissions
I ran command  chmod g-x,o-x projects to remove execution permissions for group and others
# Resulting Permissions
drwxr-xr-x 3 researcher2 research_team 4096 Jul 14 19:56 .
drwxr-xr-x 1 root        root          4096 Jul 14 19:56 ..
-rw------- 1 researcher2 research_team   66 Jul 14 20:30 bash_history
-rw-r--r-- 1 researcher2 research_team  220 Mar 27  2022 .bash_logout
-rw-r--r-- 1 researcher2 research_team 3574 Jul 14 19:56 .bashrc
-rw-r--r-- 1 researcher2 research_team 3574 Jul 14 19:56 .profile
dr-xr--r-- 3 researcher2 research_team 4096 Jul 14 19:56 projects

# Summary
In this project, I explored some fundamentals of Linux, focusing on file and directory permissions. I used commands like ls -la to view detailed file information, including hidden files and permission settings. I also used the chmod command to modify access permissions for a file or directory. Through these tasks, I gained practical experience in managing user access, an essential part of system administration and Linux file security.