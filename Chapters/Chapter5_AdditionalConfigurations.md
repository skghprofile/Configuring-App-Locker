# Chapter 5 - Additional Configurations

## Introduction

In this chapter, there will be a few other configurations I want to change that are related to AppLocker and PC security.

## Issue With AppLocker Blocking PowerShell Scripts

Despite setting AppLocker rules to block all unsigned PowerShell scripts, they still run in [Constrained Language Mode](https://devblogs.microsoft.com/PowerShell/PowerShell-constrained-language-mode/). This mode theoretically limits script capabilities, but malicious scripts can bypass it in several ways.

One common method is using a different version of PowerShell, such as PowerShell 2.0, which can be enabled through the Windows Features menu, or PowerShell 7.x, which can be installed via various methods [here](https://learn.microsoft.com/en-us/PowerShell/scripting/install/installing-PowerShell-on-windows?view=PowerShell-7.4).

To mitigate these risks, uninstall or disable these PowerShell versions. Since I don’t have PowerShell 7.x installed, I only needed to ensure PowerShell 2.0 is disabled in the "Windows Features” menu:

![Windows Features Window](/Images/AL-img38.png)

Another bypass method involves changing the execution policy with simple commands. For example:

```
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```


By default, the script's execution policies should be "Undefined," which is equivalent to "Restricted" but can be easily bypassed.

Below are my current PowerShell script execution policies:

![PowerShell Window](/Images/AL-img39.png)

To prevent malicious scripts from bypassing AppLocker and altering execution policies, I need to set the "MachinePolicy” scope to allow only signed scripts. The "MachinePolicy" scope has the highest authority and is executed before the "Process" scope.

To change the "MachinePolicy" scope, I need to navigate to the "Turn on Script Execution" setting in the Windows PowerShell folder in the Local Group Policy Editor.

Windows PowerShell folder path in Group Policy Editor: **Computer Configuration > Administrative Templates > Windows Components > Windows PowerShell**

![Windows PowerShell Folder in Local Group Policy Editor Window](/Images/AL-img40.png)

Double-clicking on the "Turn on Script Execution" setting opens it up in a new window. In that new window, I selected the "Enabled" radio button and selected the "Allow only signed scripts" in the Execution Policy dropdown menu. I then clicked the "Apply" and then "OK" button to save the changes

![Turn On Script Execution Window](/Images/AL-img41.png)

With the changes saved, I opened a new PowerShell window and input the "Get-ExecutionPolicy -List" command to ensure that the changes were applied correctly.

As shown in the image below, the "Machine Policy" execution policy is now "AllSigned" instead of "Undefined".

![PowerShell Window](/Images/AL-img42.png)
