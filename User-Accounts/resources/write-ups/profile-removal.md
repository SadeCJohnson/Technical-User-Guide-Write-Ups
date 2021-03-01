# Removing User Profiles

### Scope
This document will walk you through the process of **removing** a **user profile** in the case of employee termination (whether voluntary or mandatory).

### Audience
* System Administrators

### Tools Required
* Terminal
* Familiarity with *nix(Linux/Unix) commands
* Employee Name

### Removing User Profile

#### Process:
1. Launch the terminal:

![Terminal Launch](/User-Accounts/resources/visual-steps/terminal-launch.gif)

2. Type the  **ls** command into the **terminal prompt** to list the pre-existing users and ensure that the user you wish to remove is listed.

 ```
    ls
 ```
3. Type the following command into the **terminal prompt** to remove the user:

    **In this case, we'll be removing user "**Wiz Khalifa**"**

```
  sudo deluser --remove-home wizkhalifa
```

4. Type **ls** again to confirm that the user has been removed

```
    ls
 ```

![Profile Removal](/User-Accounts/resources/visual-steps/account-removal.gif)

5. Repeat step for any additional users you wish to remove

