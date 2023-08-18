# Altschool cloud engineering assignment

## create a new user
Code: sudo useradd Tobi

**Screenshot of the user add process below;**
I had to create a new link for the images on Git directly because the initial screenshot link kept generating errors. However the screenshots below in the respective questions shows the process and commands/codes.
![ScreenShot_Vagrantfile_useradd](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/adb87429-a12a-4938-b2b3-f577b65fd577)

## set an expiry date of 2weeks for the user
code: sudo usermod -e $(date -d "+2 weeks" +%Y-%m-%d) Tobi

**Screenshot of set an expiry date of 2weeks for the user**
![SS_Expirydate_Tobi](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/597a800d-5a6e-4282-bdc9-b688d5db80bc)

## prompt the user to change there password on login
code: sudo chage -d 0 Tobi

**Screenshot change passwd**
![Screen Shot 2023-08-18 Change passed at 6 57 18 PM](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/8c675f05-d052-4375-bd75-9a8779148848)


## attach the user to a group called altschool
code: sudo usermod -aG altschool Tobi

**Screenshot attach the user to a group called altschool!**
![Screen Shot 2023-08-18 attach the user to a group called altschoolat 7 01 30 PM](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/fcaf7181-18c4-4bb7-ba26-c0918c3e6ab7)

## allow altschool group to be able to run only cat command on /etc/
Steps
** sudo Visudo
** Scroll down to the section that defines user and group privileges. 
** Add a line to allow the "altschool" group to run only the **cat** command on **/etc/**. Add the below code line under the existing group definitions:
code: **%altschool ALL=(ALL) /bin/cat /etc/***
** Save the file and exit the text editor.
All of the "altschool" group now have the right to run only the **cat** command on files within the **/etc/** directory using sudo privileges.

**Screenshot allow altschool group to be able to run only cat command on /etc/**
![Screen Shot 2023-08-18 allow altschool group to be able to run only cat command on :etc: 1 at 7 16 13 PM](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/a46c4b8f-eb1a-4de3-8dea-382f62f21b2e)

![Screen Shot 2023-08-18 allow altschool group to be able to run only cat command on :etc: 2 at 7 18 08 PM](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/d08fa322-decf-4a50-bf27-9dcf642a1d99)



## create another user. make sure that this user doesn't have a home directory.
 code: sudo useradd -M Kavod

**Screenshot create another user. make sure that this user doesn't have a home directory**
 ![Screen Shot 2023-08-18 create another user  make sure that this user doesn't have a home directory at 7 27 38 PM](https://github.com/RansomedKC/CloudEngineering-Assignment1/assets/137722760/e94c17e4-3e34-4641-8837-7d99fb276a53)
