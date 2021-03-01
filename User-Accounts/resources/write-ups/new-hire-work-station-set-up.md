# Creating The New Hire Workstation

### Scope
This document will walk you through the process of **creating folders** for new hires, **managing folder permissions**
and **installing applications** via the **terminal**.

### Audience
* System Administrators 

### Tools Required
* Terminal
* Familiarity with *nix(Linux/Unix) commands 
* New Hire Information
* New Hire Role-based Access Control (RBAC) Company Policy 
    * This is to ensure that each new hire receives the rightful permissions


**Note: These steps were executed on the Ubuntu Operating System - however this is not a requirement**

### Process
#### Creating mandatory folders:
1. Launch the terminal:

![Terminal Launch](/User-Accounts/resources/visual-steps/terminal-launch.gif)

2. It is mandatory for all new hires to have the following directories under their profiles:
    
* **work-resources**
    * This directory will hold all important work documents, including tax information, HR references, etc.
* **hire-info**
    * This directory will hold all onBoarding information to ensure new hires will have access to the documents instructing them 
      on getting set-up on **day 1**.
    

Accordingly, these directories will need to be created.
To create the **work-resources** directory for **Camille Rose**, type the following into the **terminal**:
```
    sudo mkdir camillerose/work-resources
```

3. After the **work-resources** directory is created for **Camille Rose**, run the following command to verify that it exists:
```
    ls -l camillerose/
```


4. After verifying the directory has successfully been created, the same process can be followed to create the **work-resources** directory for remaining new hires.
```
    sudo mkdir sadecjohnson/work-resources; sudo mkdir wizkhalifa/work-resources
```

5. Verify the creation of these directories via:

```
    ls -l sadecjohnson/
```

```
    ls -l wizkhalifa/
```

**OR** via:

```
    ls -l sadecjohnson/; ls -l wizkhalifa
```

6. To create the **hire-info** directory for **Camille Rose**, and the other new hires, type the following into the **terminal**:
```
    sudo mkdir camillerose/hire-info; sudo mkdir sadecjohnson/hire-info; sudo mkdir wizkhalifa/hire-info
```  

7. Verify the creation of all new hire directories:

```
    ls -l camillerose/; ls -l sadecjohnson; ls -l wizkhalifa
```


![Folder Creation](/User-Accounts/resources/visual-steps/folder-creation.gif)


#### Managing permissions:

1. Type the following command into the **terminal prompt** to view the initial **permissions** granted to the new hire mandatory 
folders:
   
**Note: The following command will check all the file permissions in a single line**
   
```
    ls -l camillerose/; ls -l sadecjohnson/; ls -l wizkhalifa/ 
```

2. If the **permissions** listed are **read, write, execute** (**rwx**), we will need to change the folder permissions to 
**read** only, and revoke the **write** and **execute** **permissions**. This can be done via the following command:
   
```
    sudo chmod 0444 camillerose/hire-info/; sudo chmod 0444 camillerose/work-resources; ls -l
```

Running the **ls -l** command at the end will verify that the **permissions** have been properly updated.

3. Repeat these same steps for remaining new hires. A visual of this process can be found below:



![Managing Permissions](/User-Accounts/resources/visual-steps/manage-permissions-2.gif)


#### App installation:

1. New Hires will need to have the right developer tools on their workstations to be productive. To ensure
productivity, apps will need to be installed as follows:
   
**Note: The app to be installed for this demonstration will be  **handbrake**, a video editing tool.**

```
    sudo apt-get install handbrake

```

2. Enter the system administrator password.
3. The specified app will successfully be installed.

![App Installation](/User-Accounts/resources/visual-steps/app-installation-6.gif)

**All tools installed on the admin account, will also be reflected under the new hire account profiles, since the new hires will
inherit the properties of the system admin parent account.**

   




    


### Future Implementation

1. Include steps to **verify app versions** to ensure workstation environment consistency.
2. Include steps to **update apps** to ensure the latest tools are being used.

**All implementations will come with the respective visuals to properly demonstrate how these tasks would be completed.** 
 
 
    
