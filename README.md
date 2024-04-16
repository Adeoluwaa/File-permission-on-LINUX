
# File Permission with LINUX

## Objective

To use Linux commands to modify file permissions, ensuring secure access and proper management of sensitive data and system files.

## Project description

I was tasked with updating the file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure. To complete this task, I performed the following tasks:


### Skills Learned

File Permission Management: Learning to change file permissions on Linux requires understanding of file ownership (user and group), file access modes (read, write, execute), and the use of chmod, chown, and chgrp commands. It also involves grasping the concept of file permissions for different user categories (owner, group, others) and applying these permissions securely to protect sensitive files and directories.

### Command Used

chmod: This command is used to change the permissions (read, write, execute) of a file or directory. For example, chmod u+x file.txt adds execute permission for the file's owner.

chown: Used to change the ownership of a file or directory. For instance, chown user:group file.txt changes the owner and group of file.txt.

chgrp: This command changes the group ownership of a file or directory. For example, chgrp group file.txt changes the group of file.txt to the specified group.

## Steps
## Check file and directory details.
To check file permission for /home/researcher2/projects , I used: **ls -l** while in the projects directory.

![Screenshot (159)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/571678a9-e599-4ef8-8c0f-ae107b1c1710)

 To check for hidden files in /home/researcher2/projects. I used: **ls-a** while in the projects directory.

 ![Screenshot (160)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/25e33851-b008-4a34-bbc3-d7cc2f47710a)

To check whether any files in the projects directory have write permissions for the owner type of other, I used: **ls-l** while in the projects directory
To change the permissions of the file so that the owner type of other doesn’t have write permissions, I used: **chmod o-w project_k.txt**

![Screenshot (161)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/276a25c1-4113-460b-a6b9-1be9c9b8c6a4)

To list the contents and permissions of the current directory and check if the group has read or write permissions, I used: **ls -l**
To change permissions of the project_m.txt file so that the group doesn’t have read or write permissions, I used: **chmod g-r project_m.txt**

![Screenshot (162)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/29fa1bc4-2081-420f-8055-93d8bc69aec7)

## Change file permissions on a hidden file
The research team has archived .project_x.txt, which is why it’s a hidden file. This file should not have write permissions for anyone, but the user and group should be able to read the file. 
To  check the permissions of the hidden file .project_x.txt , I used : **ls -la**

![Screenshot (163)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/1433830d-ac7b-4c7a-83f4-a7e8248a999e)

To change the permissions of the file .project_x.txt so that both the user and the group can read, but not write to, the file, I used: 
**Chmod u-w .project_x.txt**
**Chmod g-w .project_x.txt**
**Chmod g+r .project_x.txt**

![Screenshot (164)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/6f0df205-f162-4433-9765-1449cd1ba608)

## Change directory permissions
The files and directories in the projects directory belong to the researcher2 user. Only researcher2 should be allowed to access the drafts directory and its contents. 

To check permissions of the drafts directory, under the  /home/researcher2/projects/drafts directory, I used: **ls-l**

To remove the execute permission from the group user, i used: **chmod g-x drafts**

![Screenshot (165)](https://github.com/Adeoluwaa/File-permission-on-LINUX/assets/158221954/15d655d0-5760-4e52-9872-b6e5fd82db50)


