# linux-user-and-group-guide

# 1) Search Words
**Command**: grep

![Screenshot from 2024-11-29 10-54-35](https://github.com/user-attachments/assets/54f32498-e662-4331-8dfc-0659ff584d72)

**Description**: Searches the text file f1.txt for lines containing the word a (case-insensitive).


# 2) Run Multiple Commands

![Screenshot from 2024-11-29 10-57-40](https://github.com/user-attachments/assets/3f4410fb-dc40-48f6-9643-d91b9ca51e34)

**Description**:
- Lists the files and directories in the current path.
- Creates a directory named abc.
- Creates an empty file named f30.
- Lists the updated files and directories.
- End of line ; 

# 3) Pipe Command

![Screenshot from 2024-11-29 11-03-23](https://github.com/user-attachments/assets/f2ede042-c622-4f4f-a6a1-03f889f788d6)

**Description**:
- output of ls -l work as input of head -n 6

![Screenshot from 2024-11-29 11-09-57](https://github.com/user-attachments/assets/9e569d49-36de-4f05-bdc9-27c7d34b84fd)

**Description**:
- Lists files with detailed information.
- Extracts the first 20 lines.
- Retrieves the last 5 of those 20 lines.
- Displays the first of the 5 lines.


# 4) User Management
## Create a User

![Screenshot from 2024-11-29 11-13-02](https://github.com/user-attachments/assets/fe44af57-aa5d-48da-8d4c-0b80d7b36cb0)

## View All Users

![Screenshot from 2024-11-29 11-13-16](https://github.com/user-attachments/assets/811fb9cd-b5fe-4dd8-a721-3acf8b9306ce)

## Verify User's Home Directory

![Screenshot from 2024-11-29 11-17-15](https://github.com/user-attachments/assets/5a0bdea1-1004-408d-8e5d-cd37fe554bc7)

## Delete User


![Screenshot from 2024-11-29 11-19-30](https://github.com/user-attachments/assets/921b8fb2-d0a5-45d1-8f09-86c97be06e76)

## Create User Again
useradd oggy
cat /etc/passwd

![Screenshot from 2024-11-29 11-21-52](https://github.com/user-attachments/assets/bd608239-0f55-4ba7-8927-8c5e6c66e0d3)

Explanation of fields:
oggy: Username
X: Password placeholder
1001: User ID (UID)
1001: Group ID (GID)
home/oggy: Home directory
bin/bash: Default shell


## Change Username

![Screenshot from 2024-11-29 11-23-48](https://github.com/user-attachments/assets/088a87dc-7254-477c-a44a-0bd8eb733546)

cat /etc/passwd

![Screenshot from 2024-11-29 11-25-03](https://github.com/user-attachments/assets/ed62aac3-24f0-49be-a4c0-fb0737a7ecc3)



## Change User ID

![Screenshot from 2024-11-29 11-27-20](https://github.com/user-attachments/assets/a05f3902-0e53-48e1-ab4a-fa3a46710865)


![Screenshot from 2024-11-29 11-27-53](https://github.com/user-attachments/assets/6980e09b-be81-4e75-a184-3bbb01fb3203)




## Add Full Name

![Screenshot from 2024-11-29 11-29-17](https://github.com/user-attachments/assets/5a21a1a8-db6c-41bf-9ab0-15c4ed66553f)

![Screenshot from 2024-11-29 11-29-54](https://github.com/user-attachments/assets/1f544029-1003-495c-be24-b7da8ea4dfd6)

## Change Home Directory

![Screenshot from 2024-11-29 11-34-39](https://github.com/user-attachments/assets/d9b2542b-3194-49e0-ba9b-4f0b2282af5b)

![Screenshot from 2024-11-29 11-33-57](https://github.com/user-attachments/assets/7247c105-13f8-4f69-b915-9eff185058f8)

cat /etc/passwd

![Screenshot from 2024-11-29 11-35-18](https://github.com/user-attachments/assets/bf7f8330-5d8c-492e-96f5-23279e67ba7a)



## Change Shell Location

![Screenshot from 2024-11-29 11-36-50](https://github.com/user-attachments/assets/89385660-f238-4702-9ac7-eb3ed14ca14d)

![Screenshot from 2024-11-29 11-38-03](https://github.com/user-attachments/assets/5ffd1399-c67b-4f6f-b253-17a66c8c4dc4)

Again change / to  /bin/bash

![Screenshot from 2024-11-29 11-39-20](https://github.com/user-attachments/assets/b96b61c4-5884-435f-85ad-de5583523518)


## Set Password

![Screenshot from 2024-11-29 11-40-26](https://github.com/user-attachments/assets/59625b81-23a4-4606-bc3e-17ecd3ad7efe)

## Login and Check Password File
- login as varun

![Screenshot from 2024-11-29 11-42-15](https://github.com/user-attachments/assets/5d8bf557-498d-423b-a529-20af8403e02d)

when we login as user, '#' is chanage into '$' 

![Screenshot from 2024-11-29 11-44-13](https://github.com/user-attachments/assets/6c1417b3-c88e-4eb0-8ab1-69e8adaa9af2)

'su' cammand use return to root 

- password file are present in 
cat /etc/shadow

![Screenshot from 2024-11-29 11-49-06](https://github.com/user-attachments/assets/6e5df49d-d827-416e-bdc9-cdcf76ab9b44)

Fields explained:

![Screenshot from 2024-11-29 11-48-06](https://github.com/user-attachments/assets/06ce04f1-a14a-441f-a01e-6627b60406b6)


## Manage Password Settings

![Screenshot from 2024-11-29 11-53-42](https://github.com/user-attachments/assets/e04370b4-740a-44fb-8d1b-5582dc124dba)

- chage -E "2024-09-23" varun  for account expire
- chage -I 3 varun for password inactive 

# 5) Group Management
## Add Group
Command:
groupadd goal1
cat /etc/group




## Delete Group
Command: groupdel goal1


## Modify Group ID
Command: groupmod -g 1232 goal1


## Change User's Primary Group
Commands:
cat /etc/passwd
groups varun
usermod -g goal1 varun




## Add User to Additional Groups
Command: gpasswd -g A1 -a varun


## Remove User from Group
Command: gpasswd -g A1 -d varun


## Add Multiple Users to a Group
Command:
gpasswd -M sam,tom,rj,jack goal1
group sam
group tom
group rj




## Check Group Members
Command: groupmems -l -g goal1


## Add User to Multiple Groups
Command:
useradd jj
usermod -G a1,b1,c1 -a jj
groups jj




## Change Group Name
Command: groupmod -n goold goal1


# 6) Assign Permissions for User Management
## File to Edit: /etc/sudoers
Add the line to grant varun privileges:
varun ALL=(ALL) ALL





Description: Comprehensive guide for managing users, groups, and permissions on Linux, with practical examples and screenshots.


