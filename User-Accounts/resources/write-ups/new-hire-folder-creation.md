# Creating Mandatory Folder Structures For New Hires

### Scope:
This document will walk you through the process of creating folders for new hires, managing these permissions
and installing applications via the **terminal**.

### Audience:
* System Administrators 

### Tools Required:
* Terminal
* Familiarity with *nix(Linux/Unix) commands 
* New Hire Information
* New Hire Role-based Access Control (RBAC) Company Policy 
    * This is to ensure that each new hire receives the rightful permissions


**Note: These steps were executed on the Ubuntu Operating System - however this is not a requirement**

### Process:
1. Launch the terminal:

![Terminal Launch](/User-Accounts/resources/visual-steps/terminal-launch.gif)

2. It is mandatory for all new hires to have the following directories under their profiles:
    
* **work-resource**
    * This directory will hold all important work documents, including tax information, HR references, etc.
* **hire-info**
    * This directory will hold all onboarding information so the new hires will know how to get set-up on **day 1**.
    

Accordingly, these directories will need to be created.
To create the **work-resources** directory for **Camille Rose**, type the following into the **terminal**:

    sudo mkdir camillerose/work-resources

3. After the **work-resources** directory is created for **Camille Rose**, run the following command to verify that it exists:

    ls -l camillerose/

4. After verifying the directory has successfully been created, the same process can be followed for additional new hires.

![Terminal Launch](/User-Accounts/resources/visual-steps/folder-creation.gif)

    


### Future Implementation:

1. Include steps to **verify app versions** to ensure consistency
2. Include steps to **update apps** to ensure the latest tools are being used

**All implementations will come with the respective visuals to properly demonstrate how these tasks would be completed.** 
 
 
    
