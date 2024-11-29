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

![Screenshot from 2024-11-29 13-07-52](https://github.com/user-attachments/assets/0b24f50e-1c38-4032-8592-0f99482b6c73)

![Screenshot from 2024-11-29 13-10-28](https://github.com/user-attachments/assets/69ef58dd-459a-478f-a5d4-5db512467e65)

![Screenshot from 2024-11-29 13-11-28](https://github.com/user-attachments/assets/1cf8cbda-b761-4c97-98a0-c733b80b8428)


## Delete Group

![Screenshot from 2024-11-29 13-15-51](https://github.com/user-attachments/assets/7e911f4b-35ac-43e5-a57a-e61e77ef1638)



## Modify Group ID

![Screenshot from 2024-11-29 13-12-41](https://github.com/user-attachments/assets/ba31edee-3dc6-4d6d-b9ad-2e73da747f9b)

![Screenshot from 2024-11-29 13-12-59](https://github.com/user-attachments/assets/3666efed-a63f-4dec-86da-d18e4ba5355b)



## Change User's Primary Group

![Screenshot from 2024-11-29 13-18-18](https://github.com/user-attachments/assets/043d49ba-f162-4112-a6d2-90941a377362)

![Screenshot from 2024-11-29 13-18-33](https://github.com/user-attachments/assets/c1f8a4b0-0559-430d-872b-ef41af5d70dc)

![Screenshot from 2024-11-29 13-20-36](https://github.com/user-attachments/assets/193cf6cb-5bd7-4064-b218-fae582baaf82)

## Add User to Additional Groups

![Screenshot from 2024-11-29 13-26-22](https://github.com/user-attachments/assets/491c6319-427b-43a6-8ac1-ca2df6f6b9fd)

![Screenshot from 2024-11-29 13-28-15](https://github.com/user-attachments/assets/1011ea49-f973-4af0-ae8a-4dff3b5f8c04)



## Remove User from Group

![Screenshot from 2024-11-29 13-29-21](https://github.com/user-attachments/assets/f64b99a9-71c1-4653-8d6f-e19cd353e49b)


## Add Multiple Users to a Group

![Screenshot from 2024-11-29 13-33-43](https://github.com/user-attachments/assets/9c793679-3853-440d-a68e-65086bc4bf71)

## Check Group Members

![Screenshot from 2024-11-29 13-34-51](https://github.com/user-attachments/assets/b9b73292-e477-4018-9072-1f9bd90a9bcb)



## Add User to Multiple Groups

![Screenshot from 2024-11-29 13-36-54](https://github.com/user-attachments/assets/05a88e1f-3eb1-4590-9671-b4a8361c6466)

## Change Group Name

![Screenshot from 2024-11-29 13-38-42](https://github.com/user-attachments/assets/7838ede9-ae71-4ad0-8e6a-cbd323bbfb7b)


# 6) Assign Permissions for User Management

![Screenshot from 2024-11-29 13-41-02](https://github.com/user-attachments/assets/3a1f8e80-dabc-4cff-8854-c34fe7190d78)

![Screenshot from 2024-11-29 13-43-02](https://github.com/user-attachments/assets/123305df-fe7c-431b-b6b1-bc23c9d1c170)

![Screenshot from 2024-11-29 13-44-20](https://github.com/user-attachments/assets/76d39baf-0c48-4a7d-a5cb-2a2f40e01171)


## File to Edit: /etc/sudoers
Add the line to grant varun privileges:
varun ALL=(ALL) ALL

![Screenshot from 2024-11-29 13-46-00](https://github.com/user-attachments/assets/ba1b5578-de11-41f8-97f4-b4d5d3d80b58)




Description: Comprehensive guide for managing users, groups, and permissions on Linux, with practical examples and screenshots.


