# Chapter 1 - Creating AppLocker Group Policy Snap-In (Shortcut)

## Introduction 

In this chapter, I will walk through the process of creating a snap-in or shortcut to the AppLocker section in the group policy editor since I plan on continually configuring AppLocker in the future. This will save a lot of time since all I will have to do is double-click an icon instead of navigating through the various menus in the group policy editor to get to the AppLocker section.

Before creating the snap-in, I will demonstrate the standard process of navigating through the group policy editor to get to the AppLocker settings/configuration:

1. Open the Windows Search menu and search for "group policy" or "edit group policy" and click the result "Edit group policy" with the icon and subheading of the Windows Control Panel.

![Group policy icon in Windows Search menu](/Images/AL-img01.png)

2. This will open the Local Group Policy Editor. From here there are a couple of menus I need to navigate through to get to the AppLocker settings/configuration.

Navigation Path to AppLocker: **Local Computer Policy > Computer Configuration > Windows Settings > Security Settings > Application Control Policies > AppLocker**

![AppLocker navigation in Local Group Policy Editor](/Images/AL-img02.png)

## Creating the AppLocker Snap-In (Shortcut)

From the example above, double clicking an icon would be much faster than going through all those steps and menus to get to the AppLocker settings/configuration menu.

Below is the process of creating the snap-in (shortcut) that navigates directly to the AppLocker settings/configuration menu:

1. Open the Windows Search menu and search "mmc" for the Microsoft Management Console and click the result with the red toolbox.

![Microsoft Management Console result in Windows Search](/Images/AL-img03.png)

2. With the Microsoft Management Console now open, click the "File" button in the top left of the window and then click the option "Add/Remove Snap-in"

![Microsoft Management Console](/Images/AL-img04.png)

3. In the Add or Remove Snap-ins window, click "Group Policy Objects" in the Available snap-ins selection box and then click "Add >" in the middle of the window.

![Add or Remove Snap-ins window](/Images/AL-img05.png)

4. Once the "Select Group Policy Object" window opens, click the "Finish" button at the bottom to close the window.

![Select Group Policy Object window](/Images/AL-img06.png)

5. To confirm that the "Group Policy Object" snap-in has been added, look at the right side of the Add or Remove Snap-ins window and in "Selected snap-ins" section, confirm that the "Local Computer Policy" object is added under the "Console Root" folder.

If everything is created successfully and in the correct place, click the "OK" button to close the "Add or Remove Snap-ins" window.

![Add or Remove Snap-ins window](/Images/AL-img07.png)

6. Now the mmc window should look similar to the local group policy editor shown earlier in this chapter. Now it's time to navigate through the menus once again to get to AppLocker settings/configuration.

Navigation Path to AppLocker: **Local Computer Policy > Computer Configuration > Windows Settings > Security Settings > Application Control Policies > AppLocker**

This time, right click the AppLocker text/icon to open the context menu and click "New Window from Here" to open AppLocker settings/configuration in its own separate window.

![Microsoft Management Console window](/Images/AL-img08.png)

7. Once in the new window, click "File" in the top left and then "Save As..." to save the snap-in as a shortcut.

![Microsoft Management Console AppLocker new window](/Images/AL-img09.png)

8. From here, I wanted to save the snap-in AppLocker shortcut to my desktop for easy access so I clicked the "Desktop" button on the left side of the "Save As" window and renamed the .msc file to "AppLockerSnapIn.msc" and clicked the "Save" button to create the shortcut.

![Microsoft Management Console AppLocker Save As... window](/Images/AL-img10.png)

9. To confirm that the snap-in shortcut was successfully created, I navigated to my Desktop and searched for the "AppLockerSnapIn.msc" icon with the red toolbox.

![AppLockerSnapIn.msc icon on Desktop](/Images/AL-img11.png)

10. Before actually configuring AppLocker, there was one last option I needed to change so that I wouldn't have to save the snap-in shortcut each time I changed something in AppLocker.

To do this, I double clicked the newly created "AppLockerSnapIn.msc" shortcut on my Desktop. In the new window that opened, I clicked "File" in the top left and then "Options" to open the options window.

In the options window, I changed the Console mode dropdown to "User mode - full access" and made sure that the "Do not save changes to this console" checkbox is checked/enabled.

I then clicked the "OK" button and then clicked the "File" button in the top left of the window and finally the "Save" option to save the changes.

![AppLockerSnapIn.msc window](/Images/AL-img12.png)

## Next Chapter: 
### [Chapter 2 - Enabling AppLocker](/Chapters/Chapter2_EnablingAppLocker.md)