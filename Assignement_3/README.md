# User and File Access Management Task

This document provides a step-by-step guide for creating users and setting up file access permissions on a Linux system. The task involves creating users, assigning sudo privileges, and setting up a directory with specific access permissions.

1. Create the Tupu user
![alt](Image/img_1.png)

2. Create the Lupu user
![alt](Image/img_2.png)

3. Create the Hupu system user
![alt](Image/img_3.png)

4. Add Tupu and Lupu to the sudo users
Using visudo to edit the sudoers file:
![alt](Image/img_4.png)

Adding users to the sudo group:
![alt](Image/img_5.png)

5. Create and set up /opt/projekti directory
![alt](Image/img_6.png)

## Explanation
Setting the setgid bit ensures that any files or directories created within _/opt/projekti_ will automatically inherit the projekti group ownership. This maintains the desired permission structure.





