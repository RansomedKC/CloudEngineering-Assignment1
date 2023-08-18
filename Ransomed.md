# Altschool cloud engineering assignment

## create a new user
Code: sudo useradd Tobi
**Screenshot of the user add process below;**
![Sudo Useradd Tobi](/ScreenShot_Vagrantfile_useradd.png)


## set an expiry date of 2weeks for the user
code: sudo usermod -e $(date -d "+2 weeks" +%Y-%m-%d) Tobi
**Screenshot of set an expiry date of 2weeks for the user**
![Sudo set an expiry date Tobi](/SS_Expirydate_Tobi.png "Sudo expiry date set for Tobi")

## prompt the user to change there password on login
code: sudo chage -d 0 Tobi
**Screenshot change passwd**
![prompt the user to change there password on login!](/Screen%20Shot%202023-08-18%20Change%20passed%20at%206.57.18%20PM.png "Sudo change passwd")


## attach the user to a group called altschool
code: sudo usermod -aG altschool Tobi
**Screenshot attach the user to a group called altschool!**
![attach the user to a group called altschool!](/Screen%20Shot%202023-08-18%20attach%20the%20user%20to%20a%20group%20called%20altschoolat%207.01.30%20PM.png"attach the user to a group called altschool")

## allow altschool group to be able to run only cat command on /etc/
Steps
** sudo Visudo
** Scroll down to the section that defines user and group privileges. 
** Add a line to allow the "altschool" group to run only the **cat** command on **/etc/**. Add the below code line under the existing group definitions:
code: **%altschool ALL=(ALL) /bin/cat /etc/***
** Save the file and exit the text editor.
All of the "altschool" group now have the right to run only the **cat** command on files within the **/etc/** directory using sudo privileges.

**Screenshot allow altschool group to be able to run only cat command on /etc/**
![allow altschool group to be able to run only cat command!](/Screen%20Shot%202023-08-18%20allow%20altschool%20group%20to%20be%20able%20to%20run%20only%20cat%20command%20on%20%3Aetc%3A%201%20at%207.16.13%20PM.png "allow altschool group to be able to run only cat command")
![allow altschool group to be able to run only cat command2!](/Screen%20Shot%202023-08-18%20allow%20altschool%20group%20to%20be%20able%20to%20run%20only%20cat%20command%20on%20%3Aetc%3A%202%20at%207.18.08%20PM.png "allow altschool group to be able to run only cat command2")


## create another user. make sure that this user doesn't have a home directory.
 code: sudo useradd -M Kavod
 **Screenshot create another user. make sure that this user doesn't have a home directory**
 ![create another user. make sure that this user doesn't have a home directory!](/Screen%20Shot%202023-08-18%20create%20another%20user.%20make%20sure%20that%20this%20user%20doesn't%20have%20a%20home%20directory%20at%207.27.38%20PM.png "create another user. make sure that this user doesn't have a home directory")
