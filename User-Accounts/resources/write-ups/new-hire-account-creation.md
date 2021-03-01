# Creating A User Account Via the Terminal

### Scope:
This document will walk you through the process of creating user profiles for new hires via the terminal.

### Audience:
* System Administrators 

### Tools Required:
* Terminal
* Familiarity with *nix(Linux/Unix) commands 
* New Hire Information


**Note: These steps were executed on the Ubuntu Operating System - however this is not a requirement**

### Process:
**1.** Launch the terminal:

![Terminal Launch](/User-Accounts/resources/visual-steps/terminal-launch.gif)

**2.** Let's assume that you need to onboard new hires "**Sade C Johnson**", "**Camille Rose**", etc

   **a.** You will need to type the  **ls** command into the **terminal prompt** to list the pre-existing users and ensure that the user doesn't  already exist.
 
   
    ls
   
   **b.** Once you verify the user doesn't exist, type in **sudo addUser sadecjohnson** 
 
    
    sudo addUser sadecjohnson
    

   **c.** Input the remaining user details to finalize the user profile creation step.
 
   **d.** Repeat these steps for additional new hire profiles that you wish to add.
 
 ![User Account Creation](/User-Accounts/resources/visual-steps/account-creation-6.gif)
 
 
 
    
